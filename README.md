# Content

This repository contains a full **anonymized backup** of all data stored in our running application at [http://db.freebim.at](http://db.freebim.at)

1. download the backup data from [https://github.com/asi-propertyserver/content](https://github.com/asi-propertyserver/content)
2. put the backup into your configured `freebim.backup.dir` - directory.

```
/etc/asi-propertyserver/backup
└── 20190330_085328
    ├── nodes
    └── relationships
```
3. log in as `admin` 
4. press the 'restore backup' button
5. wait and watch the server logs. After `restoreBackup` has finished you have to reload the app in the browser.

```
...
2019-03-31 09:12:01,844  INFO SpectroomBackupServiceImpl:241 - restore relationships finished.
2019-03-31 09:12:01,844  INFO SpectroomBackupServiceImpl:243 - restoreBackup finished.
...
```

Since this is a full backup restore these steps will also **override** your configured `admin` and `guest` user settings.  
The login-data used in the backup are:

| Username    | Password       |
|:------------|:---------------|
| `admin`     | `password`     |

**Don't forget to change the password** of `admin` afterwards.

