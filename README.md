# lern-batch
lerning batch script

## nano movelog.bat

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
