<p align="center">
  <img src="img/kibo.png" alt="Kibo" width="96">
</p>

<h1 align="center">Kibo</h1>

<p align="center">
  <b>Muitos agentes de IA. Um só lugar.</b><br>
  Seus agentes do Claude Code trabalhando ao mesmo tempo, como uma equipe, com o console, os arquivos e as tarefas à vista.
</p>

<p align="center">
  <a href="https://github.com/nexsoftgroup/kibo/releases/latest/download/Kibo-Setup.exe"><img src="https://img.shields.io/badge/Baixar_para_Windows-%C3%BAltima_vers%C3%A3o_%28.exe%29-3346e0?style=for-the-badge" alt="Baixar a última versão do Kibo para Windows (.exe)"></a>
  <a href="https://kibo.nexsoftgroup.com"><img src="https://img.shields.io/badge/Site-kibo.nexsoftgroup.com-0f2340?style=for-the-badge" alt="Site: kibo.nexsoftgroup.com"></a>
</p>

<p align="center">
  <a href="https://github.com/nexsoftgroup/kibo/releases/latest"><b>Baixar</b></a> ·
  <a href="docs/README.md">Documentação</a> (em espanhol) ·
  <a href="https://github.com/nexsoftgroup/kibo/releases">Versões e novidades</a> ·
  <a href="https://github.com/nexsoftgroup/kibo/issues/new/choose">Relatar um problema ou sugerir uma ideia</a>
</p>

<p align="center">
  Grátis · 100% local · Sem telemetria · Não lê suas credenciais · Beta
</p>

<p align="center">
  <a href="README.md">Español</a> · <a href="README.en.md">English</a> · <b>Português (Brasil)</b>
</p>

![O Kibo com quatro sessões do Claude Code trabalhando ao mesmo tempo, e o cartão de uma equipe do Agent Hub](img/portada.png)

