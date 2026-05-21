---
title: "PROC-SEC-003 Donnees Acces Appareils"
source: "PROC-SEC-003_Donnees_Acces_Appareils.docx"
---

Codification

PROC-SEC-003

Entrée en vigueur

Mars 2026

Mise à jour

[Date]

Procédure – Gestion des incidents – Données, accès et appareils

R. Remplacement

Aucun document ne précède la présente procédure.

1. Objet

La présente procédure guide l’ensemble des employés, gestionnaires et équipes techniques dans la détection, le signalement et la gestion des incidents liés aux données, aux accès et aux appareils. Elle couvre les huit vecteurs définis à la section 4, qui se distinguent des deux autres familles par leur nature silencieuse : ces incidents sont souvent découverts après coup, parfois des jours ou des semaines après leur occurrence. Le premier geste est donc la qualification de l’impact, pas l’isolation.

Elle s’inscrit dans le cadre de la POL-SEC-001 et de la DIR-SEC-001, et est conforme aux obligations du Processus GMVI du MCN/CGCD, notamment en ce qui concerne la protection des renseignements personnels (Loi 25).

⚠️ Particularité de cette famille :  Contrairement aux familles 1 et 2, plusieurs incidents de cette famille ne requièrent pas d’isolation immédiate d’un système. La première action est de SIGNALER et de QUALIFIER l’impact avant d’agir — sauf en cas de compte administrateur actif en abus ou d’intrusion réseau en cours.

2. Champ d’application

La présente procédure s’applique à :

- tous les employés, contractuels, stagiaires et partenaires de l’organisation;

- tout actif informationnel de l’organisation, qu’il soit hébergé en interne, en infonuagique ou chez un tiers;

- tout compte utilisateur, de service ou administrateur lié aux systèmes de l’organisation;

- tout appareil utilisé à des fins professionnelles, qu’il soit fourni par l’organisation ou personnel (BYOD).

3. Définitions

Terme

Définition

Renseignements personnels (PRP)

Toute information permettant d’identifier directement ou indirectement une personne physique, au sens de la Loi sur la protection des renseignements personnels dans le secteur privé (Loi 25) et de la Loi sur l’accès aux documents des organismes publics.

Atteinte à la confidentialité

Accès, divulgation, copie, utilisation ou vol non autorisé de renseignements personnels au sens de la Loi 25 (art. 63.7).

Compte privilégié

Compte disposant d’autorisations élevées (administrateur local, administrateur domaine, compte de service avec droits étendus).

Principe du moindre privilège

Principe de sécurité selon lequel un utilisateur ou système ne doit disposer que des droits strictement nécessaires à l’exercice de ses fonctions.

Inventaire des actifs

Registre des systèmes, appareils et données de l’organisation, maintenu à jour et utilisé pour évaluer l’impact d’un incident.

Effacement sécurisé à distance

Procédure d’effacement des données d’un appareil perdu ou volé via un système de gestion des appareils mobiles (MDM).

DLP

Data Loss Prevention – système de contrôle visant à détecter et prévenir les fuites de données non autorisées.

IDS / IPS

Intrusion Detection / Prevention System – système de détection ou de prévention des intrusions sur le réseau.

RPRP

Responsable de la Protection des Renseignements Personnels – responsable désigné conformément à la Loi 25.

COMSI

Coordonnateur Organisationnel des Mesures de Sécurité de l’Information – déclare au ROCD dès le niveau 2 GMVI.

CAI

Commission d’accès à l’information – autorité québécoise à notifier en cas d’atteinte aux renseignements personnels (Loi 25, art. 63.8 à 63.11).

4. Instructions

4.1 Vecteurs couverts et signaux d’alerte

La présente procédure couvre les huit vecteurs suivants. La plupart sont à nature silencieuse : la découverte intervient après l’occurrence, parfois plusieurs jours plus tard.

Vecteur / Incident

Description

Signaux d’alerte typiques

