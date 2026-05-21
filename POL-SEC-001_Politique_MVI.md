---
title: "POL-SEC-001 Politique MVI"
source: "POL-SEC-001_Politique_MVI.docx"
---

Codification

POL-SEC-001

Entrée en vigueur

Mars 2026

Mise à jour

[Date]

Politique – Gestion des menaces, vulnérabilités et incidents de sécurité de l’information

R. Remplacement

Aucune politique ne précède le présent document.

1. Contexte

L’organisation est un organisme public assujetti au cadre normatif du gouvernement du Québec en matière de sécurité de l’information. À ce titre, elle est partie prenante du Processus de gestion des menaces, vulnérabilités et incidents (GMVI) établi par le Ministère de la Cybersécurité et du Numérique (MCN) et administré par le Centre gouvernemental de cybersécurité et de cybersécurité (CGCD), en lien avec le Centre opérationnel de cybersécurité (COCD) compétent.

Le paysage des cybermenaces auxquelles font face les organismes publics est en constante évolution. Les attaques par ingénierie sociale, les logiciels malveillants et l’exploitation de vulnérabilités constituent des vecteurs d’attaque majeurs susceptibles de compromettre la confidentialité, l’intégrité et la disponibilité des actifs informationnels de l’organisation et, par ext ension, de l’ensemble de l’écosystème gouvernemental.

La présente politique établit le cadre organisationnel de la gestion de ces menaces, en assurant la cohérence avec les exigences du GMVI, la Loi sur la cybersécurité, la Loi 25 sur la protection des renseignements personnels, le Cadre gouvernemental de gestion de la sécurité de l’information (CGGSI) et les référentiels NIST CSF 2.0, ISO/IEC 27035:2023 et CIS Controls v8.

📋 Cadres normatifs de référence :  Processus GMVI (MCN/CGCD)  │  Loi sur la cybersécurité (LRQ, c. C-33.1)  │  Loi 25 (protection des renseignements personnels)  │  LGGRI  │  NIST CSF 2.0  │  ISO/IEC 27035:2023  │  CIS Controls v8

2. Objet

La présente politique a pour objet d’établir les principes, les obligations et le cadre de gouvernance qui régissent la gestion des menaces, des vulnérabilités et des incidents (MVI) de sécurité de l’information au sein de l’organisation. Elle assure l’alignement avec les exigences du processus GMVI du Centre gouvernemental de cybersécurité (CGCD) et établit les obligations de déclaration, de coordination et de reporting qui incombent à l’organisation en sa qualité d’organisme public.

3. Champ d’application

La présente politique s’applique à :

- l’ensemble des employés, gestionnaires, cadres, contractuels, stagiaires et partenaires de l’organisation ayant accès aux actifs informationnels ou aux systèmes de l’organisation;

- tout actif informationnel de l’organisation, qu’il soit hébergé en interne, en infonuagique ou exploité par un tiers;

- tout appareil utilisé à des fins professionnelles, qu’il soit fourni par l’organisation ou personnel (BYOD);

- toute menace, vulnérabilité ou incident de sécurité de l’information relevant des catégories visées à la section 5.

4. Définitions

Terme

Définition

Menace, vulnérabilité ou incident (MVI)

Tout événement ou condition susceptible de compromettre la sécurité des actifs informationnels. Regroupe trois catégories : menace (potentielle), vulnérabilité (faiblesse exploitable), incident (att einte confirmée ou en cours).

Niveau de coordination

Niveau défini par le GMVI (1 à 4) déterminant l’instance de coordination responsable de la MVI, selon son impact et son étendue.

COMSI

Coordonnateur Organisationnel des Mesures de Sécurité de l’Information – principal point de contact de l’OP pour toutes les MVI.

CSIO

Chef de la Sécurité de l’Information Organisationnelle – responsable de la prise en charge de toutes les MVI au niveau de l’OP.

OSC

Opérateur de solutions de cybersécurité – opère les outils de cybersécurité de l’OP.

ROCD

Responsable opérationnel de cybersécurité – coordonne les MVI de niveau 2 au niveau du COCD.

CDSI

Chef délégué de la sécurité de l’information – responsable de la prise en charge des MVI au palier COCD.

COCD

Centre opérationnel de cybersécurité – instance de coordination de niveau 2.

CGCD

Centre gouvernemental de cybersécurité – coordonne les MVI de niveau 3 et plus. Effectue la veille gouvernementale.

CGSI

Chef gouvernemental de la sécurité de l’information – autorité gouvernementale ultime.

RGCD

Responsable gouvernemental de cybersécurité – émet des obligations aux membres du Réseau gouvernemental.

CCGSI

Comité de crise gouvernemental en sécurité de l’information – activé au niveau 4.

CERT/AQ

Centre d’alerte et de réponse aux incidents de sécurité du Québec – intervient dans le suivi des incidents de niveaux 2, 3 et 4.

Formulaire MVI

Document formel obligatoire pour toute MVI de niveaux 3 et 4, transmis selon les canaux préscrits par le GMVI.

Mode Alerte / Crise

