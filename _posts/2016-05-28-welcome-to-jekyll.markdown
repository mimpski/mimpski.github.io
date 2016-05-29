---
layout: post
title:  Starting a Laravel project
description: A quick reference for starting a new Laravel project
date:   2016-05-27 20:24:13
categories: laravel reference
---

Most Laravel tutorials (and the documentation) covers how to set up your first instance of Laravel but misses out any information on creating more after that. This is a quick reference of the process to follow on a Mac using Homestead. 

CD into the /Code directory

```
laravel new ProjectName

homestead edit
```

Map the new folder and add the Database name to the list.

```
sudo nano /etc/hosts

homestead up

homestead provision

homestead ssh

  mysql -u homestead

  create database ProjectName;

  exit;

```

Edit ENV file with new database details

Test the connection details using SequelPro

Go to ProjectName.dev (or the url you set in the hosts file)

## Errors

If you get "input file not found", this will likely mean an error in your homestead.yaml. Double check that all data is aligned with spaces and NOT tabs. This does cause problems with the setup, you may need to reprovision homestead.

### Valet

Now that Valet is available, you could just rely on Homestead for the database connection. The set up would be similar to above, download laravel, create database then run valet.

CD into /Code

```
  laravel new ProjectName

  valet park
```

Go to ProjectName.dev
