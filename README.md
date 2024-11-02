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
### Configuração inicial do  Git

 Definir o seu nome de usuário e endereço de e-mail. 

``` 
   git config --global user.name "Seu nome para exibição"
   git config --global user.email "seu-email@email.com"
```
#### Colorir as linhas
 Para melhorar a visualização do git no terminal podemos colorir as linhas com o comando abaixo.

``` 
   git config --global color.ui auto
   git config --global color.diff auto
   git config --global color.status auto
   git config --global color.branch auto
```
#### Testando Suas Configurações
Se você quiser testar as suas configurações, você pode usar o comando

``` 
   git config --list
```
#### Descartar todas as alterações não confirmadas, revertendo-os para o estado do  último commit  

``` 
  git checkout .
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
### Criar links simbólicos

```
   ln -s [arquivo_ou_diretório_destino] [nome_do_link]
```
exemplo : 

```
   ln -s /opt/lampp/htdocs/
```

#### Criar links simbólicos na  área de trabalho
```
   ln -s /home/[usuário]/[arquivo_ou_diretório_destino] /home/[usuário]/Área\ de\ Trabalho/workspace
```

----------------------------------------------------------------------------------   
### Instalar qualquer app .deb e todas sua dependências 
   ``` 
    sudo dpkg -i *.deb ; sudo apt-get install -f -y
   ```

----------------------------------------------------------------------------------
### Ativar o suporte a AppImage

``` 
   sudo apt install libfuse2
 ```

----------------------------------------------------------------------------------
###  Instalar o  Gear lever

 Um utilitário para gerenciar AppImages 

``` 
   flatpak install flathub it.mijorus.gearlever
 ```

----------------------------------------------------------------------------------
###   Instalar o gdedi

``` 
   sudo apt install gdebi
 ```

----------------------------------------------------------------------------------
###  Corrigi falha no Libdvd-pkg: `apt-get check` 

Para corrigi  execute o seguinte comomandos  : 

``` 
   sudo dpkg-reconfigure libdvd-pkg
 ```

ou através desde  comando  :

``` 
   sudo dpkg --configure -a
 ```

  seguido por :

``` 
   sudo apt-get clean
 ```

 ou pelo a comando :

``` 
   sudo apt-get install -f
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
### Verificar  espeficiaçãoes sobre a memoria ram 

 ``` 
     dmidecode --type 17|less
```

----------------------------------------------------------------------------------
### Desativar inicialização automática do Docker na inicialização

Para os usuários com o Ubuntu 15.04+ (onde o SO usa systemd ), de acordo com o doc na inicialização pode ser desativada por:

 ``` 
     sudo systemctl disable docker
```
Nos sistemas desde o Ubuntu 16.04+ (onde o SO usa systemd), de acordo com o documento , a inicialização automática na inicialização pode ser desativada por:

``` 
   sudo systemctl disable docker.service
   sudo systemctl disable docker.socket
 ```

Iniciar o serviço do Docker

 ``` 
   sudo systemctl start docker 
 ```
Para parar o serviço do Docker

 ``` 
   sudo systemctl stop docker
 ```

 Verificar o status do serviço do Docker 

 ``` 
   sudo systemctl status docker
 ```
 Suba os containers do Docker

  ``` 
    docker-compose up -d
  ```
 Parar o containers 

  ``` 
    docker-compose down
  ```
  ou 
  ``` 
   docker stop $(docker ps -aq)
  ```
