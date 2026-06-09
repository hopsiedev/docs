# Carregando e instalando mods/plugins

Personalizar seu servidor com mods, plug-ins ou modos de jogo personalizados é uma das melhores maneiras de aprimorar a experiência de jogo. Este guia irá orientá-lo na instalação de plug-ins individuais, mods e modpacks de servidor inteiros em seu servidor Vellix Hosting.

---

## 1. Plugins vs. Mods: O que meu servidor usa?

Antes de enviar arquivos, você deve saber o que o software do seu servidor suporta:
* **Plugins (Spigot, Paper, Purpur):** Amplie a funcionalidade do servidor (como adicionar reivindicações, economia ou prefixos de bate-papo) sem exigir que os jogadores instalem nada em seus computadores.
* **Mods (Forge, Fabric, NeoForge):** Adicione blocos, itens, criaturas e dimensões personalizados. **Tanto o servidor quanto os jogadores devem ter exatamente os mesmos mods instalados.**

---

## 2. Instalação de plug-ins ou mods individuais

1. Baixe os arquivos `.jar` para os plug-ins/mods que deseja usar de fontes confiáveis (por exemplo, CurseForge, Modrinth ou SpigotMC).
   * *Certifique-se de que eles sejam compatíveis com a versão do jogo que seu servidor está executando.*
2. Pare o servidor no **Console**.
3. Abra o **Web File Manager** ou conecte-se via **SFTP**.
4. Navegue até a pasta apropriada:
   * Para plug-ins Spigot/Paper/Purpur: Carregue os arquivos `.jar` para o diretório **`plugins/`**.
   * Para mods Forge/Fabric: Carregue os arquivos `.jar` para o diretório **`mods/`**.
5. Volte para o **Console** e clique em **Iniciar** ou **Reiniciar**.
6. Verifique se eles foram carregados corretamente:
   * No Minecraft, execute o comando `plugins` no console (ou `/plugins` no jogo) para ver seus plugins ativos.

---

## 3. Instalando um Modpack completo (por exemplo, pacote de servidor CurseForge)

Para executar um modpack pré-empacotado (como RLCraft, Pixelmon ou Better MC):

1. Baixe os arquivos do **Server Pack** para o modpack (geralmente um arquivo `.zip` contendo as pastas `mods`, `config` e bibliotecas).
2. Pare seu servidor.
3. Abra seu cliente **SFTP** e conecte-se ao servidor.
4. Se você tiver arquivos existentes, primeiro faça backup deles e depois exclua-os do diretório do servidor para evitar conflitos.
5. Carregue o arquivo modpack `.zip` para o diretório raiz do seu servidor.
6. Abra o **Gerenciador de arquivos da Web** em seu navegador, localize o arquivo `.zip` carregado, clique nos três pontos `...` e escolha **"Desarquivar"** para extrair todos os arquivos.
7. Verifique as configurações de inicialização:
   * Na guia **"Inicialização"** na barra lateral, certifique-se de ter selecionado a **versão Java** correta exigida pelo modpack (por exemplo, Java 17 para Minecraft 1.18+, Java 21 para Minecraft 1.20.5+).
   * Certifique-se de que o **Arquivo Jar do Servidor** ou os parâmetros de inicialização correspondam aos requisitos do script de inicialização do modpack.
8. Volte para o **Console** e clique em **Iniciar**.

---

## Solução de problemas comuns

* **O servidor está preso em um loop de inicialização:** Verifique o log do console. Se você vir `java.lang.UnsupportedClassVersionError`, significa que sua versão do Java está desatualizada ou muito nova para a versão do jogo. Altere a versão do Java na guia **Inicialização**.
* **Erro de dependência ausente:** Alguns mods ou plug-ins exigem que outros mods da biblioteca principal funcionem. Leia a página de descrição do mod/plugin e carregue as dependências ausentes na pasta do servidor.
* **Modpack não carrega blocos personalizados:** Verifique se você carregou os arquivos mod para o diretório `mods/` do servidor e se instalou exatamente a mesma versão do modpack em seu inicializador local (CurseForge App, Modrinth App, Prism Launcher).