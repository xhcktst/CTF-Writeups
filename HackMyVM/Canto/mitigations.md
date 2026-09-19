# Mitigations 🔐

For this specific scenario, there are some major important configurations that would have prevented this attack:

##### 1) Correct update policy 💾
The first flawn exploited was an outdated version of plugin that contained vulnerabilities. Implementing a correct policy to update wordpress, plugins and themes would fix this issue.

**Recommendation**: set up automatic updates in wordpress. Find more on how to set automatic updates in this [wordpress article.](https://wordpress.org/documentation/article/plugins-themes-auto-updates/) 

##### 2) Properly manage sensitive information 👁️
We got access as user "erik" because the password was stored in plain text in a file with reading permits for everyone. Storing passwords in files is NOT recommended in anycase. Files containing sensitive information should have restricted access to only the users that requires to have access to such information.

**Recommendation**: for password management, implement a secure password manager. This not only will help to use/store/remember passwords but some of them also provides alerts to change password periodically and implement a correct password policy in the organization.

Additionally, for files containing sensitive information that user "erik" needs to access it is recommended to use the correct permits. You can find more about file and directories permits [here](https://www.computerhope.com/unix/uchmod.htm) 

In this specific case the file containing the password for erik have reading permits for everyone. 
This can be solved easily:

1) **Only root needs access:** 

As root we execute:

```terminal
chmod 700 [filename]
```

2) **root and "erik" need access:**

We first need to change the ownership if the file is owned by root and group is also root. We run as root:

```terminal
chown root:erik [filename]
```

The configuration would be now owner=root and group=erik. So now as root we change the permits:

```terminal
chmod 740 [filename]
```

This will basically give full permits to root and "only read" permits to Erik. No one else can access.

##### 3) sudo permits 👮‍♂️
We got access as root for a misconfigured sudo permits without the need to use any password. Erik can run "cpulimit" as root, being able to do that allowed us to exploit this vulnerability to escalate priviledge. 

**Recommendation**: remove any unnecesary user from sudoers lists. If certain user requires to be in the list implement a password configuration so anyone that want to run as root needs to introduce the password.

**Example in this machine:**

![](./assets/Canto_12.png)

As we can see the user "Erik" is in the sudoers files with NOPASSWD set. This is how we can escalate privileges. In this current example, assuming erik needs to be able to run `cpulimit`as root I would suggest a simple change in the file to ask for the root password. Basically we need to add default configuration that will ask for root password.

We need to be "root" to be able to modify the sudoers file. We execute:

```terminal
sudo visudo
```

**Note**: important to use "visudo" to edit this file, any error in syntax here could be catastrophic.

We add the following line in defaults

```editor
Defaults rootpw
```

and we modify Eriks line:

``` editor
erik    ALL=(ALL:ALL) /usr/bin/cpulimit
```

The file should look like this:

![](./assets/Canto_13.png)

Now if we try to escalate privileges like we did before, it's not going to work:

![](./assets/Canto_14.png)