Fuite ou vol de données

Divulgation non autorisée de données à un tiers extérieur, par erreur humaine, compromission ou action malveillante.

Courriel envoyé à la mauvaise adresse, signalement externe, alerte DLP, activité de téléversement anormale.

Accès non autorisé à des données sensibles

Consultation ou téléchargement de données protégées par un individu sans autorisation légitime.

Accès à des heures inhabituelles, volume de téléchargement anormal, accès à des fichiers hors périmètre du rôle.

Destruction ou altération malveillante de données

Suppression, modification ou corruption intentionnelle de données organisationnelles.

Fichiers supprimés en masse, données modifiées sans trace d’autorisation, sauvegardes corrompues.

Intrusion sur le réseau

Accès non autorisé à l’infrastructure réseau, par un acteur externe ou interne.

Connexions depuis des IPs inconnues, équipements réseau non reconnus, alertes IDS/IPS.

Compte compromis

Prise de contrôle d’un compte utilisateur ou de service par un acteur malveillant, interne ou externe.

Connexions depuis des pays inhabituels, tentatives de connexion échouées massives, activités post-connexion anormales.

Abus de compte à privilèges élevés

Utilisation abusive ou non autorisée d’un compte administrateur ou à accès privilégié pour accéder, modifier ou exfiltrer des données.

Actions administratives hors procédures, accès à des systèmes hors périmètre, modifications de configuration non planifiées.

Perte ou vol d’un appareil non chiffré

Disparition physique d’un ordinateur portable, téléphone ou tablette contenant des données organisationnelles non chiffrées.

Employé signalant la perte, appareil absent à l’inventaire, connexion à distance impossible.

Connexion à un réseau Wi-Fi non sécurisé

Utilisation d’un réseau public ou non sécurisé pour accéder à des systèmes ou données organisationnels.

Connexion VPN non active, utilisation d’un réseau inconnu, alertes système de gestion des appareils (MDM).

4.2 Instruction 1 – Découverte ou suspicion d’un incident

Contrairement aux familles 1 et 2, la première action n’est pas l’isolation systématique. Elle est la qualification immédiate : l’incident est-il actif en ce moment?

1

Signaler immédiatement à la Boîte Sécurité

Par courriel à securite@[organisation].ca ou par téléphone (poste [XXXX]).

Décrire ce qui a été observé : quelle donnée, quel compte, quel appareil, quelle activité suspecte, depuis quand.

2

Préserver les preuves

Ne pas supprimer, modifier ou déplacer des fichiers suspects.

Ne pas tenter de « corriger » la situation seul (modifier des droits, supprimer des journaux, réinitialiser un compte).

3

Exceptions — action immédiate requise sans attendre

Compte administrateur en abus actif : suspendre le compte immédiatement et signaler.

Intrusion réseau active détectée : isoler le segment affecté et signaler.

Appareil perdu contenant des données sensibles : déclencher l’effacement MDM si disponible et signaler.

4.3 Consignes spécifiques par vecteur

Vecteur / Situation

Consignes immédiates

Fuite de données — erreur humaine (courriel mal envoyé, fichier partagé par erreur)

Signaler immédiatement. Ne pas tenter de rappeler ou d’effacer sans coordination. Identifier précisément la nature des données divulguées. Évaluer Loi 25 si renseignements personnels impliqués.

Fuite de données — divulgation malveillante (employé ou tiers)

Signaler. Préserver les preuves (journaux d’accès, transferts). Ne pas confronter l’employé suspect avant coordination avec la sécurité et les RH.

Accès non autorisé à des données sensibles

Signaler. Identifier le compte impliqué. Révoquer l’accès si l’accès est encore actif. Consigner les journaux d’accès avant toute action.

Destruction ou altération malveillante de données

Signaler d’urgence. Ne pas tenter de restaurer sans instruction. Identifier l’étendue de l’impact et les sauvegardes disponibles.

Intrusion réseau active détectée

