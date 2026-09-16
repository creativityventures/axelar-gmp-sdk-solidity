# 5. Gouvernance, upgrades et limites

Les contrats de gouvernance inter-chaînes permettent de proposer puis d’exécuter des actions sur des opérateurs ou des contrats. `InterchainGovernance`, `InterchainMultisig` et `AxelarServiceGovernance` séparent la proposition, la preuve et l’exécution, avec des rôles qui doivent rester explicitement bornés.

Les proxies et `Upgradable` rendent possible une évolution contrôlée du code. Cette souplesse implique de documenter l’admin, l’implémentation courante, la procédure de changement et les délais ; une adresse de proxy ne suffit pas à établir le comportement final.

Périmètre : lecture statique des contrats, interfaces, README et tests présents dans l’amont. Aucune installation, compilation, exécution de test ni déploiement n’a été effectué. Les tests du dépôt servent de référence aux lecteurs qui veulent reproduire les scénarios séparément ; ce parcours ne constitue pas un audit.

[Retour au sommaire](./README.md)
