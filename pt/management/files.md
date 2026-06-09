# Gerenciador de arquivos da web

O **Gerenciador de Arquivos** (encontrado na guia **Arquivos** no menu da barra lateral) permite que você gerencie todos os dados do seu servidor diretamente do seu navegador sem precisar de software externo.

---

## Operações básicas de arquivo

Ao abrir o Gerenciador de Arquivos, você verá o diretório raiz do seu servidor. A partir daqui, você pode realizar diversas ações principais:

* **Criar arquivos e pastas:** Clique nos botões **"Criar arquivo"** ou **"Nova pasta"** no canto superior direito.
* **Editar arquivos:** Clique em qualquer arquivo baseado em texto (como `.yml`, `.json`, `.conf`, `.properties` ou `.txt`). Isso abre um **editor de código integrado** com destaque de sintaxe. Depois de fazer as alterações, clique em **"Salvar conteúdo"** na parte inferior.
* **Fazer upload de arquivos:** Arraste e solte arquivos do seu computador diretamente na janela do navegador ou clique no botão **"Fazer upload"** para navegar e selecionar arquivos.
  > [!TIP] 
  > O gerenciador de arquivos da web é perfeito para edições de configurações individuais ou upload de arquivos menores (menos de 100 MB). Para transferências maiores (como mapas inteiros, mundos ou modpacks grandes), recomendamos conectar via **SFTP**.

---

## Menu de ação (os três pontos `...`)

À direita de cada arquivo e pasta, você encontrará um botão de três pontos `...` que abre o menu de ação:

1. **Renomear:** Altere o nome de um arquivo ou diretório.
2. **Mover/Copiar:** Realoque o arquivo. Você pode mover arquivos fornecendo seu caminho relativo (por exemplo, mover `server.properties` para uma pasta inserindo `backup-configs/server.properties`).
3. **Baixar:** Salve o arquivo diretamente em seu computador.
4. **Excluir:** Remova permanentemente o arquivo ou pasta do armazenamento do servidor.
   > [!WARNING] 
   > A exclusão de arquivos é permanente e não pode ser desfeita. Crie um backup do seu servidor antes de realizar exclusões em massa.

---

## Compactando e extraindo arquivos (.zip)

Carregar pastas contendo centenas de pequenos arquivos individuais (como modpacks ou configurações de plugins) um por um é altamente ineficiente. Em vez disso:

1. Compacte a pasta do seu computador em um arquivo `.zip`.
2. Carregue o arquivo `.zip` único no painel (por meio do Web File Manager ou SFTP).
3. No Gerenciador de arquivos da Web, clique nos três pontos `...` próximos ao arquivo `.zip` carregado.
4. Selecione **"Desarquivar"** ou **"Descompactar"**. O painel extrairá todos os arquivos e subpastas instantaneamente.
5. *(Opcional)* Exclua o arquivo `.zip` carregado para economizar espaço em disco.

Você também pode compactar arquivos no painel selecionando-os usando as caixas de seleção à esquerda, clicando no botão **"Arquivar"** na parte superior e baixando o arquivo `.zip` resultante.