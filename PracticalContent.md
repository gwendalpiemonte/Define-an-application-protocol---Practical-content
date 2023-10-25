# Define an application protocol

## Explore existing application protocols

#### Protocole SMTP (Simple Mail Transfer Protocol) :

- **A quoi sert le protocole SMTP ?**   
  Le protocole SMTP sert à envoyer des courriers électroniques. Il est utilisé pour acheminer des e-mails depuis le client de messagerie de l'expéditeur vers le serveur de messagerie du destinataire.

- **Sur quel port fonctionne le protocole SMTP ?**   
  SMTP fonctionne généralement sur le port 25. Cependant, il existe d'autres ports, comme le 587 (SMTP avec authentification) et le 465 (SMTP sécurisé, souvent appelé SMTPS).

- **Sur quel protocole fonctionne le protocole SMTP ?**   
  SMTP fonctionne sur le protocole TCP (Transmission Control Protocol).

- **Qui initie la connexion ?**   
  L'expéditeur (client de messagerie) initie la connexion SMTP en se connectant au serveur de messagerie du destinataire.

- **Quels sont les messages disponibles ?**   
  Les messages SMTP comprennent des commandes comme "EHLO" (pour identifier le client), "MAIL FROM" (pour spécifier l'expéditeur), "RCPT TO" (pour spécifier le destinataire), "DATA" (pour commencer la transmission du message), et d'autres commandes pour la gestion des e-mails.

#### Protocole POP3 (Post Office Protocol version 3) :

- **A quoi sert le protocole POP3 ?**   
  Le protocole POP3 est utilisé pour récupérer des e-mails depuis un serveur de messagerie. Il permet aux utilisateurs de télécharger leurs e-mails depuis le serveur vers leur client de messagerie, en les supprimant généralement du serveur.

- **Sur quel port fonctionne le protocole POP3 ?**   
  POP3 fonctionne généralement sur le port 110. Le port 995 est utilisé pour POP3 sécurisé (POP3S).
 
- **Sur quel protocole fonctionne le protocole POP3 ?**   
  POP3 fonctionne sur le protocole TCP.

- **Qui initie la connexion ?**   
  Le client de messagerie (utilisateur) initie la connexion POP3 en se connectant au serveur de messagerie.

- **Quels sont les messages disponibles ?**   
  Les messages POP3 incluent des commandes telles que "USER" (pour spécifier l'utilisateur), "PASS" (pour fournir le mot de passe), "LIST" (pour lister les e-mails disponibles), "RETR" (pour récupérer un e-mail spécifique), et d'autres commandes pour la gestion des e-mails.

- **Quelle est la différence entre POP3 et SMTP ?**   
  La principale différence entre POP3 et SMTP réside dans leur fonction : POP3 est utilisé pour récupérer les e-mails du serveur vers le client, tandis que SMTP est utilisé pour envoyer des e-mails du client vers le serveur. POP3 supprime généralement les e-mails du serveur après leur récupération, tandis que SMTP est responsable de les transférer vers le serveur de messagerie du destinataire.

#### Protocole IMAP (Internet Message Access Protocol) :

- **A quoi sert le protocole IMAP ?**   
  IMAP est utilisé pour gérer et synchroniser les e-mails sur un serveur de messagerie. Il permet aux utilisateurs de visualiser leurs e-mails sans les télécharger, offrant une meilleure organisation et une expérience de messagerie plus flexible.

- **Sur quel port fonctionne le protocole IMAP ?**   
  IMAP fonctionne généralement sur le port 143. Le port 993 est utilisé pour IMAP sécurisé (IMAPS).

- **Sur quel protocole fonctionne le protocole IMAP ?**   
  IMAP fonctionne sur le protocole TCP.

- **Qui initie la connexion ?**   
  Le client de messagerie (utilisateur) initie la connexion IMAP en se connectant au serveur de messagerie.

- **Quels sont les messages disponibles ?**   
  Les messages IMAP incluent des commandes telles que "LOGIN" (pour s'authentifier), "SELECT" (pour sélectionner une boîte aux lettres), "FETCH" (pour récupérer des e-mails), et d'autres commandes pour gérer les e-mails et les dossiers.

- **Quelle est la différence entre POP3, SMTP et IMAP ?**   
  POP3 est principalement utilisé pour récupérer des e-mails et les supprimer du serveur, SMTP est utilisé pour envoyer des e-mails, tandis qu'IMAP est utilisé pour gérer et synchroniser les e-mails sur le serveur sans les supprimer. IMAP offre une expérience de messagerie plus flexible, permettant un accès à distance aux e-mails et une meilleure organisation.

#### Protocole SSH (Secure Shell) :

- **Quel est le but du protocole SSH ?**   
  SSH est utilisé pour établir des connexions réseau sécurisées et cryptées, notamment pour l'accès à distance aux systèmes et la transfert de données sécurisées.

- **Sur quel port fonctionne le protocole SSH ?**   
  SSH fonctionne généralement sur le port 22.

- **Sur quel protocole fonctionne le protocole SSH ?**   
  SSH fonctionne sur le protocole TCP.

- **Qui initie la connexion ?**   
  Le client SSH initie la connexion au serveur SSH.

- **Quels sont les messages disponibles ?**   
  SSH comprend une série de messages d'initialisation, d'authentification, et de négociation de clés, tels que "SSH_MSG_KEXINIT" (pour l'initialisation de la clé), "SSH_MSG_USERAUTH_REQUEST" (pour l'authentification de l'utilisateur), etc.

- **Comment se déroule l'échange de version ?**   
  L'échange de version SSH se produit lorsque le client et le serveur communiquent pour négocier les versions prises en charge. Cela inclut l'envoi des informations sur les versions de protocole et les algorithmes de chiffrement pris en charge.

#### Protocole HTTP (Hypertext Transfer Protocol) :

- **A quoi sert le protocole HTTP ?**   
  HTTP est utilisé pour transférer des documents hypertextes, tels que des pages Web, sur le World Wide Web.

- **Sur quel port fonctionne le protocole HTTP ?**   
  HTTP fonctionne généralement sur le port 80. Le port 443 est utilisé pour HTTP sécurisé (HTTPS).

- **Sur quel protocole fonctionne le protocole HTTP ?**   
  HTTP fonctionne sur le protocole TCP.

- **Y a-t-il une différence entre HTTP/2 et HTTP/3 ?**   
  Oui, HTTP/2 et HTTP/3 sont des versions améliorées de HTTP. HTTP/2 introduit la multiplexage des flux et une meilleure gestion de la performance, tandis que HTTP/3 utilise le protocole QUIC pour des performances encore meilleures et une communication sécurisée.

- **Qui initie la connexion ?**   
  Le client Web (navigateur) initie la connexion HTTP en envoyant une demande à un serveur Web.

- **Quels sont les messages disponibles ?**   
  Les messages HTTP incluent les requêtes (comme GET, POST) envoyées par le client et les réponses (comme les codes de statut) renvoyées par le serveur pour indiquer le résultat de la demande.
