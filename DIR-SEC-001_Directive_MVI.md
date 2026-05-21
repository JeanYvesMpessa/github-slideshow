---
title: "DIR-SEC-001 Directive MVI"
source: "DIR-SEC-001_Directive_MVI.docx"
---

Codification

DIR-SEC-001

Entrée en vigueur

Mars 2026

Mise à jour

[Date]

Directive – Gestion des menaces, vulnérabilités et incidents de sécurité de l’information

R. Remplacement

La présente directive remplace la directive d’escalade DIR-SEC-ESC-001 (Mars 2026), dont elle intègre et élargit la portée.

1. Objet

La présente directive définit les modalités opérationnelles de gestion des menaces, vulnérabilités et incidents (MVI) de sécurité de l’information au sein de l’organisation, en conformité avec le Processus de gestion des menaces, vulnérabilités et incidents (GMVI) du Ministère de la Cybersécurité et du Numérique (MCN) et la Politique de gestion des MVI (POL-SEC-001).

Elle établit les obligations de détection, de signalement, de déclaration, de confinement, d’éradication, de reprise et de documentation qui s’imposent à tous les intervenants de l’organisation, et précise les liens avec la chaîne de coordination gouvernementale (COCD, CGCD, CGSI, CCGSI).

📋 Cadres de référence :  Processus GMVI (MCN/CGCD)  │  POL-SEC-001  │  NIST CSF 2.0 / SP 800-61r3  │  ISO/IEC 27035:2023  │  CIS Controls v8 (Contrôle 17)  │  Loi sur la cybersécurité  │  Loi 25

2. Champ d’application

La présente directive s’applique à l’ensemble des employés, gestionnaires, cadres, contractuels et partenaires de l’organisation, pour toutes les catégories de menaces visées par la POL-SEC-001. Elle s’applique également aux tierces parties opérant des actifs ou des services pour le compte de l’organisation.

3. Définitions

Les définitions établies à la section 4 de la POL-SEC-001 s’appliquent intégralement à la présente directive. Les définitions complémentaires suivantes s’y ajoutent :

Terme

Définition

Dossier MVI

Ensemble des documents liés à une MVI : journal d’incident, preuves collectées, notifications, formulaire MVI, bilan. Maintenu par le COMSI.

Formulaire MVI

Document formel prescrit par le GMVI, obligatoire pour les niveaux 3 et 4, transmis aux destinataires GMVI définis à l’Annexe 2 du processus.

Registre des événements

Registre prévu à l’article 16 de la Directive sur la sécurité de l’information, tenu par le COMSI et accessible au CGCD sur demande.

Analyse de préjudice

Processus d’évaluation de l’impact d’une vulnérabilité, conduit par le COCD à partir de l’indicateur de probabilité d’exploitation (CVSS) défini par le CGCD.

IOC (Indicator of Compromise)

Artefact observable (adresse IP, URL, hash, domaine) témoignant d’une activité malveillante. Collecté et transmis au COCD/CGCD pour enrichissement de la veille gouvernementale.

Mode Alerte / Mode Crise

Statuts formels d’une MVI déclarés par le CCGSI. Le Mode Alerte déclenche une surveillance renforcée; le Mode Crise active le Plan gouvernemental de gestion de crise en sécurité de l’information.

Réseau d’alerte interne

Dispositif de communication entre le ROCD et les COMSI des OP sous sa responsabilité, activé lors de MVI de niveau 2 et plus.

4. Modalités

4.1 Niveaux de coordination GMVI et obligations de déclaration

Toute MVI détectée est classée selon les niveaux de coordination GMVI. La classification est établie par le COMSI et validée par le CSIO. En cas de doute, le niveau supérieur s’applique. Le niveau peut être réévalué en tout temps lors d’un développement important. Lorsque c’est le cas, les étapes 3.1, 3.2 et 3.3 du processus GMVI doivent être répétées.

Niveau

Instance responsable

Critères de déclenchement

Délai de déclaration

Action de déclaration requise