Isoler le segment réseau affecté. Signaler en urgence. Ne pas modifier la configuration du matériel réseau sans instruction de la Boîte Sécurité.

Compte utilisateur compromis

Révoquer la session active. Réinitialiser le mot de passe. Activer le MFA si non déjà actif. Analyser les journaux d’activité du compte.

Compte administrateur compromis ou en abus

SUSPENDRE LE COMPTE IMMEDÌATEMENT. Signaler d’urgence. Analyse forensique des actions effectuées. COMSI déclare au ROCD.

Perte ou vol d’appareil non chiffré avec données sensibles

Déclencher l’effacement MDM immédiatement si disponible. Signaler. Évaluer la nature des données présentes sur l’appareil. Évaluer Loi 25.

Perte ou vol d’appareil chiffré

Signaler. Déclencher l’effacement MDM par précaution. Consigner l’incident au registre. Niveau GMVI 1 si chiffrement confirmé.

Connexion Wi-Fi non sécurisée avec accès à des systèmes organisationnels

Signaler. Vérifier si le VPN était actif. Changer les mots de passe des services accédés. Évaluer les risques selon la sensibilité des systèmes consultés.

4.4 Informations à fournir lors du signalement

Lors de tout signalement, fournir les informations suivantes dans la mesure du possible :

- Type de vecteur : fuite de données, accès non autorisé, appareil perdu, compte compromis, intrusion, etc.

- Nature des données impliquées : sensibles, renseignements personnels, administratives, publiques.

- Compte(s) concerné(s) et niveau de privilèges.

- Systèmes ou applications touchés.

- Date et heure approximatives de l’occurrence ou de la découverte.

- Actions déjà effectuées avant le signalement.

- Toute preuve disponible (journaux, courriels, captures d’écran, alertes DLP).

📬 Contacts – Boîte Sécurité :  securite@[organisation].ca  |  Poste interne : [XXXX]  |  Lundi au vendredi, 8 h – 17 h  |  Pour les comptes administrateurs compromis et les intrusions actives : contacter directement par téléphone

4.5 Obligations spécifiques liées aux renseignements personnels (Loi 25)

Tout incident impliquant des renseignements personnels doit faire l’objet d’une évaluation spécifique conforme à la Loi sur la protection des renseignements personnels dans le secteur privé (Loi 25) et à la Loi sur l’accès aux documents des organismes publics, sections 63.7 à 63.11.

Étape

Obligation

1. Identifier la nature des données

Déterminer si des renseignements personnels ont été accédés, divulgués, copiés, utilisés ou volés.

2. Évaluer le risque de préjudice

Analyser si l’atteinte est susceptible de causer un préjudice sérieux aux personnes concernées.

3. Informer le RPRP

Le RPRP de l’organisation doit être informé dès la découverte de l’atteinte.

4. Informer le CSIO

Le RPRP informe le CSIO, qui décide de la déclaration à la CAI et aux personnes concernées.

5. Déclarer à la CAI

Si risque sérieux de préjudice : déclarer à la CAI SANS DÉLAI (Loi 25, art. 63.8 à 63.11).

6. Notifier les personnes concernées

Si risque sérieux de préjudice : notifier les personnes concernées sans délai.

7. Tenir un registre

Consigner l’atteinte dans le registre des atteintes à la sécurité, tenu par le RPRP.

📬 Référence légale :  Loi 25 – Sections 63.7 à 63.11 de la Loi sur l’accès aux documents des organismes publics et sur la protection des renseignements personnels. CAI : 1-888-528-7741

4.6 Niveaux GMVI et obligations de déclaration

Les incidents de cette famille sont classés selon les niveaux du processus GMVI. La présence de renseignements personnels exfiltrés ou la compromission d’un compte administrateur font systématiquement l’objet d’une évaluation pour le niveau 2.

Niveau GMVI

Critères

Action de déclaration

1

