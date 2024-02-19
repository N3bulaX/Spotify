# Spotify
Introducción

para personalizar el oficial de Spotify cliente.
Instalación
Windows

si la instalacion da error al ejecutar como administrador darle ¨N¨ en  la primera opcion despues ¨Y¨ y se intalara corectamnete 

recordar todo esto desde la version de spotify launcher ( https://www.spotify.com/us/download )no la de microsft una ves todo echo distrutar de spotify sin anuncios y customs

```
iwr -useb https://raw.githubusercontent.com/spicetify/spicetify-cli/master/install.ps1 | iex
```

Este es el método de instalación se recomienda para la mayoría de los usuarios. Es la forma más rápida y segura para instalar Spicetify.
Powershell (binario precompilado) ejecutar como administrador

También ejecute el siguiente si desea instalar el Spicetify Mercado , que le da acceso a una ficha en Spotify de la barra lateral que permite buscar e instalar temas , extensiones , y fragmentos si al ejecutar el primer comando le diste no en la primera opcion no tendras que ejecutar el siguiente comando ya se habra instalado la tienda y no tendras que ejecutar la siguiente linea.

```
iwr -useb https://raw.githubusercontent.com/spicetify/spicetify-marketplace/main/resources/install.ps1 | iex
```

Powershell(admin)

```
Powershell como(admin)
```
![image](https://github.com/N3bulaX/Spotify/assets/117851699/19883eb6-af35-4f43-bca2-154f26a44a8a)

```
run
```
![image](https://github.com/N3bulaX/Spotify/assets/117851699/7a5ef2c1-69ee-443f-aa14-97047568c8a7)

```
Una ves echo todo para tener spotify sin auncion te iras a la seccion de Marketplace
```
![image](https://github.com/N3bulaX/Spotify/assets/117851699/65ee814e-1c8f-4f44-befa-7aed10ef9a03)


```
Una ves ahi buscar la siguiente extencion le das descargar y  reiniciar, listo disfruta  
```
![Captura de pantalla 2024-02-19 232830](https://github.com/N3bulaX/Spotify/assets/117851699/779cb288-5f4c-4b61-b2d4-47de22906ba4)


Linux y MacOS
Shell (binario precompilado) - Recomendado

curl -fsSL https://raw.githubusercontent.com/spicetify/spicetify-cli/master/install.sh | sh

Homebrew o LinuxBrew

brew install spicetify/homebrew-tap/spicetify-cli

En macOS, será necesario establecer spotify_path a /Applications/Spotify.app/Contents/Resources en el ~/.config/spicetify/config-xpui.ini archivo de configuración.
AUR

yay -S spicetify-cli

Nota para los usuarios de Linux
Spotify instalado desde AUR

Antes de aplicar Spicetify, usted necesita tener permiso de escritura en Spotify archivos, ejecutando el comando:

sudo chmod a+wr /opt/spotify
sudo chmod a+wr /opt/spotify/Apps -R

Nota: Tu Spotify ubicación del cliente puede ser diferente.
Spotify instalado a través de spotify-launcher paquete (Arch Linux)

Si Spotify es instalado a través de la spotify-launcher paquete, a continuación, Spotify no instalar a /opt/spotify es, en cambio, en esta carpeta: ~/.local/share/spotify-launcher/install/usr/share/spotify/

Este directorio deberá ser agregado a la spotify-path la sección de la configuración (y usted no tendrá que cambiar los permisos como el AUR método).
Spotify instalado de Snap

Las aplicaciones que se instalaron a partir de Complemento no puede ser modificado por lo que necesita para seguir estos pasos para obtener Spicetify de trabajo:

    Desinstalar de Spotify en el Snap o ejecutar el comando snap remove spotify
    Instalar Spotify utilizando apt: 

curl -sS https://download.spotify.com/debian/pubkey_7A3A762FAFD4A51F.gpg  | sudo apt-key add -
echo "deb http://repository.spotify.com stable non-free" | sudo tee /etc/apt/sources.list.d/spotify.list
sudo apt-get update && sudo apt-get install spotify-client

    Después de Spotify está instalado con éxito, usted necesita para obtener leer permisos de escritura en Spotify archivos, mediante la ejecución de comandos: 

sudo chmod a+wr /usr/share/spotify
sudo chmod a+wr /usr/share/spotify/Apps -R

Nota: Tu Spotify ubicación del cliente puede ser diferente.
Spotify instalado desde Flatpak

    Usted necesita encontrar donde Flatpak tiendas de su cliente de Spotify. En Manjaro, es almacenado en: 

/var/lib/flatpak/app/com.spotify.Client/x86_64/stable/active/files/extra/share/spotify/

    El tuyo puede ser diferente, intente estos pasos: 

    Encontrar flatpak el lugar de instalación con el comando: flatpak --installations
    Ir a ese directorio y cavar hasta encontrar la carpeta que contiene artículos como estos: 

flat2

Después de Spotify ubicación, conjunto spotify_path en el archivo de configuración para que el directorio:

flat2

    Encontrar su prefsarchivo: Podría ser cualquiera de estos dos lugares: 

    ~/.config/spotify/prefs
    ~/.var/app/com.spotify.Client/config/spotify/prefs

Compruebe tanto, ampliar el derecho a la ruta de acceso absoluta y configurarlo para que prefs_path en el archivo de configuración.

spicetify config prefs_path ~/.var/app/com.spotify.Client/config/spotify/prefs

    Finalmente, en el terminal, establecer permisos de lectura/escritura para que: 

sudo chmod a+wr /var/lib/flatpak/app/com.spotify.Client/x86_64/stable/active/files/extra/share/spotify
sudo chmod a+wr -R /var/lib/flatpak/app/com.spotify.Client/x86_64/stable/active/files/extra/share/spotify/Apps

Instalaciones Heredadas

Si, por alguna razón, usted no está utilizando la mayoría hasta la fecha de Spotify cliente, puede que tenga que instalar una versión específica de Spicetify. Esto no es recomendable ya que nuestro enfoque principal será siempre la última versión de Spotify.

Como tal, usted tendrá que ejecutar cualquiera de los siguientes comandos con la versión deseada. Si desea utilizar el antiguo Spotify cliente v1.1.56 o más, usted tiene que instalar spicetify v1.2.1.

Windows : En powershell

$v="1.2.1"; Invoke-WebRequest -UseBasicParsing "https://raw.githubusercontent.com/spicetify/spicetify-cli/master/install.ps1" | Invoke-Expression

Linux/MacOS: En bash

curl -fsSL https://raw.githubusercontent.com/spicetify/spicetify-cli/master/install.sh -o /tmp/install.sh
sh /tmp/install.sh 1.2.1

