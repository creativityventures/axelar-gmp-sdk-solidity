# 1. Axelar GMP : rôle et périmètre

Ce dépôt fournit les bibliothèques Solidity et les contrats d’intégration du General Message Passing d’Axelar. Il ne constitue pas à lui seul tout le réseau : il expose les interfaces de gateway, les exécutables, la gouvernance et les briques de déploiement utilisées par les applications.

Le parcours distingue l’émission d’un message, sa validation par une gateway, puis son exécution dans le contrat destinataire. Les contrats d’exemple et les interfaces permettent de suivre ces frontières sans confondre une demande de message avec une preuve de livraison.

Les familles importantes sont `gateway`, `executable`, `express`, `governance`, `upgradable` et `utils`. La licence et les contrôles d’administration doivent être lus au niveau de chaque fichier avant toute réutilisation.

[Chapitre suivant : émission et exécution d’un message](./02-messages-execution.md)
