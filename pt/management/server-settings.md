# Opções de inicialização e alocações de portas

Para executar mods personalizados, configurar sistemas de votação, configurar chats de voz ou modificar a versão do Java que seu servidor executa, você precisará gerenciar suas alocações de portas e variáveis de inicialização.

---

## 1. Alocações de portas (configurações de rede)

Seu servidor recebe um IP e uma porta primários (por exemplo, `190.22.44.112:25565`). Alguns plug-ins (como *Dynmap*, *Votifier* ou *Simple Voice Chat*) requerem suas próprias portas adicionais para comunicação.

### Como solicitar e atribuir portas adicionais:
1. Faça login em [panel.vellix.host](https://panel.vellix.host) e selecione seu servidor.
2. Clique na aba **"Rede"** no menu da barra lateral.
3. Se você tiver alocações disponíveis, clique em **"Criar Alocação"** (ou abra um ticket de suporte no Discord se precisar de portas adicionais atribuídas ao seu nó).
4. A nova porta aparecerá na lista.
5. No arquivo de configuração do plugin, substitua a porta padrão pela nova porta atribuída (nunca use portas aleatórias; use apenas portas alocadas especificamente para o seu servidor na guia Rede).

---

## 2. Modificando opções de inicialização

A guia **"Inicialização"** contém variáveis de ambiente importantes que determinam como o executável do servidor de jogo é iniciado:

* **Versão Java:** Selecione a versão do kit de desenvolvimento Java (JDK).
  * **Java 8/11:** Para versões mais antigas do Minecraft (1.12.2 e inferiores).
  * **Java 17:** Padrão para Minecraft 1.18 a 1.20.4.
  * **Java 21:** Padrão para Minecraft 1.20.5 e superior.
* **Arquivo Jar do Servidor:** O nome do arquivo que o servidor executará (por exemplo, `server.jar` ou `vanilla.jar`). Certifique-se de que o arquivo carregado em seu Gerenciador de arquivos tenha exatamente o mesmo nome digitado aqui.
* **Variáveis ​​de comando de inicialização:** Sinalizadores personalizados, como número máximo de jogadores, portas de consulta ou versões do servidor, dependendo do jogo.

> [!IMPORTANT] 
> Algumas variáveis de inicialização são bloqueadas pelo sistema para manter a estabilidade. Se você precisar fazer modificações em campos bloqueados ou precisar de sinalizadores de inicialização personalizados (como sinalizadores de desempenho do Aikar), entre em contato com nossa equipe de suporte no Discord.