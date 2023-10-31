# Setup Configuration

> Configuração do ambiente de desenvolvimento
>> Testado na distribuições linux:
>>> - Pop Os
>>> - Ubuntu  

### Removendo travas eventuais do apt

   ``` 
   sudo rm /var/lib/dpkg/lock-frontend ; sudo rm /var/cache/apt/archives/lock ; 
   ```
----------------------------------------------------------------------------------
 ### Atualizar os repositórios
   ``` 
   sudo apt update -y
   ```
 ### Atualizar o sistema 

   ``` 
   sudo apt upgrade -y 
   ```

Na distribuição Linux Pop Os pode ser utilizado também o seguinte comando   :

   ``` 
   sudo apt full-upgrade
   ```
----------------------------------------------------------------------------------
###  Instalação de codecs 

   ``` 
   sudo apt install ubuntu-restricted-extras 
   ```
   Na distribuição Linux Pop Os pode ser utilizado também o seguinte comando instalação de codecs 

   ``` 
   sudo apt install -y ubuntu-restricted-extras
   ```
  em seguinda o comando :

   ``` 
   sudo apt install -y gstreamer1.0-plugins-bad gstreamer1.0-plugins-ugly gstreamer1.0-plugins-good libavcodec-extra gstreamer1.0-libav chromium-codecs-ffmpeg-extra libdvd-pkg
   ```
----------------------------------------------------------------------------------  
### Instalar suporte a flatpak 

   ``` 
   sudo apt install flatpak
   ```

  ``` 
   flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
   ```
----------------------------------------------------------------------------------
 ### Instalar o suporte pacotes snap

  1. atualize o sistema 
  2. execute o seguinte comando :
   ``` 
   sudo apt install snapd
   ```
   3. Para testar seu sistema, instale o snap hello-world e verifique se ele funciona corretamente:

   ``` 
   sudo snap install hello-world
   ```
   após  a conclusão execute o comando    

  ``` 
    hello-world
   ```
   para testar a instalação de pacotes   snap

----------------------------------------------------------------------------------
 ### Ataualizar pelo terminal o pacotes  snap execurte o seguinte comando :
  
  - ### Flatpaks
  
    ``` 
    flatpak update
    ```
- ### Snaps
   ``` 
  snap refresh
   ```
  ``` 
  snap refresh --list
   ```
----------------------------------------------------------------------------------
 ### Instalar suporte 7zip
  ``` 
  sudo apt-get install p7zip p7zip-full p7zip-rar lzma lzma-dev
   ```
----------------------------------------------------------------------------------
 ### Instalar openjdk 

  1. Adicione o repositório 
   ``` 
   sudo add-apt-repository ppa:openjdk-r/ppa
   ```
  2. Atualize o gerenciador de pacotes
   ``` 
  sudo apt-get update
   ```
  3. Agora use o comando abaixo para instalar 
   ``` 
  sudo apt-get install openjdk-8-jdk
   ```
  4. Agora use o comando abaixo para vertificar a versão instalada 
   ``` 
  java -version 
   ```
----------------------------------------------------------------------------------
 ### Instalar google chorme 
   ``` 
  cd ~/Downloads/ && wget -c https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb && sudo dpkg -i *.deb
   ```
----------------------------------------------------------------------------------   
### Instalar curl 
   ``` 
  sudo apt  install curl
   ```
----------------------------------------------------------------------------------   
### Instalar o pacote de comandos para internet
   ``` 
  sudo apt install net-tools
   ```
----------------------------------------------------------------------------------
### Instalar o VSCode

 - ``` 
    curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.gpg
   ```

- ``` 
    sudo install -o root -g root -m 644 microsoft.gpg /etc/apt/trusted.gpg.d/
   ```

- ``` 
   sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main" > /etc/apt/sources.list.d/vscode.list'
   ```

- ``` 
    sudo apt-get install apt-transport-https -y
   ```

- ``` 
    sudo apt-get update
   ```

- ``` 
    sudo apt-get install code -y 
   ```
----------------------------------------------------------------------------------
### Instalar o Postman

   ``` 
  snap install postman
   ```
----------------------------------------------------------------------------------
### Instalar o Insomnia

   ``` 
  sudo snap install insomnia
   ```
----------------------------------------------------------------------------------
### Instalar o mysql-workbench
   ``` 
  sudo snap install mysql-workbench-community
   ```
----------------------------------------------------------------------------------   
### Instalar o DBeaver
   ``` 
 sudo snap install dbeaver-ce
   ```
----------------------------------------------------------------------------------  
### Instalar qualquer app .deb e todas sua dependências 
   ``` 
sudo dpkg -i *.deb ; sudo apt-get install -f -y
   ```

----------------------------------------------------------------------------------
### Atualização do sistema e limpeza dos sistema 
   ``` 
 sudo apt update && sudo apt dist-upgrade -y && sudo apt autoclean -y && sudo apt autoremove -y
   ```
----------------------------------------------------------------------------------
### Atualização do sistema geral 
   ``` 
 sudo apt update && sudo apt dist-upgrade -y 
   ```

----------------------------------------------------------------------------------
### limpeza dos sistema

- ``` 
    sudo apt autoclean
   ```
- ``` 
    sudo apt autoremove -y
   ```
----------------------------------------------------------------------------------
