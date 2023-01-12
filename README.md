---
description: description
---

# README

![GitHub language count](https://img.shields.io/github/languages/count/pedrorenan/electron-docker-dev-env) ![Repository size](https://img.shields.io/github/repo-size/pedrorenan/electron-docker-dev-env) [![Siga no Twitter](https://img.shields.io/twitter/url?url=https://github.com/pedrorenan/electron-docker-dev-env) ](https://www.twitter.com/pedrorenan/)[![GitHub last commit](https://img.shields.io/github/last-commit/pedrorenan/electron-docker-dev-env) ](https://github.com/tgmarinho/README-ecoleta/commits/master)![License](https://img.shields.io/badge/license-MIT-brightgreen) [![Stargazers](https://img.shields.io/github/stars/pedrorenan/electron-docker-dev-env?style=social)](https://github.com/pedrorenan/electron-docker-dev-env/stargazers)

* [🇧🇷🇵🇹 Português](./#-português)
* [🌎 English](./#-english)

## 🇧🇷🇵🇹 Português

#### Modelo para Ambiente de Desenvolvimento Electron com Docker.

Tabela de conteúdos

\=================

* [Sobre o projeto](./#-sobre-o-projeto)
* [Funcionalidades](./#-funcionalidades)
* [Como executar o projeto](./#-como-executar-o-projeto)
* [Pré-requisitos](./#pré-requisitos)
* [Como contribuir no projeto](./#-como-contribuir-no-projeto)
* [Autor](./#-autor)
* [Licença](./#-licença)

### 💻 Sobre o projeto

A motivação desse projeto é conseguir desenvolver usando Electron independente o sistema operacional. [Você pode ler mais sobre essa motivação aqui](https://medium.com/@pedrorenan/em-busca-da-independ%C3%AAncia-para-o-ambiente-de-desenvolvimento-2adc22f6f250).

***

### ⚙️ Funcionalidades

Gera um ambiente de desenvolvimento Electron com Docker que permite empacotar e exportar o aplicativo.

***

### 🚀 Como executar o projeto

#### Pré-requisitos

* [Docker](https://www.docker.com/get-started)
* [VSCode](https://code.visualstudio.com/download)
* Extensão [Remote-Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

**macOS**

* [Homebrew](https://brew.sh/)
* XQuartz

```bash
# Instale o XQuartz
$ brew cask install xquartz
```

abra o XQuartz, navegue até _Preferences -> Security_ e deixe as duas opções marcadas.

![XQuartz Prefereces Security](assets/xquartz\_preferences.png)

***

Instruções:

É recomendável que você clique em _Use this template_, dessa maneira você já poderá criar o repositório com o nome do seu projeto e iniciar o desenvolvimento. Faça o clone dele no seu computador e siga as demais instruções.

**macOS**

```bash
# Obtenha seu ip
$ ip=$(ifconfig en0 | grep inet | awk '$1=="inet" {print $2}')

# Adicione esse ip na lista dos permitidos para conectar no servidor X
$ xhost + ip

# Acesse a pasta do projeto no terminal/cmd
$ cd [your-repository-name]

# Descomente a linha remoteEnv 
$ sed 's+//\"remoteEnv+\"remoteEnv+g' .devcontainer/devcontainer.json

# Substitua HOST_IP pelo ip obtido
$ sed -i '' -e 's+HOST_IP+'$ip'+g' .devcontainer/devcontainer.json

```

**Todos os SOs**

```bash
# Abra o projeto com o VSCode
$ code .
```

Quando o [VSCode](https://code.visualstudio.com/download) abrir você verá uma mensagem informando que foram detectadas as configurações necessárias para que a extensão [Remote-Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) faça a mágica acontecer.

![Remote Containers Dialog](assets/remote-containers-dialog.png)

Clique em "Reopen in Container". O [VSCode](https://code.visualstudio.com/download) vai reiniciar e é só aguardar o ambiente ficar pronto para você. Pode demorar um pouco na primeira vez se você nunca tiver feito o download dos containers necessários 🕐. Mas vale a pena!

Quando finalizar, você terá um terminal dentro do [VSCode](https://code.visualstudio.com/download) que já está dentro do container. Tudo integrado! Tipo [Inception](https://www.imdb.com/title/tt1375666/) mesmo 🍿.

💡 Tudo que você executar nesse terminal será executado dentro do container apenas!

```bash
# Inicie o projeto
$ npm start
```

![Running the project](assets/electron\_npm\_start\_macos.png)

> 🚀 Tente Editar o arquivo index.html para ver o _hot reloading_ em ação.

> 💡 Usuários de macOS sempre devem estar com o xQuartz aberto e com o ip local na lista de permitidos.

Para empacotar e exportar o aplicativo:

**macOS**

```bash
# Empacotar e exportar o aplicativo
$ npm run make-macos
```

**Todos os SOs**

```bash
# Empacotar e exportar o aplicativo
$ npm run make
```

> ✅ Os arquivos exportados serão gerados pasta _out/make/\[formato]_

### 💪 Como contribuir no projeto

1. Faça um **fork** do projeto.
2. Crie uma nova branch com as suas alterações: `git checkout -b my-feature`
3. Salve as alterações e crie uma mensagem de commit contando o que você fez: `git commit -m "feature: My new feature"`
4. Envie as suas alterações: `git push origin my-feature`

> Caso tenha alguma dúvida confira este [guia de como contribuir no GitHub](CONTRIBUTING.md)

***

### 🦸 Autor

[![Twitter Badge](https://img.shields.io/badge/-@pedrorenan-1ca0f1?style=flat-square\&labelColor=1ca0f1\&logo=twitter\&logoColor=white\&link=https://twitter.com/pedrorenan)](https://twitter.com/pedrorenan) [![Linkedin Badge](https://img.shields.io/badge/-Pedro%20Renan-blue?style=flat-square\&logo=Linkedin\&logoColor=white\&link=https://www.linkedin.com/in/opedrorenan/)](https://www.linkedin.com/in/opedrorenan/) [![Gmail Badge](https://img.shields.io/badge/-pedrorenan@gmail.com-c14438?style=flat-square\&logo=Gmail\&logoColor=white\&link=mailto:pedrorenan@gmail.com)](mailto:pedrorenan@gmail.com)

***

### 📝 Licença

Este projeto esta sobe a licença [MIT](LICENSE/).

Feito com ❤️ por Pedro Renan 👋🏽 [Entre em contato!](https://www.linkedin.com/in/opedrorenan/)

***

## 🌎 English

#### Electron Docker Development Environment Template

Table of content

\=================

* [About](./#-about)
* [Features](./#-features)
* [How it works](./#-how-it-works)
* [Prerequisites](./#prerequisites)
* [How to contribute](./#-how-to-contribute)
* [Author](./#-author)
* [License](./#-license)

### 💻 About

***

### ⚙️ Features

***

### 🚀 How it works

#### Prerequisites

When [VSCode](https://code.visualstudio.com/download) opens, you will see a message stating that the necessary settings have been detected for the [Remote-Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension to make the magic happen.

![Remote Containers Dialog](assets/remote-containers-dialog.png)

Click on “Reopen in Container”. The [VSCode](https://code.visualstudio.com/download) will restart. Just wait for the environment to get ready for you. It may take a while during the first time, specially if you have never downloaded the necessary containers 🕐. But it's worth it!

Once done, you will have a terminal inside the [VSCode](https://code.visualstudio.com/download) that is already inside the container. Everything integrated! Like [Inception](https://www.imdb.com/title/tt1375666/) 🍿.

💡 Everything you do in this terminal will be done only inside the container!

### 💪 How to contribute

1. Fork the project.
2. Create a new branch with your changes: `git checkout -b my-feature`
3. Save your changes and create a commit message telling you what you did: `git commit -m" feature: My new feature "`
4. Submit your changes: `git push origin my-feature`

> If you have any questions check this [guide on how to contribute](CONTRIBUTING.md)

***

### 🦸 Author

[![Twitter Badge](https://img.shields.io/badge/-@pedrorenan-1ca0f1?style=flat-square\&labelColor=1ca0f1\&logo=twitter\&logoColor=white\&link=https://twitter.com/pedrorenan)](https://twitter.com/pedrorenan) [![Linkedin Badge](https://img.shields.io/badge/-Pedro%20Renan-blue?style=flat-square\&logo=Linkedin\&logoColor=white\&link=https://www.linkedin.com/in/opedrorenan/)](https://www.linkedin.com/in/opedrorenan/) [![Gmail Badge](https://img.shields.io/badge/-pedrorenan@gmail.com-c14438?style=flat-square\&logo=Gmail\&logoColor=white\&link=mailto:pedrorenan@gmail.com)](mailto:pedrorenan@gmail.com)

***

### 📝 License

This project is under the license [MIT](LICENSE/).

Made with ❤️ by Pedro Renan 👋🏽 [Get in Touch!](https://www.linkedin.com/in/opedrorenan/)

***

check this https://dev.to/darksmile92/run-gui-app-in-linux-docker-container-on-windows-host-4kde
