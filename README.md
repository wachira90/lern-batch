# lern-batch
lerning batch script

## nano moveauditlog.bat

````
@ECHO OFF
if EXIST F:\ (
    ECHO RUN SCRIPT
    PUSHD F:\AUDITLOG\
    FORFILES /M *.sqlaudit /D -1 /C "cmd /C if @isdir==FALSE move @file D:\AUDITLOG\"
    POPD
) else (
    ECHO NOT EXIST DRIVE
)
````

## move file older than 30 day 

````
PUSHD \\folder1
FORFILES /M *.doc /D -30 /C "cmd /C if @isdir==FALSE move @file .\archive\"
FORFILES /M *.xls /D -30 /C "cmd /C if @isdir==FALSE move @file .\archive\"
POPD
````

## date

````
C:\scriptbackup>echo %DATE% %TIME%
2023-02-22 12:55:15.68

C:\scriptbackup>
````
