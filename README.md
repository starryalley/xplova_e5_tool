# Xplova E5 Tool

A convenient tool for Xplova E5 bike computer user to upload/convert XZR (their proprietary format) to GPX for uploading to other sport tracking sites. 

They should work fine for other Xplova computers recording XZR formats of activity.

## Notice

The conversion is made possible by [Xplova's website](http://tour.xplova.com/). You also need a valid account in that site for the conversion.

## Usage

```
$ python xplova_tool.py -h
usage: xplova_tool.py [-h] (-a ACTIVITY | -i IMPORT_FILE | -c) [-o EXPORT_GPX]
                      [-u USER] [-p PASSWD] [-v]

Auto uploader script for sport activity sites

optional arguments:
  -h, --help            show this help message and exit
  -a ACTIVITY, --activity ACTIVITY
                        activity_id to export to gpx file
  -i IMPORT_FILE, --import-file IMPORT_FILE
                        file to upload
  -c, --check-update    Check E5 update
  -o EXPORT_GPX, --export-gpx EXPORT_GPX
                        exported gpx filename
  -u USER, --user USER  Login username
  -p PASSWD, --passwd PASSWD
                        Login password
  -v, --version         show program's version number and exit
```


Convert XZR to GPX:

```
$ python xplova_tool.py -i ~/Downloads/065612.XZR -o test.gpx -u starryalley@gmail.com
Password:
Login successful! UserId: 2399, UserName: Mark Kuo
Uploading...
Upload successful!
Activity ID: 459538
GPX file successfully exported to test.gpx!
```


Check E5 software update:

```
$ python xplova_tool.py -c
Checking software update. Ignore other options...
Latest version: 1.2.0.03, Download link: http://tour.xplova.com/inc/downloadBin.php?binFile=XplovaE5SWUpdater_V1.2.0.03.exe&
```

# Dependencies

```pip install poster```
