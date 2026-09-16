# 2. Émission et exécution d’un message

Les interfaces `IAxelarGateway` et `IAxelarGatewayWithToken` exposent `callContract` et `callContractWithToken`. L’appel indique la chaîne et l’adresse de destination, ainsi que le payload ; la variante avec token ajoute l’actif et le montant à remettre.

Un contrat applicatif hérite généralement d’un exécutable Axelar. La fonction publique `execute` reçoit les éléments du message et délègue à une implémentation interne, après le contrôle de l’appelant et de l’identifiant de commande. Pour les tokens, `executeWithToken` ajoute les contraintes de l’actif et de la quantité.

Le payload doit être conçu comme une entrée hostile : le destinataire doit décoder strictement les paramètres attendus, vérifier les valeurs métier et éviter de confondre l’expéditeur cross-chain avec un appelant local.

Les contrats centraux à suivre sont `contracts/executable/AxelarExecutable.sol` et les interfaces correspondantes.

[Chapitre suivant : validation cryptographique et gateway](./03-gateway-preuves.md)
