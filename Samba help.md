## Backup the main samba file
`sudo mv smb.conf smb.conf.sav`

## OhHeyItsLou
### Add the following in the new smb.conf file

```
[global] 
    server string = Lou‘s Linux Box
    workgroup = THEANALOGKID
    netbios name = lobo
    security = user
    encrypt passwords = yes
    guest account = nobody
    name resolve order = bcast host
    hosts allow = 192.168.0.0/16
    hosts deny = 0.0.0.0/0
    include = /etc/samba/smbshared.conf
```

### Add folders to be shared by using following code as a template. Add the code to the file smbshared.conf    
```
[Music]    
    comment = Linux File Server Share
    path = /mediaLou/Storage/Music
    Browsable = yes
    guest ok = yes
    Read only = yes
    available - yes
    public = no
    writable = no
    valid users = lobo

[Videos]
    comment = Linux File Server Share
    path = /home/lobo/Videos/
    Browsable = yes
    guest ok = yes
    Read only = yes
    available - yes
    public = no
    writable = no
    valid users = lobo
```    
    
### Create user and user password for sambs  

`sudo smbpasswd -a <username>`

`sudo gedit /etc/samba/smbusers`

### Add the following to smbusers
   ```
   <username> = “<username>"
  ```
### Allow firewall pass
    `sudo ufw allow Samba`
    

## Chris
```    
[global] 
    server role = standalone server
    map to guest = bad user
    usershare allow guests = yes
    hosts allow = 192.168.0.0/16
    hosts deny = 0.0.0.0/0

[linuxsharename]
    comment = Open Linux Share
    path = /home/lobo/Public
    read only = no
    guest ok = yes
    force create mode = 0755
    force user = lobo
    force group = lobo
```

### Test samba settings  
`testparm`
