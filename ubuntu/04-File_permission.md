### File Permission

#### Add User

```
sudo adduser username
```

#### Give permission to user use sudo

```
sudo visudo
```

--------------Open edit file with nano also
This will open the sudoers file in a text editor. Look for a line that includes the phrase %sudo ALL=(ALL:ALL) ALL.
Add a new line below that line and enter: username ALL=(ALL:ALL) ALL
Save the file and exit the text editor.

```
username ALL=(ALL) ALL
```

#### Add under group any user

```
sudo usermod -aG sudo username
```

// www-data - group name, $USER - get automatic current user, also can use username like `$ sudo usermod -aG www-data asifulmamun`, here usermod user adding under the www-data group
// Check - also you can check how many groups using the user username with this comman `$ grep -i --color 'username' /etc/group`

```
sudo usermod -aG www-data $USER
```

// $USER change also with username like as `su mostafizur`

```
su $USER
```

#### Show all users in ubuntu

```
cut -d: -f1 /etc/passwd
```

or

```
compgen -u
```

or

```
getent passwd
```

#### Show all Groups in ubuntu

```
compgen -g
```

or

```
getent group
```

#### Show User info - mostafizur user replace with your username

```
getent passwd mostafizur
```

#### Show group info user - mostafizur user replace with your username

```
grep -i --color 'mostafizur' /etc/group
```

#### Add user mostafizur and group www-data - mostafizur can access file like as owner also www-data because mostafizur also www-data group member

```
sudo chown -R $USER:www-data filename.txt/foldername
```

1. $USER - also change with asifulmamun but need write permission to group
2. Permission to grop `$ sudo chmod -R g+w html`

---

[BACK Ubuntu Main](ubuntu-main.md)
<br/>
[BACK Main](../README.md)