États formels d’une MVI pouvant être déclarés par le CCGSI, déclenchant des obligations spécifiques à chaque intervenant.

CVSS

Common Vulnerability Scoring System – système standard d’évaluation de la gravité des vulnérabilités utilisé par le CGCD.

Registre des événements de sécurité

Registre prévu à l’article 16 de la Directive sur la sécurité de l’information. Le CGCD se réserve le droit de le consulter.

Renseignements personnels (PRP)

Données identifiées comme renseignements personnels au sens de la Loi 25. Toute atteinte doit faire l’objet d’une déclaration à la Commission d’accès à l’information (CAI).

5. Principe général

L’organisation s’engage à gérer de façon proactive, structurée et coordonnée toute menace, vulnérabilité ou incident susceptible d’affecter ses actifs informationnels ou ceux de l’écosystème gouvernemental auquel elle appartient. Cette gestion s’effectue en pleine conformité avec le processus GMVI du MCN/CGCD, en maintenant à tout moment les capacités de détection, de signalement, de confinement, d’éradication et de reprise nécessaires à la protection des renseignements et des services dont elle a la responsabilité.

Les menaces visées par la présente politique couvrent les catégories suivantes, retenues en fonction de leur pertinence pour l’environnement opérationnel de l’organisation :

Catégorie

Menaces visées

Exemples représentatifs

Ingénierie sociale

Hameçonnage, harponnage, fraude au président (BEC), hameçonnage par SMS (smishing), hameçonnage vocal (vishing), hameçonnage par QR (quishing), usurpation d’identité interne

Courriel frauduleux, SMS malveillant, appel téléphonique frauduleux, QR code malveillant

Logiciels malveillants

Virus, vers, rançongiciel, logiciel espion, enregistreur de frappes, cheval de Troie, Logiciel furtif (rootkit), logiciel sans fichier, cryptomineur non autorisé

rançongiciel (ransomware) en propagation, enregistreur de frappes (keylogger) sur poste administratif, logiciel sans fichier (fileless malware) en mémoire

Exploitation technique

Exploitation de vulnérabilités (CVE), injection SQL, script intersites (XSS), déni de service (DoS/DDoS), attaque de l’intercepteur (MitM)

Exploitation de correctif non appliqué, attaque sur application web, saturation d’infrastructure

Accès et identités

Compte compromis (interne ou externe), abus de compte à privilèges élevés

Prise de contrôle de compte administrateur, mouvement latéral post-compromission

Données et infrastructure

Fuite ou vol de données, accès non autorisé à des données sensibles, destruction ou altération malveillante de données, intrusion sur le réseau

Exfiltration de renseignements personnels, destruction de bases de données

Appareils et périphériques

Perte ou vol d’un appareil non chiffré, connexion à un réseau Wi-Fi non sécurisé

Ordinateur portable perdu en déplacement, connexion sur réseau public non protégé

6. Principes directeurs

6.1 Intégration au processus GMVI

L’organisation reconnaît le processus GMVI du MCN comme cadre de référence obligatoire pour la gestion de toute MVI. Elle s’engage à respecter les niveaux de coordination, les délais de déclaration, les formats de communication et les obligations de reporting qui en découlent. Le tableau suivant présente la structure de coordination GMVI applicable à l’organisation :

Niveau de coordination

Instance responsable

Déclencheur principal

Déclaration obligatoire

Niveau 1

COMSI / CSIO (Organisme public)

MVI gérée entièrement à l’interne de l’OP

COMSI informe le ROCD

Niveau 2

ROCD / COCD

MVI dépassant les capacités de l’OP ou touchant plusieurs OP

COMSI déclare au ROCD; ROCD informe le CGCD

Niveau 3

CGCD / CGSI

MVI à impact gouvernemental élargi

CGCD coordonne; COCD déclare au CGCD

Niveau 4 (Crise)

CCGSI (Comité de crise gouvernemental)

MVI classifiée en mode « Alerte » ou « Crise » par le CCGSI

CCGSI active le plan gouvernemental de gestion de crise

6.2 Déclaration obligatoire et chaîne de communication

Toute MVI détectée doit faire l’objet d’un signalement interne immédiat. Les obligations de communication vers l’écosystème gouvernemental sont les suivantes :

- Le COMSI informe le CSIO de toutes les MVI détectées, quel qu’en soit le niveau.

- Le COMSI informe le ROCD des MVI de niveau 1.

- Le COMSI déclare toute MVI de niveau 2 et plus au ROCD, sans délai.

- Pour les niveaux 3 et 4, le formulaire MVI officiel est obligatoire.

- Le COMSI assure la liaison avec les équipes internes (opérations, communications, PRP) et avec les forces de l’ordre si la MVI intègre un volet criminel.

- L’organisation se conformera à toute instruction obligatoire émise par le RGCD, à toute indication d’application du CGSI et à toute demande du CGCD, notamment la mise à disposition du registre des événements de sécurité prévu à l’article 16 de la Directive.

6.3 Gestion des vulnérabilités

L’organisation maintient un processus actif de gestion des vulnérabilités conforme aux exigences du GMVI. À ce titre :