Incident isolé, impact limité, pas de renseignements personnels, géré entièrement à l’interne. Ex. : appareil perdu chiffré, accès non autorisé détecté et révoqué.

COMSI informe le ROCD. Documentation au registre.

2

Données sensibles accédées ou exfiltrées, compte administrateur compromis, intrusion active sur le réseau, appareil non chiffré perdu avec données sensibles.

COMSI déclare au ROCD sans délai. Évaluer Loi 25.

3

Exfiltration confirmée de renseignements personnels en grande quantité, intrusion touchant plusieurs OP ou systèmes gouvernementaux, destruction de données critiques.

COCD déclare au CGCD. Formulaire MVI obligatoire. Notification CAI.

4

Compromission systémique de l’infrastructure, atteinte à l’intégrité de systèmes d’État, crise déclarée par le CCGSI.

CCGSI active le plan de crise gouvernemental.

⚠️ Obligation GMVI :  Toute MVI de niveau 2 et plus doit être portée à la connaissance du CSIO (hiérarchie interne OP) ET déclarée au ROCD (obligation GMVI externe) sans délai par le COMSI, conformément à DIR-SEC-001. Ces deux obligations sont simultanées.

4.7 Rappels importants

🚫 Rappel 1 — Ne jamais confronter seul :  Si un employé interne est suspecté d’être à l’origine d’un incident (fuite, abus de privilèges), ne jamais le confronter directement. Contacter la sécurité et les ressources humaines. Une action prématurée peut détruire les preuves.

🚫 Rappel 2 — Loi 25 s’applique même aux erreurs non malveillantes :  Un courriel envoyé par erreur à la mauvaise personne contenant des renseignements personnels est une atteinte au sens de la Loi 25. L’intention n’a aucune incidence sur l’obligation de déclaration.

🚫 Rappel 3 — Un appareil chiffré perdu reste un incident à signaler :  Même si l’appareil est chiffré, la perte doit être signalée pour permettre la révocation des accès, l’effacement MDM, la mise à jour de l’inventaire et la consignation au registre.

5. Rôles et responsabilités

Acteur

Responsabilités

Tous les employés

Signaler immédiatement tout incident découvert. Ne pas tenter de résoudre seul. Préserver les preuves.

Gestionnaires

Signaler immédiatement tout incident dont ils ont connaissance, y compris les comportements suspects de membres de leur équipe.

Service Bureautique

Recevoir et qualifier les signalements, effectuer les actions techniques de premier niveau selon les instructions, transmettre à la Boîte Sécurité.

Boîte Sécurité

Triage, classification GMVI, analyse forensique, coordination de la réponse, notification COMSI et évaluation Loi 25.

RPRP

Recevoir la notification du CSIO. Évaluer l’obligation de déclaration à la CAI. Tenir le registre des atteintes. Notifier les personnes concernées si requis.

COMSI

Coordonner la réponse, déclarer au ROCD (N2+), maintenir le registre des événements, assurer la liaison avec le COCD/CGCD.

CSIO

Responsable de la prise en charge de toutes les MVI. Décisions stratégiques, approbation des communications, notification Loi 25 en concertation avec le RPRP.

MAJ. Mise à jour

Ce document est placé sous la responsabilité du COMSI et doit être révisé :

- Annuellement, après tout incident de niveau 3+, lors de modifications législatives (Loi 25, LPRPDE) ou lors de changements majeurs dans la gestion des accès de l’organisation

- Après tout changement organisationnel majeur affectant les rôles décrits.

- Lors de toute évolution significative du cadre réglementaire applicable.

A. Approbation

Fonction

Nom

Signature

Date

[Titre]

[Prénom Nom]

📎 Documents connexes :  POL-SEC-001  |  DIR-SEC-001  |  PB-BUR-003  |  PB-SEC-003  |  PB-COMSI-003  |  PB-CSIO-003  |  PB-GEN-003  |  Loi 25 (sections 63.7 à 63.11)  |  Processus GMVI (MCN/CGCD)
