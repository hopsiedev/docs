#Conexão SFTP (FileZilla/WinSCP)

Para transferir pastas inteiras, mapas pesados, modpacks grandes ou fazer modificações em massa em seu servidor, o gerenciador de arquivos da web pode ser lento. Para essas tarefas, usar um cliente **SFTP (Secure File Transfer Protocol)** é a melhor opção.

---

## 1. Recupere suas credenciais SFTP

Cada servidor de jogo na Vellix Hosting tem seus próprios detalhes exclusivos de conexão SFTP:

1. Faça login em seu servidor no painel em [panel.vellix.host](https://panel.vellix.host).
2. Clique na guia **"Configurações"** ou **"SFTP"** no menu de navegação da barra lateral.
3. Localize a seção **Detalhes do SFTP** para encontrar:
   * **Endereço/Host do Servidor:** O endereço do nó que hospeda seu servidor (por exemplo, `sftp.vellix.host` ou um endereço IP).
   * **Porta:** Geralmente `2022` (a porta SFTP padrão para nosso daemon de painel).
   * **Nome de usuário:** Um identificador de usuário exclusivo formatado como `yourusername.serverid` (por exemplo, `admin.a1b2c3d4`).
   * **Senha:** **Esta é exatamente a mesma senha** que você usa para fazer login no painel da web.

---

## 2. Conectando-se ao FileZilla (recomendado)

[FileZilla](https://filezilla-project.org/) é um cliente SFTP gratuito e multiplataforma disponível para Windows, macOS e Linux.

### Etapas para conectar:
1. Inicie o FileZilla.
2. Na barra **Quickconnect** na parte superior, preencha os seguintes campos:
   * **Host:** Copie e cole o *Endereço do Servidor* do painel.
   * **Nome de usuário:** Copie e cole o *Nome de usuário* do painel.
   * **Senha:** Digite a senha da sua conta.
   * **Porta:** Digite `2022`.
3. Clique no botão **"Conexão rápida"**.
4. Se um aviso sobre uma *"Chave de host desconhecida"* aparecer, marque a caixa *"Sempre confiar neste host"* e clique em **OK**.
5. Uma vez conectado, os arquivos locais do seu computador serão exibidos à esquerda e o diretório do servidor remoto aparecerá à direita. Agora você pode arrastar e soltar arquivos para transferi-los.

---

## 3. Conectando com WinSCP (somente Windows)

[WinSCP](https://winscp.net/) é um utilitário popular e gratuito somente para Windows para transferências seguras.

### Etapas para conectar:
1. Abra o WinSCP.
2. Na janela **Login**, configure o seguinte:
   * **Protocolo de arquivo:** Selecione **SFTP**.
   * **Nome do host:** Insira o *Endereço do servidor* no painel.
   * **Número da porta:** Insira `2022`.
   * **Nome de usuário:** Digite seu *Nome de usuário* no painel.
   * **Senha:** Digite a senha da sua conta.
3. Clique em **"Login"** (ou clique em **"Salvar"** para armazenar esta sessão para facilitar o acesso futuro).
4. Aceite o aviso da chave do host do servidor em sua primeira conexão.

---

## Dicas essenciais de transferência

> [!TIP] 
> **Evite transferir pastas brutas com milhares de arquivos pequenos:** Protocolos como SFTP exigem um handshake para cada arquivo. Transferir diretamente uma pasta com 2.000 arquivos mod pode levar horas. Em vez disso, compacte a pasta em seu computador, carregue o arquivo `.zip` via SFTP e use a opção **"Desarquivar"** do gerenciador de arquivos da web para extraí-lo em segundos.

> [!WARNING] 
> Se você atualizar a senha da sua conta no painel da web (conforme descrito no Guia de segurança), sua senha SFTP será atualizada instantaneamente para corresponder a ela. Não se esqueça de atualizar suas senhas de conexão salvas no FileZilla ou WinSCP!