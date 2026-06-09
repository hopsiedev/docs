# Subusuários e permissões

Se você estiver executando um servidor com uma equipe, talvez queira dar aos seus construtores, desenvolvedores ou coproprietários acesso ao painel do servidor. O recurso **Subusuários** permite que você convide outros jogadores para o seu painel com permissões específicas e granulares, garantindo que eles acessem apenas o que precisam.

---

## 1. Convidando um subusuário

Para adicionar um novo subusuário:

1. Faça login no painel em [panel.vellix.host](https://panel.vellix.host) e selecione seu servidor.
2. Clique na aba **"Usuários"** no menu de navegação da barra lateral.
3. Clique no botão **"Criar novo"** no canto superior direito.
4. Preencha o formulário de convite:
   * **E-mail do usuário:** Digite o endereço de e-mail exato da pessoa que você deseja convidar.
     * *Observação: Caso ainda não possua conta no painel, receberá um e-mail convite para configurar sua senha e se cadastrar.*
   * **Permissões:** Marque as caixas de seleção correspondentes às permissões que você deseja conceder.

---

## 2. Gerenciando permissões granulares

Você pode personalizar exatamente o que cada subusuário pode fazer no seu servidor. As permissões são divididas em categorias lógicas:

###Console de controle
* **Controlar estado de energia:** Permite iniciar, parar, reiniciar e encerrar o servidor.
* **Enviar comandos:** Permite digitar e enviar comandos na barra de comandos do console ao vivo.

### Gerenciamento de arquivos
* **Ler Arquivos:** Permite visualizar diretórios e abrir arquivos para leitura de conteúdo.
* **Escrever arquivos:** Permite editar arquivos, criar novos e fazer upload de pastas.
* **Excluir arquivos:** Permite excluir arquivos e pastas.
* **Detalhes SFTP:** Permite visualizar os detalhes da conexão SFTP (eles se conectarão usando seu próprio nome de usuário e senha do painel).

### Bancos de dados e backups
* **Criar Bancos de Dados:** Permite criar e excluir bancos de dados MySQL.
* **Ver senha do banco de dados:** Permite revelar credenciais de conexão com o banco de dados.
* **Criar backups:** Permite fazer backups manuais do servidor.
* **Restaurar backups:** Permite reverter arquivos do servidor usando um backup existente.

### Configurações e programações
* **Criar Agendamentos:** Permite agendar tarefas (reinicializações, backups, envio de mensagens automáticas).
* **Editar configurações de inicialização:** Permite modificar variáveis ​​de ambiente e opções de comando de inicialização.

---

## 3. Revogação ou edição de acesso

Você pode modificar as permissões de um subusuário ou remover totalmente seu acesso a qualquer momento:

* **Para editar permissões:** Vá para a guia **"Usuários"**, clique no ícone de edição (lápis) ao lado do e-mail do subusuário, marque/desmarque as permissões e clique em **"Salvar"**.
* **Para revogar o acesso:** Clique no ícone de exclusão (lixeira) ao lado do e-mail do subusuário. O acesso deles ao painel do seu servidor será encerrado imediatamente.