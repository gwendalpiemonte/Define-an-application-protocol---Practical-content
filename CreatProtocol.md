# Définir son propre protocole d'application

Dans cette section, vous définirez votre propre protocole d'application en fonction d'un contexte donné.

### Le contexte:

Vous travaillez pour une entreprise qui souhaite créer un nouveau protocole d'application pour sa nouvelle application. 

Cette application sera utilisée pour envoyer des messages texte entre utilisateurs.

Les utilisateurs utilisent un client pour interagir avec le serveur.

Le serveur s'exécute sur un port spécifique (1234). 

Les clients se connectent au serveur. 

Le serveur ne peut accepter qu'un nombre limité de connexions (5). 

Le serveur peut refuser une connexion s'il est déjà plein.

Une fois connectés, les utilisateurs peuvent envoyer des messages texte à d'autres utilisateurs.

Le serveur accepte les messages texte du client et les envoie au destinataire.

Le serveur ne peut accepter que les messages texte des utilisateurs connectés. 

Les messages texte ne peuvent avoir qu'une certaine longueur (100 caractères).

### L'exercice:

Il vous est demandé de définir le protocole applicatif qui sera utilisé par les clients et le serveur.

Gardez à l’esprit les points suivants :

- Quel est le but du protocole ?
- Sur quel(s) port(s) le protocole fonctionne-t-il ?
- Sur quel(s) protocole(s) le protocole fonctionne-t-il ?
- Qui initie la connexion ?
- Quels sont les messages/actions disponibles ?
- Quel est le format des messages/actions ?
 - Existe-t-il des cas limites ou des cas d'erreur ? Que se passe-t-il dans ces cas ?

## Reponse à l'exercice

### Quel est le but du protocole ?
Le but de ce protocole est d'échanger des messages texte entre utilisateurs avec une architecture client-serveur.
Il permet aux utilisateurs de se connecter à un serveur et d'envoyer des messages texte à d'autres utilisateurs connectés et de recevoir des messages d'autres utilisateurs.

### Sur quel(s) port(s) le protocole fonctionne-t-il ?
Le protocole utilise le port 1234.

### Sur quel(s) protocole(s) le protocole fonctionne-t-il ?
Le protocole utilise le protocole TCP (Transmission Control Protocol)

### Qui initie la connexion ?
Les clients (ici les gens de l'entreprise) initie la connexion TCP en se connectant au serveur par le port 1234.

### Quels sont les messages/actions disponibles ?
Connexion au serveur   : les clients établissent une connexion au serveur.
Envoyer un message     : les utilisateurs connectés peuvent envoyer des messages à d'autres utilisateurs connectés.
Recevoir un message    : les utilisateurs peuvent recevoir des messages qui leur sont envoyés.
Deconnexion au serveur : les clients finissent la connexion au serveur.

### Quel est le format des messages/actions ?
Demande de connexion:
- Format :  `CONNECT <username>`

Réponse à la demande de connexion:
- Acceptée
  - Format : `ACCEPTED`

- Refusée
  - Format : `REFUSED <error>`

Envoyer un message:
- Format :  `SEND <contact_username> <message>`

Réponse à l'envoie du message:
- Acceptée
  - Format : `DELIVERED <contact_username>`

- Refusée
  - Format : `UNDELIVERED  <error>`

Deconnexion:
- Format :  `DISCONNECT`

Réponse à la deconnexion:
- Format :  `DISCONNECTED` 

### Existe-t-il des cas limites ou des cas d'erreur ? Que se passe-t-il dans ces cas ?
Connexion refusée: 
Si le serveur a atteint sa limite de 5 connexions en même temps.
Le serveur va refuser toute tentative de connexion  jusqu'à ce qu'un emplacement soit disponible. 
Si le serveur est plein le client qui essaie de se connecter va être informé que le serveur est plein.

Limite de longueur du message: 
Si un utilisateur envoie un message plus grand que la limite fixée (100 caractères).   
le serveur ne va pas accepter le message et en informer l'expéditeur.

Utilisateur ou destinataire inéxistant: 
Si un client essaie d'envoyer un message à un utilisateur qui n'est pas connecté ou si le nom du destinataire n'est pas reconnu.
Le serveur doit traiter cela comme une erreur et en informer l'expéditeur.

### Diagramme de séquence

<img src="https://github.com/gwendalpiemonte/Define-an-application-protocol-Practical-content/blob/main/DAI.png" width="300"/>

