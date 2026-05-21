---
title: "PB-BUR-003 ServiceBureautique"
source: "PB-BUR-003_ServiceBureautique.docx"
---

Codification

PB-BUR-003

Entrée en vigueur

Mars 2026

Mise à jour

[Date]

PLAYBOOK

Données, accès et appareils – Réception et actions de premier niveau

Service Bureautique

📋 Alignement cadre :  NIST CSF 2.0 / SP 800-61r3  │  ISO/IEC 27035:2023  │  CIS Controls v8 (Contrôle 17)

1. Positionnement et spécificités de cette famille

Pour la famille Données, accès et appareils, le Service Bureautique joue un rôle de qualification et de réponse technique ciblée. Contrairement aux familles 1 et 2, l’isolation systématique n’est pas la première action — la qualification de l’impact est prioritaire.

📌 Chaîne :  Utilisateur → Service Bureautique → Boîte Sécurité → COMSI → CSIO (hiérarchie interne OP) | COMSI → ROCD (obligation GMVI N2+)

💡 Différence clé vs familles 1 et 2 :  Pas d’isolation immédiate sauf exception (compte admin compromis, intrusion active). La première action est SIGNALER et QUALIFIER. Préserver les preuves avant toute autre action.

2. Réception du signalement

2.1 Informations à collecter immédiatement

✔

Signalement initial – données, accès, appareil

□

Nom, prénom et unité administrative de l’utilisateur

□

Type d’incident : fuite / accès non autorisé / appareil perdu / compte compromis / intrusion / autre

□

Nature des données impliquées : renseignements personnels / données sensibles / administratives / publiques

□

Compte(s) concerné(s) et niveau de privilèges (utilisateur standard / administrateur)

□

Systèmes ou applications touchés

□

Date et heure approximatives de l’occurrence ou de la découverte

□

Pour un appareil : modèle, numéro de série, chiffrement actif (oui/non), MDM inscrit (oui/non)

□

Actions déjà effectuées avant le signalement

□

Preuves disponibles (journaux, courriels, alertes DLP, captures d’écran)

2.2 Classification préliminaire GMVI

Situation découverte

Niveau GMVI

Première action

Appareil chiffré perdu — aucune donnée sensible

1

Signaler, effacement MDM, consigner.

Appareil non chiffré perdu — données non sensibles

1

Effacement MDM. Signaler. Évaluer contenu.

Accès non autorisé — données non sensibles

1

Révoquer accès. Signaler. Consigner logs.

Wi-Fi non sécurisé — VPN actif

1

Signaler. Changer MdP. Consigner.

Appareil non chiffré perdu — données sensibles / PRP

2

Effacement MDM. COMSI déclare ROCD. Loi 25.

Accès non autorisé — données sensibles ou PRP

2

Révoquer accès. COMSI déclare ROCD. Loi 25.

Compte administrateur compromis ou en abus

2

Suspendre compte. COMSI déclare ROCD d’urgence.

Intrusion réseau active

2 ou 3

Isoler segment. COMSI déclare ROCD. Forensique.

Fuite / exfiltration de données confirmée

2 ou 3

Containment. COMSI déclare ROCD. Loi 25.

Destruction de données critiques

2 ou 3

Préserver. Évaluer sauvegardes. COMSI déclare ROCD.

⚠️ Obligation GMVI :  Toute MVI de niveau 2 et plus doit être portée à la connaissance du CSIO (hiérarchie interne OP) ET déclarée au ROCD (obligation GMVI externe) sans délai par le COMSI. Ces deux obligations sont simultanées. La présence de renseignements personnels déclenche systématiquement l’évaluation Loi 25.

3. Actions techniques par vecteur

3.1 Appareil perdu ou volé

✔

Actions — appareil perdu / volé

□

Vérifier si l’appareil est inscrit au MDM et si le chiffrement est actif

□

Déclencher la commande de verrouillage à distance via MDM (si disponible)

□

Déclencher l’effacement à distance si données sensibles présentes (sur instruction de la Boîte Sécurité)

□

Révoquer les certificats et jetons d’authentification associés à l’appareil

□

Mettre à jour l’inventaire des appareils

□

Documenter la date/heure de perte et le dernier emplacement connu

3.2 Compte compromis ou accès non autorisé

✔

Actions — compte compromis / accès non autorisé

□

Révoquer toutes les sessions actives du compte concerné

□

Réinitialiser le mot de passe et les jetons MFA

□

Consigner les journaux d’accès AVANT toute réinitialisation (ne pas effacer)

□

Pour un compte administrateur : SUSPENDRE le compte immédiatement, notifier le COMSI

□

Analyser les actions effectuées depuis le compte compromis (exports, modifications, suppressions)

□

Identifier les systèmes auxquels le compte a accédé anormalement

3.3 Fuite ou exfiltration de données

✔

Actions — fuite de données

□

Identifier précisément la nature et le volume des données impliquées

□

Identifier le destinataire ou le canal de fuite (courriel, service infonuagique externe (cloud), clé USB, partage)

□

Consigner les journaux DLP et d’audit avant toute action corrective

□

NE PAS tenter de rappeler ou d’effacer sans coordination avec la Boîte Sécurité

□

Identifier si des renseignements personnels sont impliqués (déclencheur Loi 25)

3.4 Intrusion réseau active

✔

Actions — intrusion réseau active (urgence)

□

Isoler le segment réseau affecté (sur instruction de la Boîte Sécurité)

□

Consigner les alertes IDS/IPS sans modifier la configuration

□

Identifier les IP sources et destinations de la connexion suspecte

□

Notifier le COMSI immédiatement par téléphone

□

Préserver les logs réseau (ne pas les purger)

4. Transmission à la Boîte Sécurité

📧 Objet standardisé :  [INCIDENT-DAA] [N1/N2/N3] – [Type] – [Système/Compte/Appareil] – [JJ-MM-AAAA]

Type d’incident

[Fuite / Accès non autorisé / Compte compromis / Appareil / Intrusion / Autre]

Données impliquées

[Type et sensibilité — PRP : oui/non]

Compte(s) concerné(s)

[Identifiant + niveau de privilèges]

Systèmes touchés

[Noms / IPs]

Date/heure occurrence

[JJ-MM-AAAA HH:MM]

Date/heure découverte

[JJ-MM-AAAA HH:MM]

Actions déjà effectuées

[Détail précis]

Preuves disponibles

[Logs, alertes DLP, captures]

Niveau GMVI proposé

[1 / 2 / 3]

5. Contacts d’urgence

Boîte Sécurité

securite@[organisation].ca  |  Poste : [XXXX]

COMSI

[Prénom Nom]  |  Poste : [XXXX]  |  Cell : [XXX-XXX-XXXX]

CSIO (N3+)

[Prénom Nom]  |  Cell 24/7 : [XXX-XXX-XXXX]

RPRP (si PRP impliquées)

[Prénom Nom]  |  Poste : [XXXX]

Responsable RH (incident interne)

[Prénom Nom]  |  Poste : [XXXX]

Approbation

Fonction

Nom

Signature

Date

[Titre]

[Prénom Nom]

📎 Documents connexes :  POL-SEC-001  |  DIR-SEC-001  |  PROC-SEC-003  |  PB-SEC-003  |  PB-COMSI-003
