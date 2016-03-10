![Logo Vagrant](https://github.com/IT-2015/Vagrant/blob/master/logo_vagrant.png)

#[Vagrant](https://www.vagrantup.com/)

## C'est quoi ?

Vagrant est un logiciel libre et open-source pour la création et la configuration des environnements de développement virtuel. Il peut être considéré comme un wrapper autour du logiciel de virtualisation comme VirtualBox.

## Comment l'utiliser ?

1. [Télécharger Vagrant](https://www.vagrantup.com/downloads.html)
2. Installation de Vagrant
3. Télécharger un Provider ([VirtualBox](https://www.virtualbox.org/), [VMWare](http://www.vmware.com/), ...)
4. Installation du Provider, chez IT c'est VirtualBox.
5. Prét à l'emploi

Vagrant s'utilise via des lignes de commandes, soyez sûr après l'installation que la commande vagrant soit reconnu par votre terminal.

Pour cela dans votre terminal :
```term
vagrant -v
```

Si la commande n'est pas reconnu, sous Windows :

> Allez dans Système > Paramètres système avancés > (BTN) Variables d'environnement...

Modifier la valeur du PATH en rajoutant le chemin de Vagrant [path]\Vagrant\bin;

(path étant le chemin ou vous avez installer Vagrant sur votre poste)

Une fois que l'outil est utilisable dans le terminal 2 choix d'installation d'une box se propose.

## 1. Installation à partir d'une Box existante
Pour installer depuis une box existante et à disposition.

Copier coller le fichier VagrantFile à l'emplacement de votre projet. 

Dans ce fichier VagrantFile modifier la ligne et cibler l'emplacement de votre fichier `.box` : 
`config.vm.box = "devbox"`
`config.vm.box_url = "[PATH]/devbox.box"`

Configurer l'IP de réseaux privé de votre box
`config.vm.network :private_network, ip: "192.168.33.10"`

Configurer le dossier synchronisé entre votre machine physique et votre machine virtuel
`config.vm.synced_folder "./", "/var/www/project"`

## 2. Installation initial
Il n'y a pas besoin VagrantFile.

Choisir une box sur un des sites d'hébergement de box.
 - http://www.vagrantbox.es/
 - https://atlas.hashicorp.com/boxes/search

```term
  vagrant box add {title} {url}
  vagrant init {title}
  vagrant up
```

Modifier {title} par le titre de la box, et l'url par celui donner par le site.

# Commande Utile

`vagrant up` Démarre ou installation une box 

`vagrant halt` Arret de la box du dossier courant

`vagrant global-status` Renseigne sur les status de vos BOX

`vagrant halt ID` Arret de la box avec l'ID

`vagrant destroy` Destruction de la box du dossier courant

`vagrant destroy ID` Destruction de la box avec l'ID

`vagrant ssh` Connection en SSH à la box du dossier courant

# Autre solution


#![Logo-puphpet](https://github.com/IT-2015/Vagrant/blob/master/logo-puphpet.png) [PUPHPET](https://puphpet.com/) 

