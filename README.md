# RODBCpatch
On windows the behaviour of RODBC depends on wether you use it from RGui or not. In the former case if odbcConnect can not connect to the database you can choose the database in a dialogbox. It does not work if you do not use Rgui. This patch solves this problem. It modifies the RODBC.c file to use the desktopwindowhandle instead of the application's window handle. With this change you experience the same behavior on any interactive R session. Tested on Windows 7.

To use the code  simply source RODBC-patch.R with

`source("https://github.com/VilmosProkaj/RODBCpatch/raw/master/RODBC-patch.R")`

in the R console. At the end of the run you will be asked if you want to update your RODBC installation. 
