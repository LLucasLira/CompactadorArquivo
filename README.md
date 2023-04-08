@echo off

echo Ola compactando arquivos

tar -cf Notas.zip *.xml 2> erros.txt

IF %ERRORLEVEL% NEQ 0 (echo "Erro na execução do script")