1

COMSI / CSIO
(Organisme public)

MVI gérée entièrement à l’interne de l’OP sans propagation externe

Sans délai (interne)

COMSI informe le CSIO. COMSI informe le ROCD. Documentation au registre des événements.

2

ROCD / COCD

MVI dépassant les capacités de l’OP, touchant plusieurs OP ou nécessitant une coordination élargie

Sans délai

COMSI déclare au ROCD. Formulaire MVI transmis. ROCD informe le CGCD et le CERT/AQ.

3

CGCD
(Gouvernemental)

MVI à impact gouvernemental élargi, nécessitant coordination entre plusieurs COCD ou secteurs

Sans délai

Formulaire MVI obligatoire. COCD déclare au CGCD. CGCD coordonne et informe le CGSI.

4 (Crise)

CCGSI
(Comité de crise gouvernemental)

MVI classifiée en mode « Alerte » ou « Crise » par le CCGSI. Impact stratégique sur l’État.

Immédiat

CCGSI active le Plan gouvernemental de gestion de crise. CGCD : volet opérationnel. CCGSI : volet stratégique.

⚠️ Obligation absolue :  Toute MVI de niveau 2 et plus doit être déclarée au ROCD sans délai, même si l’information est préliminaire ou partielle. Le COMSI ne peut substituer cette déclaration par une escalade interne uniquement.

4.2 Détection et signalement

Tout employé, gestionnaire ou système automatique ayant détecté ou suspecté une MVI doit en informer le Service Bureautique ou la Boîte Sécurité immédiatement. Le signalement doit préciser :

- La nature et la description de la MVI (type de menace, systèmes potentiellement affectés).

- La date et l’heure de détection ou du signalement.

- Les actions déjà effectuées (y compris les erreurs ou clics accidentels).

- Tout comportement anormal observé sur le système ou le réseau.

Le COMSI est le principal point de contact de l’OP pour toutes les actions reliées à la cybersécurité. Il est notamment responsable de :

- Recevoir et traiter les notifications du CGCD et du COCD.

- Assurer la liaison avec les équipes internes de l’OP (opérations, communications, PRP).

- Assurer la liaison avec les forces de l’ordre si la MVI comporte un volet criminel.

- Évaluer le niveau de coordination requis à l’aide des outils normalisés du GMVI.

4.3 Confinement, éradication et reprise

Dès la détection d’une MVI, les mesures de confinement appropriées sont activées sans délai par la Boîte Sécurité et le Service Bureautique, sous la coordination du COMSI. Les options de remédiation disponibles, conformément au GMVI, sont :

- L’application d’un correctif de sécurité.

- L’application d’une mesure d’atténuation jugée adéquate.

- L’isolement du système affecté.

- La fermeture du système (en cas de préjudice élevé ou très élevé, sur instruction du CGCD).

Aucun système isolé ne peut être remis en service sans validation préalable de la Boîte Sécurité et du COMSI. Pour les MVI de niveaux 3 et 4, la décision de reprise est prise en concertation avec le COCD ou le CGCD.

4.4 Gestion des vulnérabilités

La gestion des vulnérabilités constitue un processus distinct mais intégré à la présente directive. Les obligations suivantes s’appliquent :

- Le COMSI s’abonne aux bulletins de sécurité émis par le CGCD, le COCD et le CERT/AQ, et s’assure de leur diffusion interne aux équipes concernées.

- Dès la réception d’un avis ou d’une alerte, l’organisation évalue les actifs affectés dans son périmètre et planifie la remédiation.

- La remédiation est appliquée dans les délais exigés, en tenant compte de l’indicateur de probabilité d’exploitation (CVSS) établi par le CGCD et communiqué par le ROCD.

- Le COMSI informe le CGCD de l’état d’avancement des travaux de remédiation à une fréquence de 14 jours civils, sauf mise en place du correctif ou exception justifiée.

- Le CGCD se réserve le droit de réévaluer le préjudice établi par le COCD et d’exiger la fermeture d’un actif comportant un préjudice élevé ou très élevé.

