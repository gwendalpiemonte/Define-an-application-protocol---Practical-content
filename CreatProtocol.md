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

### Sur quel(s) port(s) le protocole fonctionne-t-il ?
Le protocole utilise le port 1234.

### Sur quel(s) protocole(s) le protocole fonctionne-t-il ?
Le protocole utilise le protocole TCP (Transmission Control Protocol)

### Qui initie la connexion ?
Les clients (ici les gens de l'entreprise) 


### Quels sont les messages/actions disponibles ?

### Quel est le format des messages/actions ?

### Existe-t-il des cas limites ou des cas d'erreur ? Que se passe-t-il dans ces cas ?



