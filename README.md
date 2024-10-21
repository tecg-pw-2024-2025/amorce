# L’amorce

Un cahier des charges pour l’amorce.

L’objectif de l’application est de centraliser un ensemble d’actions et d’informations concernées par l’activité de l’amorce. 

## Les fonds

L’amorce dispose d’un compte en banque. Elle accepte des versements d’argent sur le compte ou en direct à ses bénévoles. Cet argent se retrouve réparti dans des fonds.

Deux de ces fonds sont permanents :

- le *fonds général* est une cagnotte qui sert à financer des projets soumis par des individus ou des associations ;
- le *fonds de fonctionnement* est destiné à permettre la couverture des frais de fonctionnement de l’amorce.

Les autres fonds sont des *fonds spécifiques*. Ils sont destinés à jouer un peu un rôle de banque pour des personnes ou des organisations qui n’ont pas d’accès au système bancaire. Ces fonds spécifiques peuvent reverser un pourcentage de leurs rentrées au *fonds général*, en remerciement du service rendu.

Étant donné la diversité de moyens de versement et la multiplicité des fonds, il est important pour l’amorce de pouvoir disposer d’une vue unifiée sur les comptes. Pour le moment, cette vue est possible via des fichiers Excel, mais c’est assez malcommode à manipuler. Une application pourrait aider en proposant une vue sur un état du compte et des fonds, ainsi qu’une historicisation des mouvements. Naturellement, cette application devrait permettre l’encodage des mouvements, et pas seulement leur visualisation. L’encodage pourra se faire tant manuellement que via une procédure automatisée (ajout périodique des mouvements récupérés en CSV auprès de l’organisme bancaire).

## La détente

De manière périodique, un groupe de 9 personnes et/ou associations tirées au sort est appelé à participer à la « détente », un événement dont la finalité principale est de déterminer comment l’argent du fonds principal va être attribué aux différents projets.

Pour être éligible à ce tirage au sort, il faut :

- soit avoir été donateur récurrent durant les trois derniers mois ;
- soit être un projet ayant déjà été soutenu financièrement par l’amorce dans le passé.

Une application serait utile ici pour aider à la sélection des membres (sélection des personnes et projets éligibles, tirage au sort, détermination de la date de la rencontre).

Chaque détente est l’occasion d’un renouvellement partiel du groupe des 9, par ajout de trois nouveaux et départ des trois plus anciens. Un membre participe donc potentiellement à trois détentes consécutives. Une fois sorti de la détente, un membre ne pourra plus être tiré au sort avant au moins un an.

![« Escalier » de renouvellement des détentes](https://github.com/user-attachments/assets/9198d778-bff7-4faf-b3cc-fcfd0a86be47)

## Fonctionnement au quotidien

En tant qu’association, l’amorce se réunit régulièrement, tous les deuxièmes lundi du mois, pour évoquer son ordre du jour, prendre un ensemble de décisions liées à son fonctionnement, bref, faire fonctionner l’amorce. Chacune de ces réunions est complétée par la rédaction d’un compte rendu. Ce document essentiel, ainsi que d’autres impliqués par diverses actions de l’amorce, doit pouvoir être archivé dans l’application. Naturellement, chaque archivage doit s’accompagner de meta-données (à quelle occasion ? par qui ? pour quoi ?). Les documents devraient par ailleurs pouvoir être accessibles depuis les sections de l’application directement concernées (un compte rendu de réunion depuis une réunion dans l'agenda par exemple). 

Un agenda pourrait être une fonctionnalité intéressante, ainsi qu’une todo-list, mais ce ne sont pas les premières fonctionnalités à considérer. 

L’application pourrait aussi permettre de retrouver les coordonnées des personnes/organisations concernées par le fonctionnement. L’idée est celle d’un carnet d’adresses. Mais attention, il faut éviter de trop historiciser dans ce dernier les activités des personnes. Rien ne devrait permettre de mettre en lien des dons et des personnes, par exemple.

L’amorce doit occasionnellement contacter une liste de personnes abonnées. Une fonctionnalité d’envoi d’e-mails est donc à prévoir dans l’application, ce qui inclut de prévoir la gestion de groupes de destinataires, et la composition éventuelle des e-mails à envoyer.

## Valeurs et respect de la vie privée

Les valeurs de l’amorce favorisent une approche technologique responsable et interopérable avec notamment des choix de formats éditables, non propriétaires, connus pour leur versatilité et leur flexibilité. Ainsi, le format CommonMark (une standardisation du format Markdown) sera privilégié pour la mise au point des mailings et les formatages de contenus et de documents au sein de l’application, et le format CSV sera privilégié pour les échanges de données.

Parmi les valeurs de l’amorce, on trouvera aussi la volonté forte de ne pas garder de trace nominative de certaines informations sensibles. Ainsi, il ne faudra jamais permettre de pouvoir reconstruire les informations d’un virement. Certes, le comptable a cette information, mais l’encodage dans l’application doit séparer les informations liées à la personne de celles liées au mouvement d’argent. En gros, on doit savoir qu’une certaine somme a été versée, pouvoir l’attribuer à un fonds, mais on ne doit pas pouvoir retrouver de qui ça vient. D’un autre côté, on doit savoir, notamment pour la détermination de l’éligibilité d’une personne au processus de détente, qui a versé de l’argent au cours des trois derniers mois, mais sans pouvoir aller plus loin dans la description des virements réalisés par exemple.
