# Création d'une boite mail partagée

## Identification

Pour créer une boite partagée sur exchange, vous devez vous rendre sur le lien qui vous a été communiqué par email. Il s'agit d'un lien https://remote.domaine.com/ecp/ ou https://webmail.domaine.com/ecp/.

Connectez-vous ensuite avec les identifiants qui vous ont été communiqués, sous la forme domaine\utilisateur, ainsi que son mot de passe. Par exemple : domtest\usertest.

![Interface de connexion à Exchange](<../../../../.gitbook/assets/image (8).png>)

## Création

Une fois connecté, cliquez sur "Boîte aux lettres partagée"

![](../../../../.gitbook/assets/shared\_mbx.png)

Vous arrivez ainsi que la page listant l'ensemble des boîtes partagées existantes.

Cliquez ensuite sur l'icône "+" pour afficher la fenêtre de création de la boîte partagée.

![](../../../../.gitbook/assets/create\_shared.png)

Une nouvelle fenêtre s'ouvre, et vous invite à saisir :

* Le nom d'affichage de la boîte : ce sera ce qui apparaitra dans l'expéditeur de vos emails

![Nom de la boîte partagée](<../../../../.gitbook/assets/image (2).png>)

* L'alias : ce sera l'adresse mail de la boite. Il ne peut y avoir ni accents ni espaces : boite-partagee@domaine.com

![Adresse mail de la boîte partagée](<../../../../.gitbook/assets/image (9).png>)

* L'unité d'organisation : l'endroit, dans l'annuaire, où créer la boite partagée. Il est impératif de créer la boite dans l'unité "Shared Mailboxes" (voir capture ci-dessous), sans quoi, la boite ne fonctionnera pas correctement

![Sélection de l'unité d'organisation](<../../../../.gitbook/assets/image (1).png>)

![Unité d'organisation à choisir](../../../../.gitbook/assets/ad\_schema.png)



* Les utilisateurs : les utilisateurs qui pourront avoir accès à cette boite partagée. En cliquant sur l'icône "+", vous pourrez choisir les personnes qui pourront lire le contenu de la boite partagée.

![Délégation de la boite mail](<../../../../.gitbook/assets/image (6).png>)

Il faut également choisir la base de données qui stockera le contenu des boîtes mail partagées. Cliquez sur "Plus d'options..." pour afficher les options avancées

![Accès aux options avancées](../../../../.gitbook/assets/more\_options.png)

Dans les options avancées, il faut sélectionner la base de données "SHARED\_MBDB\_xx\_xx", par exemple SHARED\_MBDB\_16\_01

![Choix de la base de données](<../../../../.gitbook/assets/image (7).png>)

## Délégation d'envoi

Dans certains cas, il peut arriver que l'utilisateur n'ait pas le droit d'envoyer d'emails depuis la boite partagée.

Dans cette situation, il sera nécessaire de forcer les droits sur la boîte mail pour l'utilisateur en question.

Pour cela, il faut se rendre à nouveau sur "Boîte aux lettres partagée"

![](../../../../.gitbook/assets/shared\_mbx.png)

Faites ensuite un double clic sur la boîte partagée en question, puis cliquez sur "délégation de boîte aux lettres" dans la liste à gauche

![Accès à la délégation des droits](../../../../.gitbook/assets/delegate\_clic.png)

Une fois sur cette page, assurez-vous que dans la liste "Accès total", l'utilisateur apparait bien en dessous de la liste des 3 entrées "Exchange xxx".

![Délégations en accès total](<../../../../.gitbook/assets/image (5).png>)

<mark style="color:red;">Attention : vous ne devez</mark> <mark style="color:red;"></mark><mark style="color:red;">**PAS**</mark> <mark style="color:red;"></mark><mark style="color:red;">supprimer ces 3 entrées, sans risquer de bloquer le fonctionnement de la boîte mail</mark>

Si l'utilisateur en question n'apparait pas dans la liste, cliquez sur l'icone "+", puis sélectionnez le dans la liste des utilisateurs qui apparait.

Assurez-vous également que l'utilisateur apparait bien dans la liste "Envoyer en tant que"

![Délégations en envoi](<../../../../.gitbook/assets/image (3).png>)

Là encore, dans le cas contraire, cliquez sur l'icone "+", puis sélectionnez et ajoutez l'utilisateur. Cliquez ensuite sur "Enregistrer" pour terminer.

Note : les droits sur les boites mail partagées peuvent mettre jusqu'à une heure pour s'activer.
