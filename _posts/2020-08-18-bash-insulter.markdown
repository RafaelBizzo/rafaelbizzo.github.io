---
categories: Linux Bash
date:   2020-08-18 21:03:36 +0530
title:  "Bash Inuslter, ser humilhado pelo próprio terminal apenas por digitar um comando errado"
layout: post
---

#  Oque é

Bash Insulter é um script criado por [hkbakke](https://github.com/hkbakke) e está disponível em seu Github sobre a licença MIT, seu objetivo é retornar uma mensagem no terminal toda vez que o usuário digitar um comando inválido. Tomei a liberdade de traduzi-lo para quem não tem tempo para tal, ou simplesmente não gosta de inglês.

![Exemplo](https://raw.githubusercontent.com/RafaelBizzo/rafaelbizzo.github.io/master/images/bash%20insulter/bash-insulter-insults-the-user-when-typing-wrong-command-1.png)

# Instalação

Para instalar o Bash Inuslter primeiro precisamos clonar o repositório, no caso vamos clonar do [meu Github](https://github.com/RafaelBizzo) com o projeto traduzido.

```bash
git clone https://github.com/RafaelBizzo/bash-insulter.git
```

Copiamos o arquivo que contém as falas para `/etc`

```bash
sudo cp bash-insulter/src/bash.command-not-found /etc/
```

Para finalizar adicionamos o seguinte script em `/etc/bash.bashrc`  utilizando seu editor de preferência: 

```bash
if [ -f /etc/bash.command-not-found ]; then
    . /etc/bash.command-not-found
fi
```

Feche e abra o terminal e veja a mágica acontecer.

# Links

[Meu repositório](https://github.com/RafaelBizzo/bash-insulter)

[Repositório original](https://github.com/hkbakke/bash-insulter)

