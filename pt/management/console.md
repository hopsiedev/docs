# Console e controles de energia

O **Console** é a interface principal para interagir diretamente com o servidor do jogo. Neste guia, você aprenderá como monitorar o uso de hardware, enviar comandos de jogo e gerenciar os estados de energia do seu servidor.

---

## Controles de energia (botões de ação)

No canto superior direito ou na barra lateral do painel do console, você encontrará quatro botões principais de controle de energia:

* **Iniciar:** Liga o contêiner do servidor e inicia o processo do jogo. Use isto se o seu servidor estiver atualmente "Offline".
* **Parar:** Envia um sinal de desligamento normal para o jogo (por exemplo, executando `/stop` ou `/save-all` no Minecraft). Isso salva seu progresso e desliga o servidor com segurança.
* **Reiniciar:** Para o jogo graciosamente e o reinicia imediatamente. Ideal para aplicar alterações de configuração ou limpar o cache de RAM.
* **Matar:** Encerra instantaneamente o processo do jogo sem salvar.
  > [!CAUTION] 
  > **Só use "Kill" se o seu servidor estiver completamente congelado ou não responder ao comando "Stop".** Usar Kill regularmente pode causar corrupção de arquivos, reverter o progresso mundial ou corromper entradas de banco de dados.

---

## Gráficos de monitoramento em tempo real

O painel Revactyl exibe gráficos contínuos e em tempo real que representam a utilização de recursos do seu servidor:

1. **Uso de CPU:** A porcentagem de capacidade de processamento usada. Se permanecer próximo de 100% por longos períodos, os jogadores poderão sofrer atrasos (considere otimizar plug-ins, mods ou atualizar seu plano).
2. **Uso de memória (RAM):** Exibe a memória atual alocada em comparação com o limite do seu plano (por exemplo, `4 GB / 8 GB`). 
   * *Se o servidor exceder seu limite de memória, o assassino OOM (Out Of Memory) integrado do painel irá parar automaticamente o servidor para proteger a estabilidade do nó. Otimize seus arquivos de jogo ou atualize seu plano se você atingir esse limite com frequência.*
3. **Uso de disco:** Espaço de armazenamento total consumido pelos arquivos do jogo (mods, mundos, logs, backups). Certifique-se de excluir arquivos de log antigos (`latest.log`, `debug.log`) ou backups antigos para liberar espaço em disco.

---

## Enviando comandos do console

Abaixo da tela preta do terminal, há uma barra de comandos de texto chamada **"Digite um comando..."**:

* Você pode digitar qualquer comando aqui para controlar o jogo diretamente do console sem precisar de privilégios de administrador no jogo.
* **Não prefixe comandos com uma barra (`/`)**. Por exemplo, digite `op PlayerName` ou `say Hello World` e pressione Enter.
* Quaisquer respostas ou erros do servidor do jogo serão impressos em tempo real no log do console acima.