> **Este repositório é a casa pública do Kibo:** um resumo, as novidades e o lugar para deixar seus comentários.
> A **[documentação completa](docs/README.md)**, com todas as capturas de tela, está neste repositório (por enquanto em
> espanhol), e cada versão com suas novidades, em **[Releases](https://github.com/nexsoftgroup/kibo/releases)**.
> O código-fonte não é publicado aqui. O app em si fala português (Brasil), espanhol e inglês.

---

## O que é o Kibo

Os agentes de IA já escrevem código, pesquisam e documentam. O difícil é coordená-los. O Kibo é um app de desktop que
transforma sessões soltas do **Claude Code** em **uma equipe que trabalha junta**, à vista e no seu computador.

- **Uma equipe, não abas soltas.** Cada projeto tem sua MAIN, que distribui o trabalho entre os agentes e responde a
  você de forma curta. Você fala com a equipe; não precisa ir sessão por sessão.
- **Muitos agentes, à vista.** Enquanto um escreve o código, outro roda os testes e outro documenta. Você vê se cada um
  está trabalhando, esperando por você ou pedindo permissão.
- **Nada se perde.** Cada conversa, captura de tela e decisão fica no seu computador, e uma Wiki que se escreve sozinha
  faz o próximo agente começar sabendo o que o anterior descobriu.

## O que ele faz

### Agent Hub: suas equipes de agentes num relance

![Agent Hub: um cartão por equipe, o mapa de equipes e o chat da equipe](img/agent-hub.png)

- **Um cartão por equipe:** cada projeto com sua MAIN, seus agentes e quantos estão trabalhando ou esperando por você.
- **O chat da equipe:** você fala com todos, com um agente ou com várias equipes, com **Ordenar** ou **Consultar**.
- **As permissões continuam sendo aprovadas por você.**

### Muitos agentes, todos ao mesmo tempo

![Uma grade 2 × 2 com quatro sessões do Claude Code ao mesmo tempo](img/cuadricula.png)

- Várias sessões do Claude Code na mesma tela, cada uma na sua tarefa.
- Você divide a área como precisar (2 colunas, 2 linhas, 2 × 2, 3 × 2) ou arrasta uma aba até uma borda.
- Cada sessão é o Claude Code de verdade, com sua conta e as permissões de sempre.

### O histórico da conversa e uma Wiki que se escreve sozinha

![A conversa da sessão, cada mensagem com seu horário, ao lado do console](img/conversacion.png)

- **Volte ao que foi dito por data** («o que conversamos ontem entre 14h e 18h») e o agente se situa.
- **Uma Wiki por projeto**, em Markdown: o que os agentes descobrem fica em notas, separando o que está confirmado do
  que falta verificar. Dá para ler no Kibo, em qualquer editor ou no Obsidian.
- **Ctrl+K** busca em projetos, agentes, tarefas e em tudo o que foi conversado.

### Tarefas agendadas: o trabalho continua mesmo sem você

![O painel de tarefas agendadas e o formulário para agendar uma](img/tareas.png)

- No horário que você escolher, o Kibo abre a sessão e **digita a instrução**, como se fosse você.
- Funciona mesmo com o Kibo fechado: Agendador de Tarefas do Windows, systemd ou cron no Linux, e launchd no macOS.

### E também

| | |
|---|---|
| **Aponte na web** | Com a extensão para Chrome e Edge, você marca um elemento ou uma área, e a sessão recebe a captura, o HTML e os erros do console. |
| **Capturas na hora** | Cole ou arraste uma captura de tela, marque com setas e caixas, e ela chega ao agente. |
| **Editor e VS Code** | Os arquivos do projeto com o editor do VS Code, e o VS Code completo numa aba, se quiser. |
| **Atalhos para tudo** | Numa janela própria (Ctrl+Alt+S), com busca. |
| **Servidores por SSH** | Sessões que rodam em outra máquina. Só com chave SSH: senhas nunca são guardadas. |
| **Temas e idiomas** | Kibo, Escuro e Claro. Em português (Brasil), espanhol e inglês. |
| **Avisos na área de trabalho** | Opcionais: quando um agente termina ou precisa de você. |

👉 **[Todas as funções, com capturas de tela](docs/funciones.md)** (em espanhol)

## Instalar

O Kibo é instalado para o seu usuário, dentro do seu perfil. Tudo vem de
[Releases](https://github.com/nexsoftgroup/kibo/releases/latest): o instalador de clique duplo e o que os comandos do terminal usam. O
instalador fala português, espanhol ou inglês, conforme o idioma do sistema.

### Windows

**Recomendado: pelo terminal, numa linha.** Abra o PowerShell (tecla Windows, digite «PowerShell» e Enter), cole isto e
aperte Enter:

```powershell
irm https://github.com/nexsoftgroup/kibo/releases/latest/download/install.ps1 | iex
```

**O que vai acontecer:** ele pergunta com qual IA você vai trabalhar, pede permissão antes de instalar cada coisa que
faltar, baixa o Kibo do GitHub, **confere a assinatura da NexSoft e o SHA-256** e abre o instalador. Assim o aviso do Windows não
aparece. O instalador mostra os [Termos de uso](https://kibo.nexsoftgroup.com/terminos#pt-BR) antes de instalar.

**Prefere o instalador de clique duplo?**

[![Baixar a última versão do Kibo para Windows (.exe)](https://img.shields.io/badge/Baixar-Kibo--Setup.exe_%28%C3%BAltima_vers%C3%A3o%29-3346e0?style=for-the-badge)](https://github.com/nexsoftgroup/kibo/releases/latest/download/Kibo-Setup.exe)

Ele baixa sempre a última versão. O número, as novidades e o SHA-256 estão em
[Releases](https://github.com/nexsoftgroup/kibo/releases/latest). O Windows vai mostrar um aviso porque ele ainda não
está assinado: **Mais informações → Executar assim mesmo**.

### Linux e macOS

Abra um terminal, cole isto e aperte Enter:

```sh
curl -fsSL https://github.com/nexsoftgroup/kibo/releases/latest/download/install.sh | sh
```

Ele faz as mesmas perguntas, baixa o Kibo do GitHub, confere a assinatura e o SHA-256 e instala para o seu usuário em `~/Kibo/kibo`, sem
`sudo`. No macOS é **experimental**: o código está escrito, mas ainda não foi testado num Mac de verdade. Se você
testar, vai nos ajudar saber como foi.

### O que você precisa

| Sistema | Estado | Precisa de |
|---|---|---|
| **Windows 10 / 11** (64 bits) | Suportado | WebView2 (vem com o Windows; se faltar, o instalador baixa), Git for Windows (o Claude Code precisa dele) e o Claude Code. Não precisa de Python: o instalador já traz. O comando do terminal instala o que faltar, se você autorizar. |
| **Linux** | Testado no Ubuntu 24.04 (WSL) | Python 3.11+, GTK, WebKit2GTK e PyGObject do sistema (ou Qt com `--qt`) e o Claude Code. O comando do terminal instala o Claude Code, se você autorizar. |
| **macOS** | Experimental | Python 3.11+ e o Claude Code. O comando do terminal instala o Claude Code, se você autorizar. |

**Claude Code**, instalado e com **a sua própria sessão iniciada**. Sem isso dá para criar e abrir projetos, mas não
sessões: o Kibo mostra o estado dele, o comando oficial para instalar e um botão para entrar, onde o login é feito por
você. O Kibo não inclui nem revende o Claude Code, e não lê suas credenciais.

> **Beta: teste com o Claude Code.** O Kibo foi feito e testado 100% com o Claude Code. A ideia é que mais adiante ele
> funcione com mais agentes de IA.

## Privacidade

O Kibo não tem servidor próprio, contas, telemetria nem backup na nuvem, e não lê suas credenciais. As conversas, os
anexos e as configurações ficam no seu computador. O que sai para a internet é o que o Claude Code já envia à
Anthropic, e o que você ativar (buscar versões novas, baixar o VS Code).

[Política de privacidade](https://kibo.nexsoftgroup.com/privacidad) (em espanhol) ·
[Segurança e verificação](https://kibo.nexsoftgroup.com/seguridad) (em espanhol) ·
[Termos de uso](https://kibo.nexsoftgroup.com/terminos#pt-BR)

## Comentários, problemas e ideias

O Kibo está em beta e seus comentários nos ajudam muito. Escreva em português, espanhol ou inglês.

- **Algo não funciona?** [Relate um problema](https://github.com/nexsoftgroup/kibo/issues/new?template=problema.yml).
  Conte sua versão do Kibo, seu sistema e os passos para o problema acontecer.
- **Teve uma ideia?** [Sugira](https://github.com/nexsoftgroup/kibo/issues/new?template=idea.yml).

Antes de colar registros ou capturas de tela, confira que não tenham senhas, tokens nem dados de clientes.

---

<p align="center">
  O Kibo é uma ferramenta que fizemos na <a href="https://nexsoftgroup.com"><b>NexSoft</b></a> e compartilhamos de graça.<br>
  <sub>Claude Code é uma marca da Anthropic. O Kibo não é um produto da Anthropic.</sub>
</p>
