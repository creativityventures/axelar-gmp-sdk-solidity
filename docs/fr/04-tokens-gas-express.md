# 4. Tokens, gas et exécution express

Le chemin avec token combine message et transfert d’actif. `AxelarExecutableWithToken` et ses interfaces encadrent l’arrivée de l’actif avant l’appel métier. L’application doit vérifier que le token, le montant et la source correspondent à ce qu’elle attend ; un payload valide ne rend pas un token inattendu sûr.

Le service de gas et les types d’estimation représentent le coût nécessaire pour faire avancer un message. La valeur doit être estimée et payée selon le chemin retenu, sans exposer de secret dans les paramètres ou les scripts.

Les exécutables express permettent une livraison anticipée par un tiers avant le règlement normal. Les variantes `AxelarExpressExecutable` et `AxelarValuedExpressExecutable` rendent explicites les notions de valeur, de remboursement et de risque de livraison anticipée.

L’express améliore la latence mais ajoute une surface économique : l’intégrateur doit prévoir les échecs, la réconciliation et les appels répétés.

[Chapitre suivant : gouvernance, upgrades et limites](./05-gouvernance-limites.md)