- Elle applique les correctifs ou mesures de remédiation dans les délais exigés par le CGCD.

- Elle informe le CGCD de l’état d’avancement des travaux de remédiation à une fréquence de 14 jours civils, sauf exception ou mise en place du correctif.

- Elle se conforme à toute évaluation de préjudice établie par le COCD et transmise via le CGCD, y compris les décisions de fermeture d’actif en cas de préjudice élevé ou très élevé.

- Elle s’abonne aux bulletins, alertes et avis du CGCD et du COCD comme source primaire d’information sur les menaces actives.

6.4 Protection des renseignements personnels (PRP)

Toute MVI impliquant des renseignements personnels au sens de la Loi 25 fait l’objet d’un traitement distinct. Le responsable de la protection des renseignements personnels (RPRP) de l’organisation informe le CSIO, qui déclare l’incident au CGCD. La déclaration à la Commission d’accès à l’information (CAI) est effectuée conformément aux obligations de la Loi 25, sans délai une fois l’atteinte confirmée.

6.5 Continuité des activités et reprise

L’organisation maintient un Plan de continuité des activités (PCA) et un Plan de reprise des activités (PRA) alignés avec les exigences du GMVI. Ces plans sont activés dès que l’impact d’une MVI compromet la disponibilité des services critiques. Leur mise à jour suit le cycle de révision annuel ou est déclenchée par tout incident de niveau 3 ou supérieur.

6.6 Documentation, registres et bilan

L’organisation tient un registre des événements de sécurité conforme à l’article 16 de la Directive sur la sécurité de l’information. Pour tout incident de niveau 3 ou 4, un bilan formel est produit dans les 30 jours suivant la résolution, en collaboration avec le COCD concerné et le CGCD. Ce bilan est transmis aux intervenants suivants : COMSI, CSIO, ROCD, CDSI, CGSI. Tout rapport produit par une firme externe est remis au CERT/AQ au plus tard deux semaines après la résolution.

6.7 Sensibilisation et formation

L’organisation s’assure que l’ensemble des employés reçoit une formation sur la reconnaissance et le signalement des menaces couvertes par la présente politique. Cette formation est intégrée au processus d’accueil des nouveaux employés et révisée annuellement ou après tout incident significatif. Le COMSI coordonne l’élaboration et la mise en oeuvre de cette formation interne.

6.8 Amélioration continue

L’organisation intègre les leçons apprises à la suite de chaque MVI dans la mise à jour de ses procédures, directives et outils. Les recommandations prioritaires du bilan d’incident font l’objet d’une vérification de leur application dans les 6 mois suivant leur émission, conformément au GMVI.

7. Rôles et responsabilités

Le tableau suivant présente l’ensemble des intervenants concernés par la présente politique, qu’ils soient internes à l’organisation ou membres de l’écosystème gouvernemental :

Intervenant

Instance

Rôle dans la présente politique

COMSI

Organisme public (OP)

Point de contact principal de l’OP pour toutes les MVI. Coordonne le niveau 1, déclare au ROCD dès le niveau 2.

CSIO

Organisme public (OP)

Responsable de la prise en charge de toutes les MVI au niveau de l’OP selon les modalités prévues.

OSC

Organisme public (OP)

Opère les outils de cybersécurité de l’OP.

ROCD

COCD

Coordonne les MVI de niveau 2 au niveau des OP supportés par le COCD. Informe le CERT/AQ et le CGCD.

CDSI

COCD

Responsable de la prise en charge de toutes les MVI au niveau de l’OP selon les modalités prévues (palier COCD).

CGCD

Gouvernement

Coordonne les MVI de niveau 3 et plus. Effectue la veille gouvernementale. Évalue les vulnérabilités via CVSS.

CGSI

Gouvernement

Chef gouvernemental de la sécurité de l’information. Aut orité gouvernementale ultime.

RGCD

Gouvernement

Émet des obligations aux membres du Réseau gouvernemental de cybersécurité.

CCGSI

Gouvernement

Comité de crise gouvernemental en sécurité de l’information. Active et gère le niveau 4.

CERT/AQ

Gouvernement

Assure le suivi des incidents de niveaux 2, 3 et 4. Reçoit les rapports du ROCD.

Les responsabilités détaillées de chaque intervenant interne sont décrites dans la Directive de gestion des MVI (DIR-SEC-001) et les playbooks opérationnels associés.

MAJ. Mise à jour

Ce document est placé sous la responsabilité du CSIO et doit être révisé :

- Annuellement ou après tout incident de niveau 3 ou supérieur, ou lors de toute modification du processus GMVI

- Après tout changement organisationnel majeur affectant les rôles décrits.

- Lors de toute évolution significative du cadre réglementaire applicable.

A. Approbation

Fonction

Nom

Signature

Date

[Titre]

[Prénom Nom]

📎 Documents connexes :  Processus GMVI (MCN/CGCD)  |  DIR-SEC-001  |  PROC-SEC-001  |  PB-GEN-001  |  Loi sur la cybersécurité  |  Loi 25  |  LGGRI  |  Directive sur la sécurité de l’information (art. 16)
