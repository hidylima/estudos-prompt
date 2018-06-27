# :books: Estudos Prompt Windows

1. ### Os primeiros comandos no prompt  

* ##### Por que aprender a usar o prompt de comando  
Muitas ferramentas no setor de desenvolvimento não possuem uma interface gráfica,  
pois elas devem funcionar em qualquer computador, inclusive nos computadores que  
não possuem essa interface, como por exemplo os computadores na nuvem.  

Outra razão, e talvez a mais importante, é que **as ferramentas na linha de comando  
podem ser controlados facilmente através de scripts, ou seja outras ferramentas.  
Isso é relacionado com a automação, ensinando as máquinas a fazerem vários passos  
automaticamente**, e bem mais rápido do que seria feito com o mouse em mãos.  

O Prompt também é chamado de cmd , terminal ou console. Todos estes são sinônimos  
nesse contexto.

Obs: O termo prompt se refere ao sinal `>`.  

* ##### Abrindo o prompt de comando  
Especificando `iniciar > cmd ou prompt` o prompt é aberto.  

A partir dessa tela, é possível interagir com o sistema operacional escrevendo  
comandos.  

* ##### A listagem inicial do caminho no prompt  
Ao abrir o prompt, ele automaticamente inicia-se na pasta pessoal do usuário. Antes  
do cursor, é exibido o caminho da pasta atual seguido pelo prompt (`>`).  

