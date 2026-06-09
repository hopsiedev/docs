# Segurança da conta

Manter sua conta segura é essencial para proteger os arquivos, configurações e jogadores do servidor. Neste guia, você aprenderá como **alterar sua senha** e ativar a **autenticação de dois fatores (2FA)**.

---

## Alterando sua senha

Por segurança, recomendamos alterar a senha temporária gerada automaticamente que você recebeu em seu e-mail de boas-vindas o mais rápido possível.

### Etapas para atualizar sua senha:
1. Faça login no painel em [panel.vellix.host](https://panel.vellix.host).
2. Clique no avatar do seu perfil no canto superior direito (ou no ícone de configurações da conta na barra lateral).
3. Selecione **"Configurações da conta"**.
4. Vá até a seção **"Alterar senha"**.
5. Digite sua senha atual (a temporária do seu e-mail).
6. Digite sua nova senha e confirme no campo abaixo.
   * *Dica: use uma combinação de letras maiúsculas, minúsculas, números e símbolos especiais.*
7. Clique no botão **"Atualizar senha"**.

> [!NOTE] 
> Alterar sua senha desconectará todas as outras sessões ativas por segurança. Você precisará usar sua nova senha para logins futuros, bem como para sua conexão SFTP.

---

## Autenticação de dois fatores (2FA)

A autenticação de dois fatores adiciona uma camada extra de segurança. Cada vez que você fizer login, será solicitado seu nome de usuário, senha e um código de verificação dinâmico de 6 dígitos gerado por um aplicativo em seu telefone.

### Etapas para ativar 2FA:
1. Navegue até **"Configurações da conta"**.
2. Localize a seção **"Autenticação de dois fatores"**.
3. Clique no botão **"Ativar"**.
4. Você verá um **QR Code** e uma chave de recuperação de backup.
5. Abra um aplicativo autenticador em seu telefone (como **Google Authenticator**, **Authy** ou **Microsoft Authenticator**).
6. Digitalize o código QR usando seu aplicativo.
7. O aplicativo irá gerar um código de 6 dígitos que muda a cada 30 segundos.
8. Digite o código atual de 6 dígitos no painel para confirmar.
9. Clique em **"Enviar"** ou **"Ativar"**.

> [!IMPORTANT] 
> **Armazene suas chaves de recuperação em um local seguro e off-line.** Se você perder seu telefone ou excluir o aplicativo, precisará das chaves de recuperação para fazer login. Sem elas, você terá que abrir um ticket de suporte em nosso servidor Discord, e nossa equipe precisará verificar manualmente sua identidade antes de desativar o 2FA.

---

## Redefinindo uma senha esquecida

Se você esquecer sua senha:
1. Visite [panel.vellix.host](https://panel.vellix.host).
2. Clique em **"Esqueceu a senha?"** no cartão de login.
3. Insira o endereço de e-mail da sua conta e clique em **"Enviar link de redefinição de senha"**.
4. Siga o link enviado para seu e-mail para configurar uma nova senha.