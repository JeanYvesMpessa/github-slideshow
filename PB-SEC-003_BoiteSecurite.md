---
title: "PB-SEC-003 BoiteSecurite"
source: "PB-SEC-003_BoiteSecurite.docx"
---

Codification

PB-SEC-003

Entrée en vigueur

Mars 2026

Mise à jour

[Date]

PLAYBOOK

Données, accès et appareils – Triage, analyse et coordination

Boîte Sécurité de l’Information

📋 Alignement cadre :  NIST CSF 2.0 / SP 800-61r3  │  ISO/IEC 27035:2023  │  CIS Controls v8 (Contrôle 17)

1. Positionnement et particularités de cette famille

Pour cette famille, la Boîte Sécurité est le centre névralgique de l’évaluation de l’impact réel et de la qualification Loi 25. La majorité des incidents sont découverts après coup — la reconstitution de la chronologie et l’identification précise des données impactées sont des actions prioritaires.

⏰ Délai de qualification :  Tout signalement doit être qualifié (type de données impliquées, PRP présentes ou non) dans un délai maximal de 2 h. Cette qualification conditionne l’obligation de déclaration à la CAI.

2. Analyse initiale du signalement

Étape

Vérification

Outil / Méthode

1

Confirmer le type d’incident et le vecteur

Description utilisateur, alertes DLP/IDS, journaux d’accès

2

Identifier la nature et le volume des données

Inventaire des actifs, classification des données, journaux de transfert

3

Déterminer si des PRP sont impliquées

Registre des traitements, cartographie des données, RPRP si nécessaire

4

Reconstituer la chronologie

Journaux système, journaux d’authentification, alertes DLP

5

Identifier le(s) compte(s) impliqué(s)

Journaux d’authentification, Active Directory, gestion des identités

6

Classifier selon niveaux GMVI

Grille DIR-SEC-001 — en cas de doute, niveau supérieur

3. Procédures de réponse par vecteur

3.1 Fuite ou exfiltration de données

1

Qualifier précisément l’étendue

Volume, nature, destinataire(s). PRP impliquées?

2

Conserver les preuves

Journaux DLP, logs de transfert, alertes. Ne rien effacer.

3

Contenir si possible

Révoquer accès au canal de fuite si encore actif. Bloquer le partage externe.

4

Évaluation Loi 25

PRP identifiées? Alerter immédiatement le CSIO et le RPRP. Documenter les catégories de données.

5

Notifier le COMSI

Briéfing SAR. COMSI déclare au ROCD si N2+.

3.2 Accès non autorisé et compte compromis

1

Révoquer les accès actifs

Toutes sessions du compte concerné. Compte admin : suspension immédiate.

2

Forensique du compte

Journaux d’authentification, historique des actions, méthode de compromission initiale.

3

Analyser le rayon de blast

Quels systèmes le compte a-t-il accédé? Quelles données ont été consultées ou exfiltrées?

4

Réinitialisation sécurisée

Nouveau mot de passe fort + MFA oblig. Après forensique terminée.

5

Notifier le COMSI

COMSI déclare au ROCD si N2+.

3.3 Destruction ou altération malveillante de données

🔴 PRIORITÉ :  Ne pas tenter de restaurer avant l’analyse forensique. La restauration écrase les preuves.

1

Préserver les preuves

Ne pas lancer de restauration. Identifier l’étendue de la destruction/altération.

2

Forensique

Journaux système, journaux d’accès, événements Windows/Linux, actions du compte impliqué.

3

Évaluer les sauvegardes

Quelle est la dernière sauvegarde saine? Impact sur les opérations?

4

Planifier la restauration

Avec le COMSI : décision sur le timing de restauration pour ne pas compromettre les preuves.

3.4 Intrusion réseau

1

Confirmer et étendre l’isolation du segment

Valider avec Svc Bureautique. Identifier le périmètre exact.

2

Analyse du trafic réseau

Logs IDS/IPS, pare-feu, NetFlow. Identifier les IPs sources, destinations, protocoles.

3

Corréler avec les journaux d’authentification

Des comptes ont-ils été utilisés lors de l’intrusion?

4

Notifier le COMSI

COMSI déclare au ROCD (N2+). Formulaire MVI si N3.

3.5 Appareil perdu ou volé

1

Confirmer le statut MDM et chiffrement

Appareil inscrit? Chiffrement actif? BitLocker, FileVault?

2

Exécuter l’effacement MDM si requis

Sur confirmation avec le COMSI si données sensibles présentes.

3

Révoquer les accès de l’appareil

Certificats, jetons, sessions actives.

4

Qualifier les données présentes

Inventaire des données sur l’appareil. PRP impliquées? Niveau GMVI?

4. Processus d’évaluation Loi 25 — étape par étape

Étape

Action requise

1. Identifier les PRP

Des renseignements personnels ont-ils été accédés, divulgués, copiés ou volés?

2. Évaluer le préjudice

L’atteinte est-elle susceptible de causer un préjudice sérieux?

3. Alerter le CSIO et le RPRP

Immédiatement dès la qualification.

4. Déclaration CAI

Si préjudice sérieux : déclarer à la CAI SANS DÉLAI (Loi 25, art. 63.8 à 63.11).

5. Notifier les personnes concernées

Si préjudice sérieux : notifier sans délai.

6. Registre des atteintes

Consigner dans le registre tenu par le RPRP, même si pas de déclaration CAI.

5. Collecte de preuves — Chaîne de custody

Type de preuve

Méthode de collecte

Conservation

Journaux d’accès / auth

Export horodaté signé avec hash

Min. 2 ans

Journaux DLP

Export complet avec métadonnées

Min. 2 ans

Logs réseau IDS/IPS

Export brut horodaté

Corrélé au dossier

Journaux Active Directory

Export événements sécurité (ID 4624, 4625, 4720...)

Min. 2 ans

Captures écran d’alertes

Horodatées

Archivées avec le dossier

Rapports MDM (appareil perdu)

Export de l’historique de localisation et d’effacement

Archivé avec le dossier

6. Notifications internes et gouvernementales

Destinataire

Niveau GMVI

Délai

Canal

Service Bureautique

1 et +

&lt; 1 h

Courriel

COMSI

1 et +

&lt; 2 h (N2+ : &lt; 30 min)

Courriel + tél.

CSIO

2 et +

&lt; 1 h

Via COMSI

RPRP

Dès PRP identifiées

&lt; 2 h

Courriel + appel

ROCD — via COMSI

2 et +

Sans délai

COMSI déclare

CAI (Loi 25)

Dès préjudice sérieux confirmé

Sans délai

CSIO + RPRP

Approbation

Fonction

Nom

Signature

Date

[Titre]

[Prénom Nom]

📎 Documents connexes :  POL-SEC-001  |  DIR-SEC-001  |  PROC-SEC-003  |  PB-BUR-003  |  PB-COMSI-003  |  Loi 25
