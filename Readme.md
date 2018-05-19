# Utilisation de Bose Quietcomfort 35 sous ubuntu 17.10

## paquets nécessaires

    sudo apt-get update && sudo apt install blueman
## fichiers à modifier

    sudo nano /etc/bluetooth/audio.conf
remplacer le contenu avec :
``` [General]
Disable=Socket
Disable=Headset
Enable=Media,Source,Sink,Gateway
AutoConnect=true
load-module module-switch-on-connect
```

    sudo nano /etc/bluetooth/main.conf
  remplacer
  ```
    ControllerMode = dual
    par
  ControllerMode = bedr
      !!rien d'autre n est a modifier!!
```
redémarrer le service bluetooth :

>  sudo service bluetooth restart

aller dans parametres > son > sortie > cliquer sur profil et choisir :
lecteur haute fidelite .....

Normalement le bose  Quietcomfort 35 devrait marcher (mais pas les appels)

