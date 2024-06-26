# Como configurar/instalar/usar o `Déjà Dup Backups` no `Linux Ubuntu`

## Resumo

Neste documento estão contidos os principais comandos e configurações para configurar/instalar/usar o `Déjà Dup Backups` no `Linux Ubuntu`.

## _Abstract_

_This document contains the main commands and settings for configuring/installing/using the `Déjà Dup Backups` on `Linux Ubuntu`._

## Descrição [2]

### `Déjà Dup Backups`

O Déjà Dup Backups é uma ferramenta de backup simples e intuitiva para sistemas baseados em Linux, como o Ubuntu. Ele oferece uma interface amigável para configurar e automatizar backups de arquivos e diretórios importantes. Com o Déjà Dup, os usuários podem programar backups regulares para dispositivos locais, como discos rígidos externos, ou serviços de armazenamento em nuvem, como o Google Drive ou o Dropbox. Além disso, ele suporta criptografia para proteger os dados sensíveis durante o armazenamento e oferece opções de restauração fáceis para recuperar arquivos em caso de perda ou falha do sistema. É uma solução eficaz e confiável para manter os dados seguros e acessíveis.


## 1. Como configurar/instalar/usar o `Déjà Dup Backups` no `Linux Ubuntu` [1][3]

Para configurar/instalar/usar o `Déjà Dup Backups` no `Linux Ubuntu`, você pode seguir estes passos:

1. Abra o terminal. Você pode fazer isso pressionando: `Ctrl + Alt + T`

2. Certifique-se de que seu sistema esteja limpo e atualizado.

    2.1 Limpar o `cache` do gerenciador de pacotes APT. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo APT e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando: `sudo apt clean` 
    
    2.2 Remover pacotes `.deb` antigos ou duplicados do cache local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando: `sudo apt autoclean`

    2.3 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando: `sudo apt autoremove -y`

    2.4 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`: `sudo apt update -y`

    2.5 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:  `sudo apt list --upgradable`

    2.6 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update -y`. Digite o seguinte comando e pressione `Enter`: `sudo apt full-upgrade -y`

    2.7 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando: `sudo apt autoremove -y`

    2.8 Remover pacotes `.deb` antigos ou duplicados do cache local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando: `sudo apt autoclean`

Para instalar o `Déjà Dup Backups`, um aplicativo de backup muito utilizado no Linux Ubuntu, através do Terminal Emulator, você pode seguir os seguintes passos. Este processo geralmente envolve a utilização de comandos `apt` para instalar pacotes de software no Ubuntu e em outras distribuições baseadas em Debian.

3. **Instale o `Déjà Dup`:** Após atualizar a lista de pacotes, instale o `Déjà Dup` com o comando: `sudo apt install deja-dup -y`

    Esse comando irá baixar e instalar o Déjà Dup e todas as dependências necessárias. Durante a instalação, pode ser que o sistema peça a confirmação para continuar, para isso, você deve pressionar `Y` e então `Enter`.

4. **Verifique a Instalação:** Após a instalação, você pode verificar se o `Déjà Dup` foi instalado corretamente digitando `deja-dup` no terminal ou procurando por ele no menu de aplicativos.

5. **Use o `Déjà Dup`:** Agora que o Déjà Dup está instalado, você pode configurá-lo e começar a fazer backups dos seus arquivos. Ele oferece uma interface gráfica intuitiva, facilitando o processo de backup e restauração.

Lembre-se de que é importante manter seus softwares sempre atualizados, não apenas por questões de novas funcionalidades, mas também por segurança. Para atualizar o Déjà Dup e outros softwares instalados via apt, você pode usar os comandos:

    ```
    sudo apt update -y
    sudo apt upgrade -y
    ```

Esses comandos vão atualizar a lista de pacotes e depois atualizar os pacotes que têm novas versões disponíveis.

O `Déjà Dup Backups` é projetado para ser uma ferramenta de backup que respeita a privacidade do usuário e a segurança dos dados. Aqui estão alguns pontos importantes que garantem que ele não "puxe" ou colete seus dados de maneira indevida:

1. **Controle do Usuário:** O `Déjà Dup` dá ao usuário total controle sobre o que é copiado e para onde. O usuário especifica os diretórios de origem para backup e o destino onde os backups serão armazenados. Isso pode ser um dispositivo de armazenamento local, um drive externo, ou uma conta de armazenamento em nuvem escolhida pelo usuário.

2. **Privacidade e Segurança:** Por padrão, o `Déjà Dup` realiza backups criptografados, o que significa que seus dados são protegidos e não podem ser lidos por outros sem a chave de criptografia. Isso é particularmente importante quando se está usando armazenamento em nuvem como destino de backup.

3. **Software Livre:** O `Déjà Dup` é software livre, o que significa que seu código-fonte é aberto e disponível para revisão. Isso permite que a comunidade examine o software em busca de potenciais vulnerabilidades de segurança ou comportamentos maliciosos, como a coleta não autorizada de dados.

4. **Sem Coleta de Dados:** Não há mecanismos dentro do `Déjà Dup` que coletam ou enviam seus dados pessoais para servidores externos (com exceção do destino de backup escolhido por você, como um serviço de nuvem, onde os dados são enviados para serem armazenados). O propósito do software é puramente realizar backups e restaurações conforme configurado pelo usuário.

5. **Transparência:** Sendo um projeto de código aberto, as atualizações e as mudanças no `Déjà Dup` são documentadas e disponíveis para o público. Isso garante uma camada adicional de transparência em relação a como o software opera e é desenvolvido.

É importante, no entanto, praticar uma vigilância contínua em relação a qualquer software que você use, especialmente quando ele lida com dados pessoais ou sensíveis. Certificar-se de que você está usando a versão mais recente do Déjà Dup e que seu destino de backup é seguro e confiável também são práticas recomendadas para manter seus dados seguros.

### 1.1 Código completo para configurar/instalar/usar

Para configurar/instalar/usar o `Déjà Dup Backups` no `Linux Ubuntu` sem precisar digitar linha por linha, você pode seguir estas etapas:

1. Abra o terminal. Você pode fazer isso pressionando: `Ctrl + Alt + T`

2. Digite o seguinte comando e pressione `Enter`:

    ```
    sudo apt clean
    sudo apt autoclean -y
    sudo apt autoremove -y
    sudo apt update -y
    sudo apt uptoremove -y
    sudo apt autoclean -y
    sudo apt install deja-dup -y
    ```


## Referências

[1] OPENAI. ***Instale Déjà Dup via Terminal.*** Disponível em: <https://chat.openai.com/c/d89b8216-2d5a-4300-a2db-dd075d12827d> (texto adaptado). Acessado em: 03/04/2023 17:11.

[2] OPENAI. ***Vs code: editor popular.*** Disponível em: <https://chat.openai.com/c/b640a25d-f8e3-4922-8a3b-ed74a2657e42> (texto adaptado). Acessado em: 03/04/2024 17:10.

