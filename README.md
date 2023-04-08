@echo off
(Com esse comando desabilitamos a exibição dos comandos no prompt do Windows relacionados ao conteúdo das instruções contidas no arquivo.) - Alura

echo Ola compactando arquivos
(exibimos uma mensagem para o usuário sobre a compactação.) - Alura

tar -cf Notas.zip *.xml 2> erros.txt
(Para lidar com arquivos compactados, usamos o comando tar.) - Alura
(O próximo argumento, o Notas.zip, é o nome do arquivo) - Alura
(*.xml. Com isso, todos os arquivos que terminam com a extensão .xml serão compactados.) - Alura

IF %ERRORLEVEL% NEQ 0 (echo "Erro na execução do script")
(condição representada pelo IF, indicando que se o conteúdo da variável ERRORLEVEL não for igual (NEQ, ou seja, Not EQual to) a zero, nós exibimos uma mensagem à pessoa informando que não foi possível encontrar os arquivos.) - Alura