O `C:` é a partição principal do computador. O prompt sempre começa no `C:`, seguido  
pela a pasta Users e sua sub-pasta. A contra barra `\` é o sinal separador de diretórios  
na linha de comando.  

* ##### `/` - Utilizando a barra ao invés da contra barra  
A barra `/` é utilizada como separador e diretórios no mundo Unix, mas também funciona  
no mundo Windows.  
`cd diretorio/diretorioFilho`

* ##### `echo` - Imprimindo uma mensagem no terminal  
Esse comando irá exivbir uma mensagem no próprio prompt:  
`echo mensagem`  

* ##### `dir` - Listando arquivos e pastas  
Esse comando lista todos os arquivos e pastas do diretório atual.  

* ##### `dir ..` - Listando arquivos e pastas do diretório acima do atual

* ##### `dir /O:S` - Listando arquivos e pastas Ordenados por Tamanho (size)
Esse comando lista por tamanho todos os arquivos e pastas do diretório atual.  

* ##### `dir /O:D` - Listando arquivos e pastas Ordenados por Data
Esse comando lista por data todos os arquivos e pastas do diretório atual.  

* ##### `dir C:\` - Listando arquivos e pastas de outro diretório
Pelo comando dir é possível também mostrar o conteúdo de um diretório que não  
é o atual. O exemplo acima mostra o conteúdo do diretório `C:`.  

* ##### `dir /O:D C:\` - Listando arquivos e pastas de outro diretório Ordenados por Data
É possível também inverter a ordem dos parâmetros do comando dir para obter o mesmo  
resultado: `dir C:\ /O:D`.  

* ##### `cd` - Navegando entre diretórios  
CD é uma abreviação para 'Change Directory'.  
`cd nomeDaPasta`  

Também é possível definir o caminho:  
`cd C:\Documentos\workspaces`  

Para voltar ao diretório anterior, ou seja, subir na hierarquia de diretórios, ir uma  
pasta para cima, `cd ..`.  

* ##### `.` - Diretório atual  
O `.` se refere ao diretório atual, onde o prompt está atualmente.  

* ##### `..` - Diretório acima do atual  
O `..` se refere ao diretório acima do diretório atual na hierarquia.  

* ##### `mkdir` - Criando diretórios  
MKDIR é uma abreviação para 'Make Directory'.  
`mkdir nomeDaPastaAserCriada`  

* ##### `move` - Movendo um arquivo ou Diretório
`move nomeDoArquivoASerMovido.extensao NomeDaPasta`  

Para mover um arquivo para uma pasta acima, o comando  
`move nomeDoArquivoASerMovido.extensao ..` pode ser usado.  

* ##### Acessando o histórico de comandos  
Ao teclar seta para cima, o histórico de comandos do prompt pode ser acessado,  
evitando que o mesmo comando tenha que ser reescrito. Útil em caso onde é  
necessário especificar o mesmo comando ou uma pequena variação dele.  

* ##### `type` - Exibindo o conteúdo de um arquivo no prompt  
`type nomeDoArquivo.extensao`  

* ##### `echo` - Criando um arquivo já com um conteúdo inserido  
Com o comando `echo conteudoASerEscrito > nomeDoArquivo.extensao` é possível  
criar um novo arquivo já com algum conteúdo inserido dentro dele. Ou seja, toda  
a saída do comando `echo` nesse caso foi gravada no arquivo criado.  

Então o caractere `>` pega a saída de um comando e a grava no arquivo indicado  
(ou repassa para outro comando).  

* ##### `copy` - Copiando um arquivo  
`copy nomeDoArquivoASerCopiado.extensao nomeDoArquivoCopia.extensao`  

* ##### `rename` - Renomeando um arquivo ou Diretório
`rename nomeDoArquivoASerRenomeado.extensao nomeDoArquivoJaRenomeado.extensao`  

* ##### `del` - Deletando um arquivo  
`del nomeDoArquivoASerDeletado.extensao`  

* ##### `tab` - Autocomplete de arquivos ou pastas  
Para evitar escrever nomes extensos, ao pressionar a tecla `tab`, o prompt irá  
autocompletar o que está sendo escrito. A tecla pode ser pressionada várias vezes  
para que várias sugestões sejam exibidas.  

* ##### `cls` - Limpando o prompt  
Cls é uma abreviação para 'Clear Screen'.  

* ##### `rmdir` - Removendo diretórios vazios  
`rmdir nomeDoDiretorioVazio`

* ##### `help` - Exibindo a ajuda de um comando  
Cada comando possui uma pequena ajuda no terminal.  
`help type`

---

2. ### `>>` - Adicionando mais conteúdo a um arquivo

Vimos neste capítulo do treinamento que podemos criar um arquivo utilizando o sinal >, mas e se quisermos adicionar mais linhas a um arquivo de texto já existente, por exemplo para guardar o resultado de diversas execuções de um programa em um único arquivo?

Para isto existe o >>, quando colocamos o sinal de maior duas vezes o Prompt entende que só deve criar um arquivo novo quando o arquivo que pedimos não existir! Caso ele já exista, ele adiciona o novo conteúdo ao final do arquivo, sem sobrescreve-lo!

Veja só como funciona:

Digamos que primeiro criamos um novo arquivo de texto com o nosso conhecido comando echo :

`echo Ola mundo > arquivo.txt`

Ao abrirmos nosso arquivo.txt , vemos o texto que esperávamos:

`type arquivo.txt`

`//arquivo.txt`
Ola Mundo

Porém se agora desejarmos **adicionar um novo texto abaixo de "Ola Mundo"? Utilizamos o '>>'!**

Desta forma:

`echo Novos dados! >> arquivo.txt`

Quando abrimos nosso arquivo.txt, vemos que o texto foi adicionado corretamente:

`type arquivo.txt`

`//arquivo.txt`
Ola Mundo
Novos dados!

Utilizamos o **>>** quando queremos **adicionar um texto a um arquivo que já existe, sem sobrescreve-lo**. Se tentarmos utilizar o >> em um **arquivo que ainda não existe, ele terá o mesmo comportamento do >**, criando assim um arquivo novo e colocando o texto lá dentro.

---

3. ### `tree` - Mostrando pastas e subpastas organizadas em uma árvore

Vamos fazer mais um teste! No prompt digite o comando tree:

![tree](https://user-images.githubusercontent.com/29297788/38460810-00a42e52-3a98-11e8-9620-86297c06c011.png)

Dependendo do diretório atual podem aparecer muitas informações mas repare que o comando tree **mostra as pastas e subpastas organizadas em uma árvore**.

O tree pode ser **útil para entender a estrutura de um projeto**. Muitas vezes você precisa baixar um projeto na Alura para importar alguns arquivos iniciais. Com o comando tree você já pode ver facilmente como o projeto está organizado! Muito útil :)  

---

4. ### `more` - Exibindo página por página do arquivo no terminal  

O comando more funciona de um jeito semelhante ao comando type, com a diferença de exibir página por página do arquivo no terminal, em vez de mostra-lo todo de uma vez.

O seu uso é análogo ao comando type, podendo ser chamado assim:

`more arquivo.txt`

Ele exibirá uma página de cada vez do arquivo, sendo muito útil quando queremos exibir arquivos de texto com várias linhas para ir lendo lentamente, em vez de abri-lo todo no terminal de uma vez. Um exemplo disso é quando queremos ler os logs de uma aplicação que está em um servidor na nuvem, neste caso é preciso ler grandes arquivos de texto linha a linha, para identificar um bug ou realizar algum teste.

Agora que você já conhece o comando more e um exemplo prático de sua aplicação, vou lhe mostrar como controlar a exibição das páginas:

- Para passar de página em página, utilize a tecla espaço do seu teclado.
- Para passar de linha a linha, utilize a tecla enter do seu teclado.
- Para sair da exibição do comando, sem chegar ao final do arquivo utilize a tecla q do seu teclado.

Como você já sabe , sempre que quiser aprender mais sobre um comando, pode utilizar o help, então caso tenha a curiosidade de aprender ainda mais sobre o comando more, é só digitar help more no terminal!

---

5. ### Um novo prompt e executando scripts

No último capítulo vimos como usar o terminal/prompt e os comandos principais para lidar com arquivos e diretórios. Vimos comandos como dir, del ou cd. Vamos continuar usando o prompt, mas antes de aprender novos comandos, instalaremos uma versão um pouco mais amigável para nós, humanos. Há uma variação do terminal que se chama cmder, a qual deixa a linha de comando colorida e com algumas facilidades. Nada te impede de continuar com o terminal antigo, no entanto vamos instalar o cmder para melhorar a visualização dos comandos.

* ##### Instalando o [cmder](http://cmder.net)
Para instalar o cmder devemos primeiro baixar o ZIP no site: http://cmder.net

Para abrir o novo terminal do Cmder basta entrar na pasta do cmder e dar um duplo-clique no executável, ou digitar windows>cmder:

![image](https://user-images.githubusercontent.com/29297788/38461182-14fe744a-3aa0-11e8-8483-a2ec04641159.png)

Isso faz com que abra um novo terminal, e veja que já está colorido! A diferença é sutil, mas vai nos ajudar mais para frente.  

* ##### Sobre o Git
Para saber mais sobre Git: Aqui usaremos a versão mínima do cmder mas para quem está interessado em usar o GIT já pode baixar a versão full também. O Git é um sistema de versão para código fonte. Ele ajuda gerenciar esse código fonte. Isso significa, sincronizar o trabalho de vários desenvolvedores no mesmo projeto. O Git mantém um histórico das alterações e cria automaticamente backups. Na Alura temos um treinamento focado nessa ferramenta poderosa: https://www.alura.com.br/course/PM-89

* ##### `ctrl+t` - Abrindo abas diferentes no terminal
É um sistema parecido com abas do browser. Posso alternar entre elas com o `ctrl+tab`. Ou seja, posso trabalhar em dois projetos diferentes, usando várias instâncias do prompt.  

![image](https://user-images.githubusercontent.com/29297788/38461252-649e7f6c-3aa1-11e8-9206-193f6b4948bd.png)

* ##### Meu primeiro script
Uma das motivações para aprender os comandos no terminal é a automação de tarefas, isto é, fazer várias coisas repetitivas mais facilmente. Uma das tarefas de um desenvolvedor é criar um backup de arquivos. Vamos, então, criar um pequeno script para "backupear" os arquivos. Tudo executado na linha de comando, ok?

Os scripts no mundo Windows não são nada mais do que arquivos de texto com a extensão bat. bat significa batch, em português "lote". Ou seja, com esse script é possível executar vários comandos em lote (uma lista de comandos).

Vamos criar um arquivo bat, na linha de comando:

`echo cls > backup.bat`

Repare que o comando não foi executado ainda, gravamos apenas o comando cls no arquivo script.bat.

![04-criacao-script](https://user-images.githubusercontent.com/29297788/38461279-1c4e0466-3aa2-11e8-82b2-fd1c3d1d349c.png)

E como posso executar o script? Basta digitar:

`backup.bat`

O script foi chamado e todos os comandos dentro dele foram executados sequencialmente! Como resultado, a tela está limpa! Fantástico :)

* ##### Processamento em lote
O arquivo tem a extensão .bat (batch, lote) não por acaso, pois podemos executar mais que um comando em sequência. Vamos abrir o arquivo limpatela.bat em um editor de texto. Vou usar um bem simples.

Já que podemos executar qualquer comando, adicionaremos depois do cls um echo informando que a tela foi limpa e depois perguntar se ele realmente quer continuar:

```
cls
echo tela limpa!
echo Realmente quer fazer backup?
```

E para parar a execução podemos adicionar o comando pause:

```
cls
echo Realmente quer fazer backup?
pause
```

![05-script-notepad](https://user-images.githubusercontent.com/29297788/38461371-3792f27a-3aa4-11e8-8199-692fb27ccadf.png)

O comando pause faz com que o usuário do script precise confirmar a continuação da execução do script. Vamos testar uma vez para deixar mais claro:

![06-executar-script](https://user-images.githubusercontent.com/29297788/38461376-43362ec6-3aa4-11e8-917f-b3c7f0bff420.png)

Isto nos permite dar a opção do usuário abortar a execução do script caso ele não deseje continuar, através do atalho `CTRL + C` ou simplesmente fechando o terminal.

Ótimo, já é um bom início. Agora vamos limpar a tela com cls, adicionar uma mensagem para o usuário saber que vamos iniciar o backup e preparar a pasta do backup através do script, indo para a pasta home do nosso usuário e criando o diretório de backup:

```
cls
echo Realmente quer fazer backup?
pause

cls
echo ok, fazendo backup...
cd C:\Users\caelum
mkdir backup
```

Todos esses comandos já conhecemos e agora podemos copiar os arquivos da pasta codigo para a pasta backup. O problema ainda é que o comando copy é muito simples e não consegue copiar pastas e sub-pastas. Ainda bem que existe o irmão gêmeo dele, o xcopy. O xcopy copia pastas e sub-pastas desde que usamos os parâmetros /E (para copiar subpastas) e /Y (para confirmar automaticamente a sobrescrita de arquivos). Sabendo disso podemos escrever:

```
cls
echo Realmente quer fazer backup?
pause

cls
echo ok, fazendo backup...
cd C:\Users\caelum
mkdir backup

xcopy /E /Y "C:\Users\caelum\codigo"  "C:\Users\caelum\backup"
```

Assim, todo o conteúdo de uma pasta será copiado para a outra.

Agora no fim do script podemos listar os arquivo da pasta backup:

```
cls
echo Realmente quer fazer backup?
pause

cls
echo ok, fazendo backup...
cd C:\Users\caelum
mkdir backup

xcopy /E /Y "C:\Users\caelum\codigo" "C:\Users\caelum\backup"  

echo Listando os arquivos do backup
dir C:\Users\caelum\backup
```

Pronto! Agora nosso script realiza o backup da pasta codigo como desejávamos!

Repare que o script é nada mais de um conjunto de comandos pequenos para realizar uma tarefa maior.

---
