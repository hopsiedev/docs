---
title: "Hospedar Bots do Discord"
sidebarTitle: "Hospedar Bots"
description: "Saiba como hospedar e criar servidores gratuitos de bots do Discord na Vellix Hosting"
---

A Vellix Hosting oferece hospedagem gratuita de bots do Discord através da integração com a nossa comunidade do Discord. Siga este guia para configurar, implantar e gerenciar sua aplicação Node.js.

---

## Especificações do Serviço

Quando você cria um servidor gratuito de bots do Discord, você obtém:

* **Ambiente de Execução Dedicado**: Ambiente isolado de Node.js em um contêiner Docker.
* **Memória (RAM)**: 250 MB de memória RAM.
* **Armazenamento**: 1 GB de armazenamento SSD de alta velocidade.
* **Gerenciamento**: Acesso total ao console e gerenciamento de arquivos FTP/SFTP.

---

## Guia de Início Rápido Passo a Passo

Siga estas etapas para implantar o seu bot:

### 1. Crie o seu Servidor
Junte-se ao nosso servidor do Discord e vá para o canal dedicado de tickets ou criação de bots:
* **Canal do Discord**: [Suporte do Discord](https://discord.com/channels/1504707289385533461/1512867928717000876)
* Clique no botão de criação de servidor.
* ⚠️ **Importante**: Certifique-se de que suas Mensagens Diretas (DMs) do Discord estejam abertas para que o nosso bot possa enviar a sua senha temporária do painel!

### 2. Faça Login no Painel
* Acesse o painel de controle: [panel.vellix.host](https://panel.vellix.host)
* Faça login usando seu endereço de e-mail e a senha temporária enviada para suas DMs do Discord.
* (Opcional) Recomendamos alterar sua senha nas configurações da conta imediatamente.

### 3. Envie os Arquivos do seu Bot
* Selecione o servidor recém-criado no painel.
* Vá para a guia **Gerenciador de Arquivos** na barra lateral.
* Envie os arquivos do seu bot (por exemplo, `index.js`, `package.json`, arquivos `.env`).
* > [!CAUTION]
  > **NÃO envie a pasta `node_modules`.** O painel instalará as dependências automaticamente para economizar largura de banda e armazenamento.

### 4. Instalar Pacotes
* Vá para a guia **Console**.
* Seus pacotes serão instalados automaticamente a partir do seu `package.json` quando você iniciar o servidor pela primeira vez, ou você pode especificar opções de inicialização personalizadas.

### 5. Inicie o seu Bot
* Configure suas variáveis de ambiente, token e segredos no painel.
* Clique no botão verde **Iniciar** no Console para inicializar o seu bot!
