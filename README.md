## <u>Nom du groupe :</u> Echec
### <u>Membres du groupe :</u> Mathis Tourier Thomas Rolland Lucas Bouchet Lucas Bruyere

_________________________

## <u>Configuration de base :</u>

<u>Configuration Container Terraform :</u>


| <u>Élements</u>        | <u>Caractéristiques</u>
| ------------- |:--------------:|
ID              |203
OS              |Debian
Processeur      |2 
Coeur           |2
Mémoire         |1Go 
Disque          |8Go 
Nom d'hôte      |echec-terraform
Domaine DNS     |final.cfai24.ajformation.fr


<u>Adresses IP :</u> 
* Container : 2a03:5840:111:1024:aaaa:bbbb:cccc:0001
* Instance BDD : 2a03:5840:111:1024:aaaa:bbbb:cccc:0002
* Vitrine instance : 2a03:5840:111:1024:aaaa:bbbb:cccc:0003
* Gestion instance : 2a03:5840:111:1024:aaaa:bbbb:cccc:0004

<u>Comptes utilisateurs :</u>


| <u>Utilisateur</u>        | <u>Mot de passe</u>
| ------------- |:--------------:|
| javond        |   Echec&Mat5       
| mtourier      | ******            
| trolland      | ******         
| lbruyere      | ******     
| lbouchet      | ******    



_________________________
## <u>Sécurité : </u>

Pour la sécurité de nos serveurs nous avons choisis de bloqué l'accès à l'utilisateur root en connexion ssh et les accès des utilisateurs sans leurs clé ssh.
Il faudra donc déjà être connecté avec un utilisateur classique afin de pouvoir se connecté en root. 

Pour ne pas avoir besoin de passer en root pour utiliser sudo (pour l'utilisateur : javond) il faut dans un premier temps executer cette commande : usermod -aG sudo javond

Puis  ajouter cette ligne : javond ALL=(ALL) NOPASSWD: ALL
dans le fichier : sudo visudo
_________________________

## <u>Tests :</u> 

Afin de confirmé que les utilisateur arrivent bien à se connecter à notre machine, nous avons tous testé les connexions & droits de chacun. Nous avons également tester avec Mr Avond s'il arrive bien à se connecté et avoir son accès root. 

Conclusion : Tout les utilisateurs arrivent à se connecter avec les bons droits. 

![alt text](image.png)

Des tests de création / supression de contenaire ont été réalisé, afin de vérifier la fiabilité d'ajout et de supression des contenaires, avec les bons noms et bonnes adresses IP. 

Conclusion : les containers se créent comme il faut, avec les bonnes adresses IP. 


## <u>Création des containers :</u> 

Pour créer un contenaire à partir de notre VM echec-terraform, il suffit de se déplacer dans le fichier /home/echec-user/terraform_project en utilisant la commande suivante : 

cd /home/echec-user/terraform_project

Puis de lancer les commandes suivantes : 

* terraform init
* terraform plan
* terraform apply

_________________________






