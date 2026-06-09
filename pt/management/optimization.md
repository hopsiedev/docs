# Dicas de otimização e desempenho do servidor

Lag e elástico podem arruinar a experiência do jogador. Embora a Vellix Hosting forneça processadores Ryzen 9 de alta frequência e SSDs NVMe rápidos, software de servidor não otimizado, configurações pesadas de mod ou contagens excessivas de entidades ainda podem degradar o desempenho. 

Siga estas dicas de otimização profissional para manter seu servidor funcionando a sólidos 20 TPS (Ticks Per Second).

---

## 1. Pré-gere seu mundo (crítico para Minecraft)

Gerar novos pedaços dinamicamente quando os jogadores voam com Elytras ou correm rápido é a causa número 1 do atraso do servidor. Ele sobrecarrega os ciclos de leitura/gravação da CPU e do disco.

### Como pré-gerar pedaços:
1. Instale o plugin **Chunky** (compatível com Spigot, Paper, Fabric, Forge).
2. Pare seu servidor.
3. Em `server.properties`, defina o tamanho da borda mundial (por exemplo, um raio de 5.000 blocos).
4. Inicie o servidor e execute estes comandos no **Console**:
   * `chunky center 0 0` (define o centro de geração).
   * `chunky radius 5000` (define o raio de geração).
   * `chunky start` (inicia o processo de geração).
5. Deixe Chunky completar a tarefa antes de permitir que os jogadores entrem. Pode levar várias horas dependendo do raio. Depois de concluído, o atraso no carregamento do bloco será praticamente eliminado.

---

## 2. Otimize os arquivos de configuração do servidor

Se você estiver executando um servidor Minecraft, use **Paper** ou **Purpur** em vez de Vanilla ou Spigot. Eles contêm patches de desempenho avançados.

Abra os seguintes arquivos no **Gerenciador de arquivos da Web** e ajuste estes valores:

###`server.properties`
* `view-distance=6` (Controla quantos pedaços são enviados ao cliente. Valores entre 6 e 8 são recomendados).
* `simulation-distance=4` (Controla quais blocos de entidades ativas e ticks são executados. Reduzir para 4 ou 5 reduz drasticamente a carga da CPU).

### `paper-world-defaults.yml` (ou `spigot.yml`)
* **Intervalos de ativação de entidades:** Reduza a distância em que animais, monstros e itens diversos funcionam.
* **Máximo de colisões de entidades:** Limite quantas vezes as entidades verificam colisões por tick (por exemplo, defina `max-entity-collisions=2`).

---

## 3. Coleta de lixo e dicas de memória

* **Use versões modernas do Java:** Versões mais recentes do Java (como Java 21) têm coleta de lixo superior (ZGC/G1GC) que reduz picos de atraso durante a limpeza de memória.
* **Evite Modpacks inchados:** Cada mod ativo aumenta o consumo de memória. Remova mods apenas estéticos que não sejam críticos para o jogo ou mods que executem cálculos excessivos de ticks.
* **Monitore logs em busca de spam:** Se um plug-in gera erros constantemente em seu console, ele gravará milhares de linhas em seu disco, criando um atraso no disco. Repare a configuração ou remova o plugin com defeito.