4.5 Communications formelles GMVI

L’organisation se conforme au référentiel de communications formelles de l’Annexe 2 du processus GMVI. Le tableau suivant présente les types de communications, leurs déclencheurs et leurs destinataires :

Type de communication

Moment / Déclencheur

Expéditeur

Destinataire(s)

Notification MVI

Dès la détection ou la notification

OP, COCD ou CGCD

CSIO (N1), COCD (N2), CGCD (N3)

Formulaire MVI

Obligatoire pour niveaux 3 et 4

OP, COCD ou CGCD

CSIO (N1), COCD (N2), CGCD (N3)

État de la situation

En continu, dès la détection jusqu’à la clôture

COCD
CGCD

CGCD
CGSI

Rapport requis

Au besoin (PRP, physique, cybercriminalité)

OP, COCD ou CGCD

Entités externes ou CGCD; EIMSIG

Bulletins, alertes et avis

En continu (veille gouvernementale)

CGCD
COCD

Abonnés de la fonction publique
OP concernés

Rapports à la haute direction

Au besoin, niveaux 3 et 4

CGCD

CGSI

Recommandations

Au besoin, niveaux 3 et 4

CGCD

RAG

Instructions obligatoires

Au besoin, niveaux 3 et 4

RGCD

Tous les intervenants

Indications d’applications

Au besoin, niveaux 3 et 4

CGSI

Tous les intervenants

Bilan d’incident

Dans les 30 jours (niveaux 3 et 4)

Instance de coordination responsable

COMSI, CSIO, ROCD, CDSI, CGSI

🚫 Règle absolue :  Aucune information sur une MVI ne peut être communiquée à l’extérieur de la chaîne de coordination sans approbation explicite du CSIO et, pour les niveaux 3 et 4, du CGCD. Toute communication médiatique ou publique est soumise à cette même approbation.

4.6 Délais obligatoires

Le tableau suivant consolide les délais applicables, en distinguant les obligations internes de celles découlant du GMVI :

Délai

Action requise

Responsable interne

Référence GMVI

Immédiat

Signalement interne par l’employé

Employé

Niveau 1

Sans délai

Transmission au COMSI et ouverture du dossier MVI

Service Bureautique / Employé

Niveau 1

Sans délai

Déclaration au ROCD (MVI de niveau 2 et plus)

COMSI

Niveaux 2, 3, 4

Toutes les 2 h

Mise à jour du journal d’incident interne

Boîte Sécurité

Niveaux 2, 3, 4

14 jours civils

Rapport d’avancement de la remédiation d’une vulnérabilité au CGCD

COMSI / CSIO

Vulnérabilités

5 jours ouvrables

Rapport de clôture interne

Boîte Sécurité + COMSI

Niveaux 1 et 2

30 jours

Bilan formel GMVI (niveaux 3 et 4)

COMSI / CSIO + Instance GMVI

Niveaux 3, 4

2 semaines post-résolution

Remise du rapport de firme externe au CERT/AQ

COMSI / CSIO

Niveaux 3, 4

6 mois post-bilan

Vérification de l’application des recommandations prioritaires

COMSI

GMVI – bilan d’incident

4.7 Protection des renseignements personnels (PRP)

Toute MVI impliquant des renseignements personnels fait l’objet d’une déclaration spécifique. Le responsable de la protection des renseignements personnels (RPRP) informe le CSIO, qui décide de l’opportunité de déclaration à la Commission d’accès à l’information (CAI) conformément à la Loi 25. Le COMSI assure la liaison avec le COCD/CGCD pour les volets PRP qui le requièrent.

📬 Rappel légal Loi 25 :  Toute atteinte à des renseignements personnels présentant un risque sérieux de préjudice doit être déclarée à la CAI et aux personnes concernées, sans délai une fois confirmée. Loi sur l’accès aux documents des organismes publics, sections 63.8 à 63.11.

4.8 Activation des modes Alerte et Crise (CCGSI)

