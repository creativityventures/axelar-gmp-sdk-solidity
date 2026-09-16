# 3. Gateway et validation des preuves

La gateway reçoit les commandes et vérifie qu’elles sont autorisées avant l’exécution. Dans l’ancienne interface, `validateContractCall` et `validateContractCallAndMint` consomment un identifiant de commande, la source, l’expéditeur et le hash du payload. Le contrat destinataire ne doit considérer le message comme authentique qu’après ce contrôle.

La gateway Amplifier suit une logique de preuve pondérée. `AxelarAmplifierGateway.validateProof` vérifie la preuve, la version des signataires et l’état courant de l’autorité. Les types de preuve sont regroupés dans `AmplifierGatewayTypes.sol`.

Cette frontière est essentielle : l’exécution métier ne remplace pas la validation du message. Les domaines, l’adresse source et le hash du payload forment une liaison cryptographique ; modifier l’un de ces champs change le message validé.

Les limites incluent la rotation des signataires, la disponibilité des gateways, la gestion des commandes déjà consommées et les différences entre les chemins legacy et Amplifier.

[Chapitre suivant : tokens, gas et exécution express](./04-tokens-gas-express.md)
