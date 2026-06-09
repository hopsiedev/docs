# Backups e restauração

Proteger o progresso do seu servidor é crucial. A perda de dados pode ocorrer devido a mods com defeito, arquivos salvos corrompidos ou erros de configuração. Neste guia, você aprenderá como criar backups manuais, restaurá-los e agendar backups automáticos.

---

## 1. Criando um backup manual

Você deve sempre criar um backup antes de fazer alterações importantes, atualizar versões do jogo ou adicionar novos mods.

1. Vá para o seu servidor no painel em [panel.vellix.host](https://panel.vellix.host).
2. Clique na aba **"Backups"** no menu da barra lateral.
3. Clique no botão **"Criar backup"** no canto superior direito.
4. Preencha os campos:
   * **Nome do backup:** Dê ao seu backup um nome descritivo (por exemplo, *Antes da atualização do Forge* ou *Salvar o mundo 2026*).
   * **Arquivos e pastas ignorados:** *(Opcional)* Insira caminhos relativos para arquivos ou pastas que você deseja excluir do backup (por exemplo, excluindo a própria pasta `backups/` ou registros grandes como `logs/` para economizar espaço). Cada regra deve ir para uma nova linha.
5. Clique em **"Iniciar Backup"**.

O painel compactará seus arquivos em um arquivo seguro em segundo plano. O cartão de backup mostrará um botão giratório até que esteja totalmente concluído.

---

## 2. Restaurando ou baixando um backup

Depois que um backup for criado, clique nos três pontos `...` no cartão de backup para abrir o menu de ação:

* **Restaurar:** Reverte todos os arquivos do servidor para o estado em que estavam quando o backup foi feito.
  > [!WARNING] 
  > **A restauração de um backup substituirá os arquivos existentes.** Você pode marcar a caixa *"Excluir arquivos antes de restaurar"* para limpar o diretório do servidor e garantir que nenhum arquivo antigo e conflitante permaneça antes de colocar os arquivos de backup.
* **Download:** Baixa o arquivo de backup (`.tar.gz`) diretamente para o seu computador.
* **Bloquear/Desbloquear:** Bloquear um backup evita que ele seja excluído automática ou manualmente por engano quando você atingir o limite de backup.
* **Excluir:** Exclui permanentemente o arquivo de backup para liberar espaço.

---

## 3. Agendamento de backups automáticos

Criar backups manualmente é útil, mas automatizar o processo garante que você nunca perca o progresso, mesmo se esquecer de executá-los. Você pode configurar um agendamento de backup na guia **"Programações"**:

1. Clique na aba **"Agendamentos"** na barra lateral.
2. Clique em **"Criar agendamento"** no canto superior direito.
3. Dê um nome à sua programação (por exemplo, *Backup diário*).
4. Defina a frequência usando a notação Cron. Aqui estão predefinições comuns:
   * **Todos os dias à meia-noite:** Minutos: `0`, Horas: `0`, Dia do mês: `*`, Mês: `*`, Dia da semana: `*`
   * **A cada 12 horas:** Minutos: `0`, Horas: `*/12`, Dia do mês: `*`, Mês: `*`, Dia da semana: `*`
5. Clique em **"Criar Agendamento"**.
6. Clique no agendamento recém-criado na lista e, em seguida, clique em **"Nova Tarefa"** no canto superior direito.
7. Altere a **Ação** para **"Criar Backup"**.
8. Preencha os arquivos ignorados (se houver) e clique em **"Criar Tarefa"**.

Seu servidor agora executará backups automáticos no intervalo configurado.