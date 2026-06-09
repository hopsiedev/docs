#Bancos de dados MySQL

Muitos plug-ins e mods de jogos (como *LuckPerms*, *CoreProtect*, *Dynmap* ou sistemas de registro personalizados) exigem um banco de dados **MySQL/MariaDB** para armazenar dados do jogador, permissões ou bloquear edições de forma rápida e confiável, em vez de armazená-los em arquivos simples locais `.json` ou `.db`, que podem diminuir o desempenho do servidor.

Com Vellix Hosting, você pode provisionar e gerenciar bancos de dados MySQL com um único clique diretamente do painel Revactyl.

---

## 1. Criando um banco de dados no painel

Para criar um novo banco de dados:

1. Acesse o painel do seu servidor no painel em [panel.vellix.host](https://panel.vellix.host).
2. Clique na aba **"Bancos de dados"** no menu de navegação da barra lateral.
3. Clique no botão **"Criar banco de dados"** no canto superior direito.
4. Preencha os campos:
   * **Nome do banco de dados:** Forneça um nome descritivo curto para o banco de dados (por exemplo, `luckperms` ou `playerdata`).
   * **Conexões de:** Defina como `%` (sinal de porcentagem) para permitir conexões de qualquer host (esta é a configuração mais flexível e evita problemas de firewall se conectar de fora do nó, por exemplo, servidores web ou proxies BungeeCord).
5. Clique no botão **"Criar banco de dados"**.

O banco de dados será criado instantaneamente e adicionado à lista.

---

## 2. Recuperando credenciais de banco de dados

Assim que seu banco de dados for criado, você verá um cartão com os parâmetros de conexão. Clique no ícone de cadeado para revelar a senha:

* **Host/Endpoint:** O endereço IP ou domínio do servidor de banco de dados (por exemplo, `mysql.vellix.host` ou um IP de nó).
* **Nome do banco de dados:** O nome final gerado pelo painel, geralmente anexado ao ID do seu servidor (por exemplo, `s1_luckperms`).
* **Nome de usuário:** O nome de usuário do banco de dados gerado automaticamente (por exemplo, `u1_xYzA`).
* **Senha:** A senha exclusiva e segura gerada para este usuário do banco de dados.
* **Porta:** A porta padrão do MySQL, que é `3306`.

---

## 3. Configurando seu plugin (exemplo: LuckPerms)

Para conectar um plugin ao seu novo banco de dados, abra o arquivo de configuração do plugin (geralmente `config.yml` ou `config.conf`) no **Gerenciador de arquivos da Web**:

1. Encontre a configuração `storage-method` ou tipo de armazenamento e altere-a de `h2` ou `sqlite` para **`mysql`**.
2. Substitua os espaços reservados de conexão pelas suas credenciais:

```yaml
# Typical MySQL database connection setup in Minecraft plugins
storage-method: mysql

address: "mysql.vellix.host:3306" # Enter the database Host and Port here
database: "s1_luckperms"          # Enter the generated Database Name
username: "u1_xYzA"               # Enter the Database Username
password: "your_secure_password"  # Enter the revealed Password
```

3. Salve o arquivo.
4. Reinicie o servidor do jogo no console para estabelecer a conexão com o banco de dados.

> [!NOTE] 
> O provisionamento do banco de dados é totalmente gratuito e o armazenamento do banco de dados não conta na alocação de disco do servidor primário. No entanto, recomendamos manter a higiene do banco de dados limpando logs antigos periodicamente para garantir o desempenho ideal da consulta.