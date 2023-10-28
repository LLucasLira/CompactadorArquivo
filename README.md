Este é um projeto simples que consiste em um script .bat para compactar arquivos.

@echo off
rem Com esse comando desabilitamos a exibição dos comandos no prompt do Windows relacionados ao conteúdo das instruções contidas no arquivo. - Alura

echo Ola compactando arquivos
rem exibimos uma mensagem para o usuário sobre a compactação. - Alura

tar -cf Notas.zip *.xml 2> erros.txt
rem Para lidar com arquivos compactados, usamos o comando tar. O próximo argumento, o Notas.zip, é o nome do arquivo *.xml. Com isso, todos os arquivos que terminam com a extensão .xml serão compactados. - Alura

IF %ERRORLEVEL% NEQ 0 (echo "Erro na execução do script")
rem condição representada pelo IF, indicando que se o conteúdo da variável ERRORLEVEL não for igual (NEQ, ou seja, Not EQual to) a zero, nós exibimos uma mensagem à pessoa informando que não foi possível encontrar os arquivos. - Alura
