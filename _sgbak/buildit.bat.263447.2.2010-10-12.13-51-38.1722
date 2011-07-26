@SETLOCAL

@REM Define the Workbench project root
set SYNPROJECTROOT=C:\Development\CodeExchange\BatchFileConversion\
set SYNBITSIZE=32

@REM Project open syn_set commands:
SET DEF=C:\Development\CodeExchange\BatchFileConversion\
SET SYNEXPDIR=C:\Development\CodeExchange\BatchFileConversion\
SET SYNIMPDIR=C:\Development\CodeExchange\BatchFileConversion\

@echo del C:\Development\CodeExchange\BatchFileConversion\SynPSG-doesNotExist-*.dbp
IF EXIST C:\Development\CodeExchange\BatchFileConversion\SynPSG-doesNotExist-*.dbp (
	del C:\Development\CodeExchange\BatchFileConversion\SynPSG-doesNotExist-*.dbp
)
@echo dblproto SYNPROJECTROOT:bat2script.dbl SYNPROJECTROOT:dbl2dibol.dbl SYNPROJECTROOT:dblibr2library.dbl SYNPROJECTROOT:dblink2link.dbl SYNPROJECTROOT:endOfToken.dbl SYNPROJECTROOT:stringCase.dbl SYNPROJECTROOT:stringReplace.dbl
dblproto SYNPROJECTROOT:bat2script.dbl SYNPROJECTROOT:dbl2dibol.dbl SYNPROJECTROOT:dblibr2library.dbl SYNPROJECTROOT:dblink2link.dbl SYNPROJECTROOT:endOfToken.dbl SYNPROJECTROOT:stringCase.dbl SYNPROJECTROOT:stringReplace.dbl
IF ERRORLEVEL 1 (exit /B ERRORLEVEL)
@echo Prototype complete

@echo dbl -d -qstrict -qalign -o bat2script SYNPROJECTROOT:bat2script.dbl SYNPROJECTROOT:dbl2dibol.dbl SYNPROJECTROOT:dblibr2library.dbl SYNPROJECTROOT:dblink2link.dbl SYNPROJECTROOT:endOfToken.dbl SYNPROJECTROOT:stringCase.dbl SYNPROJECTROOT:stringReplace.dbl
dbl -d -qstrict -qalign -o bat2script SYNPROJECTROOT:bat2script.dbl SYNPROJECTROOT:dbl2dibol.dbl SYNPROJECTROOT:dblibr2library.dbl SYNPROJECTROOT:dblink2link.dbl SYNPROJECTROOT:endOfToken.dbl SYNPROJECTROOT:stringCase.dbl SYNPROJECTROOT:stringReplace.dbl
IF ERRORLEVEL 1 (exit /B ERRORLEVEL)
@echo Compile complete

@echo Linking...
@echo dblink -d -o bat2script bat2script
dblink -d -o bat2script bat2script
IF ERRORLEVEL 1 (exit /B ERRORLEVEL)
@echo Link complete

@echo Build complete


@ENDLOCAL