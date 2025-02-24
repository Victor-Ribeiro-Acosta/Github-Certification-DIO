# <center>**Comandos Git para iniciantes**</center><br><br>

## **git init**<br>

<span style = "font-size:18px">Esse comando é o maís básico, ele permite iniciar um repositório git dentro da pasta na qual estamos trabalhando. Quando vamos usar o git no projeto local, iniciamos assim: </span>
<br><br>

```
    $git init
```
<br><br>
<img src = gifs/git_init.gif width = 600> <br>

## **git remote** <br>

<span style = "font-size:18px">Esse é o comando que nos permite conectar nosso repositório local a um repositório remoto, para realizarmos esse processo no github, primeiro precisaremos da url do repositório, obtida da seguinte forma:</span><br><br>

<img src = gifs/copia_repositorio.gif width = 600> <br><br>

<span style = "font-size:18px">O primeiro comando que usamos é o seguinte:</span> <br><br>

```
    $git remote add origin 
```
<br><br>
<img src = gifs/git_remote.gif width = 600> <br><br>

<span style = "font-size:18px">Assim que executarmos, o git vai criar um origin, onde a url do nosso repositório ficará registrada, sempre que precisarmos puxar alguma alteração ou enviar uma alteração para o github, usaremos o origin.</span> <br><br>

```
    $git remote -v
```
<br><br>
<span style = "font-size:18px">Esse outro comando nos retorna o repositório registrado na origin, muito útil quando não sabemos em qual repositorio nosso projeto está conectado.</span> <br><br>

<img src = gifs/git_remote_v.gif width = 600> <br><br>

## **git add** <br>

<span style = "font-size:18px">Quando realizamos alguma alteração no repositório local, essas não serão salvas no repositório remoto, isso quer dizer que, se alguma coisa ocorrer, há um grande risco de que todo o trabalho seja perdido. Para evitar contratempos, usamos o add para adicionar as modificações ao commit.</span> <br><br>

```
    $git add arquivo
```
<br><br>
<span style = "font-size:18px">Esse comando guarda apenas um arquivo em específico.</span> <br><br>

```
    $git add .
```
<br><br>
<span style = "font-size:18px">Esse é o comando usado quando pretende-se guardar todas as alterações feitas no projeto</span> <br><br>

<img src = gifs/git_add.gif width = 600> <br><br>

## **git status** <br>

<span style = "font-size:18px">Esse comando mostra todas as informações da branch na qual estamos trabalhando, assim, podemos ver:
    - Qual a branch em que estamos
    - Quais modificações foram feitas
    - Se falta alguma operação do git (como o add, commit ou push)</span> <br><br>

<img src = gifs/git_status.gif width = 600> <br><br>

## **git commit** <br>

<span style = "font-size:18px">Após usarmos o add, ainda não está garantido que nossas alterações tenham sido salvas, para isso usamos o commit, ele serve como um ponto de verificação ao qual podemos retornar. Fazendo uma analogia, no momento que definimos um commit seria como iniciar uma nova fase em um jogo de videogame, se você perder o duelo, você voltará para o começo da fase e não do jogo, com o commit, podemos definir pontos dentro do nosso trabalho aos quais podemos retornar quando ocorrer algum problema.</span> <br><br>

```
    $git commit -m "mensagem"
```
<br><br>
<img src = gifs/git_commit.gif width = 600> <br><br>

<span style = "font-size:18px">Após realizarmos o commit, o git status não mostrará mais nenhuma alteração, pois, essas já foram salvas no commit.</span> <br><br>

<img src = gifs/git_status_commit.gif width = 600> <br><br>

## **git branch** <br>

<span style = "font-size:18px">As branches são ramificações que permitem diversos desenvolvedores trabalharem no mesmo projeto sem gerar conflitos.
o git branch permite uma série de funções, desde de criar, visualizar e excluir branches.</span> <br>

```
    $git branch main
```
<br><br>
<span style = "font-size:18px">O comando acima criará uma branch main, padrão para o github.</span> <br><br>


```
    $git branch -M main
```
<br><br>
<span style = "font-size:18px">Esse comando vai renomear a branch master para main, que é a branch criada por padrão no github.</span> <br><br>
<img src = gifs/git_branch.gif width = 600> <br><br>

```
    $git branch
    $git branch --list
```
<br><br>
<span style = "font-size:18px">Ambos os comandos permitem visualizar as branches criadas.</span> <br><br>

```
git brnach -d main
```
<br><br>
<span style = "font-size:18px">Esse comando deleta uma branch.</span> <br><br>


## **git push** <br>

<span style = "font-size:18px">Após configurar a branch e fazer o commit, é hora de enviar as alterações salvas no commit para o repositório, para isso, usamos o comando push.</span> <br><br>

```
    $git push -u origin main
```
<br><br>
<span style = "font-size:18px">Todas as alterações comitadas na branch main serão enviadas ao repositorio salvo em origin (no nosso caso, é o github).</span> <br><br>

<img src = gifs/git_push.gif width = 600> <br><br>

## **git pull** <br>
<span style = "font-size:18px">Quando trabalahmos de maneira colaborativa, é comum que outras pessoas enviem suas alterações no projeto também, porém, isso pode gerar conflitos, pois, seu projeto local não estará com as atualizações feitas, para buscar as atualizações e impedir conflitos, você deve usar o git pull, que trará as modificações diretamente do repositorio remoto para o reositório local.</span> <br><br>

```
    $git pull origin
```
<br><br>
<img src = gifs/git_pull.gif width = 600> <br><br>

## **Git clone** <br>

<span style = "font-size:18px">Esse comando permite fazer uma cópia de um projeto em um repositório remoto para o repositório local (sua máquina), ele, basicamente, funciona como um ctrl + C e ctrl + V do git.
Para fazer uma cópia do projeto do github, usa-se o seguinte comando:</span> <br><br>
```
    $git colne link_repositorio
```
<br><br>

<img src = gifs/git_clone.gif width = 600> <br>