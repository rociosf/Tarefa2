# TAREFA 2


# Instala Git en Windows

Descarga o instalador de Git para Windows https://git-scm.com/download/win 

Executa o instalador.

Segue as instruccións pinchando "NEXT" ata chegar a "FINISH" (o programa estaría instalado e listo para usar).


# Configuración de usuario en Git

Abre o símbolo de sitema.

Configura o teu nome de usuario e correo en Git.

```
git config --global user.email “sanchez.fernandez.rocio.ald@gmail.com"
```
```
git config --global user.name "Rocío SF"
```


# Crea un repositorio

Creamos un arquivo `hola.txt` e `git.txt` e inicializamos con `git init`.

Engadimos os arquivos ó repositorio con `git add  . ` (engade todo o que temos no directorio). 

Se temos archivos que non nos interesa engadir crearemos o arquivo `.gitignore`.

Primeiro commit. Executamos: `git commit -m "Primeiro commit"`

Co comando `git log --oneline --graph --decorate –all` podemos obter información do commit no que estamos a traballar, da rama na que estamos, etc...

Remote (remoto): establecemos a URL do repositorio (https://github.com/rociosf/Tarefa2). É necesario para facer git push. 
Usamos `git remote add origin https://github.com/rociosf/Tarefa2`

Agora nombramos a rama. Usamos `git branch -M main`

Facemos push con `git push -u origin main`


# Comandos: 
`git clone [url]` clona un repositorio remoto para tenerlo como local.


# PRACTICA:

`git diff` para ver a diferencia entre dúas orixes ou ramas.

`git show` para ver máis detalles sobre commits ou ramas.

`git annotate (ficheiro)` para ver quen fixo cambios.


# PRACTICA:

`git checkout` para desfacer cambios realizados. Para iso necesitamos especificar o arquivo que queremos voltar ó seu estado do repositorio con `git checkout -- (arquivo)` ou `git checkout -- . ` para tódolos da carpeta.

`git restore stage` para desfacer un git add ou facer `git restore (arquivo)` para desfacer os cambios que fixemos a un arquivo.

`git reset` borra cambios en diferentes partes. Ten 3 posibles formas:
    `--soft` reseteará os cambios no HEAD (commit).
    `--mixed` borrará o commit e o git add
    `--hard` borrará o commit, o git add e os cambios no repositorio local.


# PRACTICA:

`git branch (nome_branch)` crea unha rama nova.
     `git branch -av` listaxe de ramas.
     `git branch -d (nome_branch)` eliminará esa rama.

`git checkout (nome_branch)` cambiará a rama actual á nombrada.

`git merge (nombre_branch)` fusionará a rama especificada coa actual.


# Comprobar estado do repositorio.

`git status` mostra os estados dos arquivos, as súas modificacións e sen seguemento ademais dos que si teñen seguemento pero non están confirmados.
```
git status
```


# Historial de confirmacións.

`git log` úsase para mostrar a historia rexistrada alcanzable dun proxecto dende a máis recente ata a máis antiga.
Tamén se usa para mostrar as diferencias entre dúas ou máis ramas a nivel commit.

Xunto ó README.md engadimos unha imaxe poñendo un exemplo con `git log` 



# Creando ramas.

`git branch Nombre`.
```
git branch nome
```

Para poder traballar nesta rama necesitamos `git checkout nome` (así se cambia dunha rama a outra).
```
git checkout nome
```

# Facendo merge en ramas.

Ó facer merge en Git crea un commit "especial" que ten dous pais diferentes.
```
git merge nome
```

Consulta das ramas existestes con `git branch -av`.
```
git branch -av
```



# COMANDOS QUE NON SE MENCIONARON ANTERIORMENTE:

 `git config --global color.ui auto` Habilita o coloreado na saída dos comandos de Git na terminal.

`git config --list` Utilízase para ver a listaxe de todas as configuracións de Git que están en uso.

`git commit --amend -m "blablabla"` Úsase para facer cambios no commit máis recente.

`git remote remove origin` Elimina o vínculo entre o repositorio local e o repositorio remoto "origin".

`git clean -f` Elimina arquivos que non están sendo seguidos por Git e que non se atopan na staging área.

`git commit -a` Só crea commits cos cambios realizados que xa están sendo seguidos por git; non engade ficheiros novos.

`git log --graph --all --oneline` Mostra o historial de commits do repositorio nun formato atractivo e fácil de ler.

`git push github master` (é unha abreviatura que se pode usar para referirse a unha URL de GitHub específica que se configurase previamente). Envía os cambios realizados na rama `master` do repositorio local á rama `master` do repositorio remoto correspondente.

`git push origin master` (configurouse como "origin" ó clonar o repositorio local). Envía os cambios realizados na rama `master` do repositorio local á rama `master` do repositorio remoto correspondente.