Lorsque le CCGSI déclare une MVI en mode « Alerte » ou « Crise », les obligations suivantes s’imposent immédiatement à l’organisation :

- Se conformer à toute directive ou instruction obligatoire émise par le RGCD ou le CGSI.

- Mettre à disposition l’ensemble des informations demandées par le CGCD, notamment le registre des événements de sécurité.

- Participer, sur convocation, aux activités de coordination de l’Équipe d’intervention ponctuelle (EIP) coordonnée par le CGCD.

- Activer le Plan de continuité des activités (PCA) si l’impact sur les services l’exige.

4.9 Registre des événements de sécurité et documentation

Le COMSI tient un registre des événements de sécurité conforme à l’article 16 de la Directive sur la sécurité de l’information. Ce registre est maintenu à jour en temps réel lors de toute MVI active et est conservé pendant une période minimale de 5 ans. Le CGCD se réserve le droit d’en demander la consultation à tout moment.

Pour chaque MVI de niveaux 3 ou 4, un bilan formel est produit dans les 30 jours suivant la résolution, en collaboration avec les instances GMVI concernées. Ce bilan est transmis à : COMSI, CSIO, ROCD, CDSI, CGSI. Tout rapport produit par une firme externe est remis au CERT/AQ au plus tard deux semaines après la résolution.

Les recommandations prioritaires du bilan font l’objet d’une vérification de leur application dans les 6 mois suivant leur émission.

5. Rôles et responsabilités

La matrice RACI ci-dessous précise les responsabilités de chaque acteur pour les activités définies par la présente directive. Légende : R = Réalise | A = Approuve | C = Contribue | I = Informe

Activité

COMSI

CSIO

OSC

ROCD/
COCD

CGCD+

Détecter et signaler une MVI (niveau 1)

R

A

C

I

I

Déclarer la MVI au ROCD (niveau 2+)

R

A

I

I

Coordonner la réponse au niveau de l’OP

R

A

C

I

I

Opérer les outils de cybersécurité

C

I

R

I

I

Triage et classification de la MVI

R

A

C

C

I

Isolation et confinement du système affecté

R

A

R

C

I

Analyse forensique

R

A

R

C

I

Coordination COCD (niveau 2)

I

I

R

I

Coordination CGCD (niveau 3+)

I

I

C

R

Évaluation CVSS de la vulnérabilité

C

I

C

R

Remédiation vulnérabilité (application correctif)

R

A

R

I

I

Rapport d’avancement remédiation (14 jours)

R

A

I

I

Notification PRP / CAI

C

R

I

I

Production bilan formel GMVI (30 jours, N3-N4)

R

A

C

C

Liaison avec les forces de l’ordre

R

A

I

I

Revue post-incident et amélioration continue

R

A

C

C

I

Mise à jour des procédures et playbooks

R

A

C

I

I

La colonne « CGCD+ » regroupe les acteurs gouvernementaux (CGCD, CGSI, CCGSI, RGCD) dont les responsabilités s’exercent au-delà du périmètre de l’organisme public, conformément au processus GMVI. Les descriptions détaillées de leurs responsabilités sont définies dans le Tableau 12 du processus GMVI (MCN/CGCD).

MAJ. Mise à jour

Ce document est placé sous la responsabilité du CSIO et doit être révisé :

- Annuellement, après tout incident de niveau 3 ou supérieur, ou lors de toute modification du processus GMVI

- Après tout changement organisationnel majeur affectant les rôles décrits.

- Lors de toute évolution significative du cadre réglementaire applicable.

A. Approbation

Fonction

Nom

Signature

Date

[Titre]

[Prénom Nom]

📎 Documents connexes :  POL-SEC-001  |  Processus GMVI (MCN/CGCD)  |  PROC-SEC-001  |  PB-GEN-001  |  Loi sur la cybersécurité  |  Loi 25 (sections 63.8 à 63.11)  |  LGGRI  |  Directive sur la sécurité de l’information (art. 16)
