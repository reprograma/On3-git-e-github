
# Git e Github :purple_heart:

1. [O que é Git](#git)
2. [O que é Github :octocat: ](#github)
3. [Instalação](#instalacao)
4. [Linhas de comandos básicos do terminal (usando git bash)](#bash)
5. [Começando com o Git](#git)


## O que é Git <a name="git"></a>

<a href="https://git-scm.com/book/pt-br/v2" target="_blank">Git</a> é um sistema de controle de versões distribuído, usado principalmente no desenvolvimento de software para registrar o histórico de edições dos arquivos.

Git, significa “pessoa desagradável” em inglês. O software foi desenvolvido por Linus Torvalds (criador do Linux). E é um software livre (open source).
<img src="./img-readme/">

Com o Git podemos desenvolver projetos colaborativos, com diversas pessoas trabalhando simultaneamente no mesmo código sem riscos de perdermos o que fizemos.

#### *Quem nunca salvou inúmeras versões de um arquivo?*

<img src="./_img-readme/files.png">


#### Como começar? :joy: :joy: :joy:

<img src="https://cdn-media-1.freecodecamp.org/images/1*0o9GZUzXiNnI4poEvxvy8g.png">

Tradução:

- Este é o *Git*. Ele rastreia o trabalho colaborativo em projetos através de um belo distribuído modelo de árvore da teoria dos grafos.

- Legal. Como usamos isso?

- Não tenho ideia. Apenas memorize esses comandos em shell e digite-os para sincronizar. Se você receber erros, salve seu trabalho em outro lugar, exclua o projeto e baixe uma nova cópia.

### Importância:

* ***Arquivos***: o Git guarda um histórico de tudo que foi alterado nos arquivos ao longo do tempo
* ***Quem***: o Git mostra quem foi o autor da mudança
* ***Mensagem***: o Git mostra a mensagem que o autor deixou referente às alterações.

---


## O que é Github :octocat: <a name="github"></a>


---

## Instalação do Git <a name="instalacao"></a>

- Baixar o Git pelo site: https://git-scm.com/downloads

 <img src="./img-readme/download-git.png">

- Instalar o arquivo `Git-2.24.0-32-bit.exe`

- Abrir o Git Bash


---


## Linhas de comando básicos do terminal (usando Git bash) <a name="bash"></a>
- Mostrar o caminho da pasta atual (***pwd***: *path working directory*)

	```
	pwd
	```

- Listar o que tem nessa pasta (***ls***: *list*)

	```
	ls
	```

- Criar uma pasta nova (***mkdir***: *make a directory*)

	```
	mkdir nova-pasta
	```

- Listar o conteúdo da pasta atual. (A pasta que acabou de ser criada deverá ser listada)

	```
	ls
	```

- Entrar na pasta nova.

	```
	cd nova-pasta
	```

- Criar um arquivo index.html pela linha de comando. O conteúdo será um texto "<html>" (***echo***)

	```
	echo "<html>" > index.html
	```

- Listar o conteúdo da pasta atual. (O novo arquivo deverá ser listado)

	```
	ls
	```

- Remover o arquivo `index.html`

	```
	rm index.html
	```

- Listar o conteúdo da pasta atual. (O novo arquivo deverá ter sido deletado)

	```
	ls
	```
	
- Voltar para a pasta acima. (***cd*** . .)

	```
	cd ..
	```

- Voltar para a pasta raiz do seu computador. (***cd***)

	```
	cd
	```

## Iniciando o controle de versão com o Git em um projeto existente na sua máquina <a name="git"></a>

### De: pasta local => Para: repositório remoto <a name="local-to-remote"></a>

#### O que vai acontecer por trás da linha de comando:

<img src="./img-readme/etapa1-git-status.png">

<img src="./img-readme/etapa2-git-add.png">

<img src="./img-readme/etapa3-git-commit.png">

<img src="./img-readme/etapa4-git-log.png">

**Etapas para rastreamento local**:

1. [Se identificar como autor(a) da mudança](#config)
2. [Iniciar o rastreamento dos arquivos desse projeto](#init)
3. [Adicionar arquivos na área de preparação (staging area)](#add)
4. [Definir mensagem que descreve as alterações realizadas (o que você desenvolveu)](#commit)

**Etapas para rastreamento remoto**:

5. [Criar um repositório novo no Github](#remote)
6. [Subir essas informações no repositório remoto do Github](#push)

---
1. **Se identificar como autor(a) da mudança** <a name="config"></a>

* Entrar na pasta do seu primeiro projeto ou a pasta de uma das aulas da Reprograma de semanas anteriores
* Clicar com o botão direito e abrir o Git bash selecionando ***Git Bash here***
 Listar o caminho local desta pasta

	```
	pwd
	```

* Configurar autoria. (Definição de quem vai assinar o compromisso pela mudança realizada)

	```
	git config --global user.name "Cintia Fumi"
	git config --global user.email "cintiafumi@gmail.com"
	```


* Verificar se suas informações de `user.name` e `user.email` foram configuradas com sucesso

	```
	git config --list
	```

---
2. **Rastrear os arquivos desse projeto** <a name="init"></a>

* Iniciar o rastreamento

	```
	git init
	```

* Listar os arquivos dessa pasta, incluindo os arquivos ocultos. E verificar se surgiu uma pasta oculta chamada .git na sua pasta atual

	```
	ls -a
	```

* Verificar o status dessa pasta

	<img src="./img-readme/etapa1-git-status.png">

	```
	git status
	```

---
3. **Adicionar arquivos na área de preparação (staging area)** <a name="add"></a>


* Adicionar o arquivo modificado. (Ex: `git add index.html`)

	```
	git add <nome do arquivo>
	```

*	Ou... Adicionar todos os arquivos
	```
	git add .
	```

* Os arquivos foram adicionados para a área de preparação (*staging area*)

	<img src="./img-readme/etapa2-git-add.png">

---
4. **Definir mensagem que descreve as alterações realizadas (o que você desenvolveu)** <a name="commit"></a>

* Adicionar a mensagem que informa o que o "compromisso" de alteração (git commit -m "Iniciando controle de versionamento do projeto inicial da Reprograma")

	<img src="./img-readme/etapa3-git-commit.png">

	*Obs: é uma boa prática escrever uma mensagem coerente e clara sobre a alteração realizada, pois você é a autora dessa alteração*
	
	<img src="https://vidadeprogramador.com.br/uploads/2017/07/tirinha1713.png">

* Verificar como ficou (***git log***)

	```
	git log
	```

	<img src="" >

		*Significa que plantamos a árvore*
	



---
5. **Criar um repositório novo no Github** <a name="remote><a>

* Após criado um no
---
### De: repositório remoto => Para: pasta local <a name="local-to-remote"></a>