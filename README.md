# Wazo_phonebook_default_profile
Wazo Patch phonebook always use default profile &lt;=19.11
<br><br>
Create by Wazo Team 
<br><br>
# Install 
Copy file in root directory<br>
```console
$ cd /usr/lib/python2.7/dist-packages
$ patch -p1 < ~/0001-phonebook-always-use-default-profile.patch
$ rm provd/phonebook.pyc
$ systemctl restart xivo-provd
``` 
<br>
Now you can reconfigure your devices <br>

```console 
$ xivo-provd-cli
xivo-provd-cli> for device in devices.find(recurse=True):
xivo-provd-cli>   devices.reconfigure(device)
``` 
