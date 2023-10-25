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
  
    - HELO/EHLO: initiates the start of the SMTP session and identifies the sender-SMTP to the receiver-SMTP
    - MAIL FROM: specifies the email address of the sender
    - RCPT TO: specifies the email address of the recipient
    - DATA: initiates the transfer of the message content
    - QUIT: ends the SMTP session


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
  
    - USER: specifies the mailbox username
    - PASS: specifies the mailbox password
    - STAT: returns the number and total size of all messages
    - LIST: returns the message number and size of each message
    - RETR: retrieves a selected message
    - DELE: deletes a selected message
    - RSET: resets the mailbox, undeleting deleted messages
    - TOP: retrieves the headers and a specified number of lines of a selected message
    - QUIT: ends the POP3 session


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
  
    - SELECT: selects a mailbox for subsequent message searching, retrieval, and manipulation
    - EXAMINE: selects a mailbox for subsequent message searching and retrieval, but not for message manipulation
    - CREATE: creates a new mailbox with the specified name
    - DELETE: deletes the mailbox with the specified name
    - RENAME: renames the mailbox with the specified name
    - SUBSCRIBE: adds the specified mailbox name to the server's set of "active" or "subscribed" mailboxes
    - UNSUBSCRIBE: removes the specified mailbox name from the server's set of "active" or "subscribed" mailboxes
    - LIST: returns a list of mailboxes that match the specified pattern
    - STATUS: returns the status of the specified mailbox
    - FETCH: retrieves the specified message(s) from the mailbox
    - STORE: alters the flags associated with the specified message(s)
    - SEARCH: searches the mailbox for messages that match the specified criteria
    - UID: prefixes a command with the unique identifier (UID) of a message, rather than its sequence number


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
  
    - SSH_MSG_DISCONNECT: disconnects the client from the server
    - SSH_MSG_IGNORE: ignores the message
    - SSH_MSG_UNIMPLEMENTED: indicates that the requested message is not implemented
    - SSH_MSG_DEBUG: sends a debug message to the client
    - SSH_MSG_SERVICE_REQUEST: requests a service from the server
    - SSH_MSG_SERVICE_ACCEPT: accepts a service request from the client
    - SSH_MSG_KEXINIT: initiates the key exchange process
    - SSH_MSG_NEWKEYS: indicates that new keys will be used for encryption
    - SSH_MSG_USERAUTH_REQUEST: requests user authentication
    - SSH_MSG_USERAUTH_FAILURE: indicates that user authentication has failed
    - SSH_MSG_USERAUTH_SUCCESS: indicates that user authentication has succeeded
    - SSH_MSG_CHANNEL_OPEN: opens a new channel for communication
    - SSH_MSG_CHANNEL_OPEN_CONFIRMATION: confirms the opening of a new channel
    - SSH_MSG_CHANNEL_OPEN_FAILURE: indicates that the opening of a new channel has failed
    - SSH_MSG_CHANNEL_DATA: sends data over an open channel
    - SSH_MSG_CHANNEL_EOF: indicates that no more data will be sent over an open channel
    - SSH_MSG_CHANNEL_CLOSE: closes an open channel


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
  
    - GET: requests a representation of the specified resource
    - POST: submits an entity to the specified resource, often causing a change in state or side effects on the server
    - PUT: replaces the specified resource with the request payload
    - DELETE: deletes the specified resource
    - HEAD: requests a response identical to a GET request, but without the response body
    - OPTIONS: describes the communication options for the target resource
    - CONNECT: establishes a network connection to a resource
    - TRACE: performs a message loop-back test along the path to the target resource
