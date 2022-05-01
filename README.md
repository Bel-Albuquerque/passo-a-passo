# passo-a-passo

## instalação de Java

```
 sudo echo "deb http://ppa.launchpad.net/linuxuprising/java/ubuntu bionic main" | tee /etc/apt/sources.list.d/linuxuprising-java.list
 sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 73C3DB2A
 sudo apt-get update
 sudo apt-get install oracle-java11-installer
 exit
```

Definir o Oracle Java 11 como padrão, caso você já tenha alguma instalação do Java:

```
 sudo apt install oracle-java11-set-default
```

Para verificar a versão do Java instalada, execute o comando abaixo:
```
 java -version
```

Para verificar a versão do compilador Java:
```
 javac -version
```
Caso queira desinstalar o Oracle Java 11 no Ubuntu, Linux Mint ou Debian, execute o comando abaixo:

```
 sudo apt remove oracle-java11-set-default
```

Instalando o Eclipse em ambiente Linux:
 - Faça o download do [Eclipse IDE for Enterprise Java and Web Developers](https://www.eclipse.org/downloads/packages/release/2021-03/r/eclipse-ide-enterprise-java-and-web-developers).
 - Extraia os arquivos em um diretŕio da sua preferência.
 - Agora precisamos adicionar o eclipse ao Launcher do Ubuntu:
     - Crie um arquivo Eclipse.desktop em ~/.local/share/applications
```
touch ~/.local/share/applications/Eclipse.desktop
```
 - Abra-o com seu editor de texto:
```
gedit ~/.local/share/applications/Eclipse.desktop
```
 - Agora adicione as seguintes linhas no arquivo:
     - Atenção para os caminhos de cada arquivo, porque isso pode mudar de acordo com o local que você extraiu o eclipse!
```
[Desktop Entry]
Comment=Eclipse
Terminal=false
Name=Eclipse
Exec=/home/usuario/Downloads/eclipse-jee-2021-03-R-linux-gtk-x86_64/eclipse/eclipse
Type=Application
Icon=/home/usuario/Downloads/eclipse-jee-2021-03-R-linux-gtk-x86_64/eclipse/icon.xpm
StartupWMClass=Eclipse
```

 - Agora feche e salve o arquivo, e no terminal digite o seginte comando, para poder tornar o arquivo executavel:
```
chmod a+x ~/.local/share/applications/Eclipse.desktop
```
