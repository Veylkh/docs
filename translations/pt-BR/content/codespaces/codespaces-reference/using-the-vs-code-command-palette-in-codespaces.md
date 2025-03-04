---
title: Usando a paleta de comando do Visual Studio no GitHub Codespaces
intro: 'Você pode usar a função de Paleta de Comando de {% data variables.product.prodname_vscode %} para acessar muitos comandos em {% data variables.product.prodname_github_codespaces %}.'
versions:
  fpt: '*'
  ghec: '*'
type: reference
topics:
  - Codespaces
  - Visual Studio Code
product: '{% data reusables.gated-features.codespaces %}'
shortTitle: Paleta de Comando do VS Code
allowTitleToDifferFromFilename: true
redirect_from:
  - /codespaces/codespaces-reference/using-the-command-palette-in-codespaces
---

## Sobre o {% data variables.product.prodname_vscode_command_palette %}

A Paleta de Comando é uma das funcionalidades focais de {% data variables.product.prodname_vscode %} e está disponível para você usar em {% data variables.product.prodname_github_codespaces %}. A Paleta de Comando permite que você acesse muitos comandos para {% data variables.product.prodname_codespaces %} e {% data variables.product.prodname_vscode_shortname %}. Para obter mais informações sobre como usar o {% data variables.product.prodname_vscode_command_palette_shortname %}, consulte "[Interface de usuário](https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette)" na documentação do {% data variables.product.prodname_vscode_shortname %}.

## Acessando o {% data variables.product.prodname_vscode_command_palette_shortname %}

Você pode acessar o {% data variables.product.prodname_vscode_command_palette_shortname %} de várias maneiras.

- <kbd>Shift</kbd>+<kbd>Command</kbd>+<kbd>P</kbd> (Mac) / <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd> (Windows/Linux).

  Observe que este comando é um atalho de teclado reservado no Firefox.
- <kbd>F1</kbd>
- No Menu de Aplicativos, clique em **Ver > Paleta de Comando…**.

  ![Menu do aplicativo](/assets/images/help/codespaces/codespaces-view-menu.png)

## Comandos para {% data variables.product.prodname_codespaces %}

Para ver todos os comandos relacionados a {% data variables.product.prodname_codespaces %}, [acesse o {% data variables.product.prodname_vscode_command_palette_shortname %}](#accessing-the-command-palette) e, em seguida, comece a digitar "Codespaces".

![Uma lista de todos os comandos que se referem a codespaces](/assets/images/help/codespaces/codespaces-command-palette.png)

### Suspender ou interromper um codespace

Se você adicionar um novo segredo ou alterar o tipo de máquina, você terá que parar e reiniciar o codespace para que aplique suas alterações.

Para suspender ou interromper o contêiner do seu codespace, [acesse o {% data variables.product.prodname_vscode_command_palette_shortname %}](#accessing-the-command-palette)e, em seguida, comece a digitar "parar". Selecione **Codespaces: Parar o codespace atual**.

![Comando para parar um codespace](/assets/images/help/codespaces/codespaces-stop.png)

### Adicionando um contêiner de desenvolvimento a partir de um modelo

Para adicionar um contêiner de desenvolvimento a partir de um modelo, [acesse o {% data variables.product.prodname_vscode_command_palette_shortname %}](#accessing-the-command-palette) e, em seguida, comece a digitar "dev container". Selecione **Codespaces: Adicionar arquivos de configuração de Contêiner do Desenvolvimento...**

![Comando para adicionar um contêiner de desenvolvimento](/assets/images/help/codespaces/add-prebuilt-container-command.png)

### Reconstruindo um codespace

Se você adicionar um contêiner de desenvolvimento ou editar qualquer um dos arquivos de configuração (`devcontainer.json` e `arquivo Docker`), você terá que reconstruir seu codespace para aplicar suas alterações.

Para reconstruir seu contêiner, [acesse o {% data variables.product.prodname_vscode_command_palette_shortname %}](#accessing-the-command-palette)e, em seguida, comece a digitar "recriar". Selecione **Codespaces: Reconstruir Contêiner**.

![Comando para reconstruir um codespace](/assets/images/help/codespaces/codespaces-rebuild.png)

### Registros de codespaces

Você pode usar o {% data variables.product.prodname_vscode_command_palette_shortname %} para acessar os registros de criação do codespace ou você pode usá-lo para exportar todos os registros.

Para recuperar os logs para {% data variables.product.prodname_codespaces %}, [acesse o {% data variables.product.prodname_vscode_command_palette_shortname %}](#accessing-the-command-palette) e, em seguida, comece a digitar "log". Selecione **Codespaces: Exportar logs** para exportar todos os logs relacionados a {% data variables.product.prodname_codespaces %} ou selecione **Códigos: Visualizar logs de criação** para ver os logs relacionados à configuração.

![Comando para acessar os registros](/assets/images/help/codespaces/codespaces-logs.png)
