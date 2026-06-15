---
title: DIR-GIA-001 — Directive de gestion des identités et des accès
code: DIR-GIA-001
niveau: Administratif
version: "0.2 (brouillon)"
status: draft
tags: [grc, cesi, gouvernance, directive, gia, controle-acces, habilitation]
---

# Directive de gestion des identités et des accès

**Fiche signalétique**

| Code | DIR-GIA-001 |
| --- | --- |
| Titre | Directive de gestion des identités et des accès |
| Niveau | Administratif |
| Version | 0.2 (brouillon) |
| Classification | [À déterminer] |
| Entrée en vigueur | [AAAA-MM-JJ] |
| Responsable | CSIO |
| Approbation | [Autorité d’approbation] |
| Document parent | POL-GIA-001, dérivant de POL-SEC-001 (principe 7.3) |
| Filiation | Pratiques GIA du MCN -> modèle CAG -> transposition [organisation] |

## 1. Remplacement

Directive nouvelle ; ne remplace aucun document antérieur en vigueur à [organisation].

## 2. Objet

Établir les **règles obligatoires** encadrant la création, l’attribution, la modification, la revue et la révocation des identités numériques et des droits d’accès aux actifs informationnels de [organisation]. Elle opérationnalise les principes de **moindre privilège**, de **besoin d’en connaître**, d’**imputabilité** et de **séparation des tâches** énoncés dans POL-GIA-001.

## 3. Champ d’application

- l’ensemble du personnel de [organisation], permanent ou temporaire ;

- les fournisseurs, sous-traitants, stagiaires, partenaires et tiers disposant d’un accès (cf. CHECK-FOURN-001) ;

- tous les types de comptes : nominatifs, à privilèges, de service, intégrés, génériques et de machine ;

- l’ensemble des identités, habilitations et droits d’accès aux systèmes, applications, réseaux, données et environnements infonuagiques sous la responsabilité de [organisation].

Les règles de comportement de l’utilisateur (usage acceptable) relèvent de DIR-UTI-TEC-001.

## 4. Définitions

| **Terme** | **Définition** |
| --- | --- |
| Identité | Ensemble d’informations associé à un utilisateur ou à une entité, représenté par un identifiant. |
| Titulaire | Propriétaire d’une identité ; responsable de toute action posée avec celle-ci. |
| Entité | Traitement, service, machine ou toute représentation capable d’agir de façon autonome auprès d’un système. |
| Authentifiant | Information confirmant une identité, fondée sur ce que le titulaire sait, possède ou est. |
| Authentifiant secret | Authentifiant connu du seul titulaire (mot de passe, NIP). |
| Authentification | Acte confirmant une identité déclarée par concordance avec son authentifiant. |
| Authentification à deux étapes | Deux preuves d’identité (p. ex. mot de passe puis question secrète). |
| Authentification à deux facteurs (2FA / MFA) | Combinaison de deux facteurs de catégories distinctes parmi savoir, posséder, être. |
| Authentification unique (SSO) | Accès à plusieurs applications via une seule authentification. Mécanisme de fédération — pas une force d’authentification. |
| Autorisation | Attribution de droits d’accès à une identité par une autorité. |
| Habilitation / droit d’accès | Permissions techniques octroyées à une identité. À ne pas confondre avec le « droit d’accès » LPRPSP. |
| Moindre privilège | Accès limité au strict minimum requis par la fonction. |
| Séparation des tâches (SoD) | Répartition des responsabilités empêchant le contrôle total d’un processus sensible par une seule entité. |
| Compte à privilèges | Compte à droits élevés (administration, comptes intégrés, exécution de programmes de service). |
| Compte de service / intégré / générique | Compte non interactif / compte système-à-système / compte anonyme potentiellement partagé. |
| Registre des accès accordés | Répertoire consignant les permissions accordées à un compte. |
| Recertification | Revue périodique attestant que chaque droit d’accès demeure justifié. |

## 5. Modalités

### 5.1 Identité unique et imputabilité

5.1.1 Chaque utilisateur ou entité dispose d’une **identité unique** ; elle ne peut être utilisée par un autre.

5.1.2 Une identité d’entité est sous la responsabilité d’**un seul gestionnaire**.

5.1.3 Un utilisateur n’a qu’une identité, sauf si ses fonctions l’exigent ou nécessitent des privilèges élevés (compte privilégié distinct — voir 5.4).

5.1.4 Les **comptes génériques ou partagés** sont interdits par défaut ; exception documentée, justifiée, limitée dans le temps, approuvée par COMSI/CSIO, avec traçabilité.

5.1.5 Le titulaire est **responsable de toute action** posée avec son identité.

### 5.2 Octroi des droits d’accès

5.2.1 Tout octroi fait l’objet d’une **demande formelle traçable**, **préalablement autorisée** par le détenteur ou son mandataire.

5.2.2 Droits attribués selon le **moindre privilège** et le **besoin d’en connaître**, via des **profils (RBAC)**.

5.2.3 Les demandes proviennent du **gestionnaire** ; le **Responsable de l’identité et des accès** vérifie conformité et complétude avant exécution.

### 5.3 Cycle de vie de l’identité

**Arrivée** — 5.3.1 Création déclenchée par un gestionnaire autorisé, rattachée à un dossier RH/contractuel valide ; droits initiaux selon le profil.

**Mobilité** — 5.3.2 Tout changement de fonction déclenche une réévaluation ; les droits inutiles sont désactivés/verrouillés/suspendus ; cumul non justifié proscrit.

**Départ / absence prolongée** — 5.3.3 Désactivation sans délai de toutes les identités (au plus tard [X h / jour ouvrable même]) ; récupération des actifs.

**Conservation et suppression (Loi 25)** — 5.3.4 Identité **non réassignée** ; **conservée le temps strictement nécessaire** à la traçabilité, selon un calendrier, puis **détruite ou anonymisée** lorsque la finalité est atteinte (LPRPSP / Loi 25).

### 5.4 Comptes à privilèges

5.4.1 Distincts des comptes nominatifs courants.

5.4.2 Attribution restreinte, justifiée, approuvée à un niveau supérieur, fondée sur le **privilège minimal en tout temps**.

5.4.3 **MFA obligatoire** ; JIT et coffre de secrets (PAM) recommandés si disponibles.

5.4.4 Activités **surveillées** ; activité anormale signalée au détenteur ; toute tentative d’accès **journalisée**.

### 5.5 Séparation des tâches incompatibles

5.5.1 Les responsabilités d’**autorisation**, d’**utilisation** et de **surveillance** des accès sont réparties entre entités distinctes.

5.5.2 Les combinaisons incompatibles sont identifiées et bloquées, ou compensées par un contrôle de détection documenté.

### 5.6 Authentifiants

5.6.1 Confidentialité et intégrité garanties à chaque étape (saisie, émission, stockage, transmission, réception).

5.6.2 Authentifiant initial **temporaire**, à **modifier à la première authentification**.

5.6.3 Mots de passe **non réutilisables**, de qualité, renouvelés selon [norme d’authentification interne].

5.6.4 **Strictement personnels** ; partage ou divulgation interdits.

### 5.7 Authentification

5.7.1 Niveau déterminé selon la **sensibilité** et le **contexte d’usage**.

5.7.2 **MFA exigée** au minimum pour : accès distants, accès à privilèges, accès des fournisseurs, accès aux renseignements personnels ou actifs sensibles (p. ex. Profil B), applications critiques. Le SSO ne se substitue jamais à la MFA.

### 5.8 Contrôle d’accès au réseau

5.8.1 Identification/authentification de toute personne ; repérage (IDS/IPS) et **isolement** de tout équipement non autorisé.

5.8.2 Réseau **segmenté en zones** selon la sensibilité ; coupe-feu sur serveurs exposés ; seuls les **ports nécessaires** ouverts, vérifiés périodiquement.

### 5.9 Contrôle d’accès aux systèmes d’exploitation

5.9.1 Administrateur identifié par un **code unique** ; tentatives infructueuses limitées (désactivation au seuil).

5.9.2 Accès et tentatives **journalisés** avec conservation ; pas de comptes génériques pour l’administration (imputabilité).

### 5.10 Contrôle d’accès aux applications et à l’information

5.10.1 Le **détenteur** autorise les accès à son information.

5.10.2 Connexions distantes encadrées ; accès aux applications sensibles **journalisés** de façon exploitable.

5.10.3 Maintenance applicative réservée au **personnel habilité** ; interventions de sous-traitants encadrées par contrat (cf. CHECK-FOURN-001).

5.10.4 Usage des **ports USB** contrôlé.

### 5.11 Contrôle d’accès des dispositifs mobiles

5.11.1 Accès distants authentifiés **utilisateur + dispositif**.

5.11.2 Minimum : verrouillage par code obligatoire, MFA/chiffrement pour l’administration, limitation des tentatives avec retour à la normale, désactivation de l’exécution automatique de code, réseaux sans fil sécurisés.

### 5.12 Revue et recertification

5.12.1 **Recertification documentée** par les détenteurs/mandataires : accès à privilèges au moins **trimestriellement** ; accès standards **[semestriellement / annuellement]**.

5.12.2 Tout droit non justifié **retiré sans délai** ; revue conservée comme preuve d’audit.

5.12.3 **Rapport des comptes inactifs** (>6 mois) transmis périodiquement aux gestionnaires.

### 5.13 Journalisation et registre

5.13.1 Journalisation : créations/modifications/suppressions d’identités et de droits, authentifications réussies/échouées, usage des comptes à privilèges.

5.13.2 **Registre des accès accordés** tenu à jour et conservé ; journaux protégés contre l’altération, revus selon le processus GMVI.

## 6. Rôles et responsabilités

| **Rôle** | **Responsabilités** |
| --- | --- |
| CSIO | Processus formel de GIA, évolution et diffusion ; approuve les accès à privilèges sensibles. |
| Responsable de l’identité et des accès (≈ Service Bureautique) | Traite les demandes selon les règles du mandataire ; vérifie origine/complétude ; tient le registre ; soumet annuellement la liste des accès. |
| Détenteur d’actif informationnel | Gestion des profils/droits sur ses actifs ; autorise les accès à son information. |
| Mandataire désigné | Gère/autorise les droits sur ses actifs ; définit profils et règles ; révise annuellement. |
| Gestionnaire | Initie/approuve les demandes ; garantit moindre privilège et SoD ; demande modification/retrait aux mouvements ; révise ; sensibilise. |
| Utilisateur | Protège son authentifiant ; usage limité aux tâches ; signale toute tentative non autorisée ; avise des accès superflus. |
| Boîte Sécurité | Surveille journaux et comptes à privilèges ; traite les anomalies. |
| Direction de l’audit interne (si applicable) | Vérifications, contrôles et enquêtes en cas de motifs de fraude. |
| COMSI | Responsable de l’application et de la mise à jour ; tient les registres d’exception. |

## 7. Mise à jour

Révision au moins **annuelle**, ou sur changement significatif (réorganisation, incident majeur, évolution réglementaire ou technologique).

## 8. Approbation

| **Fonction** | **Nom** | **Date** | **Signature** |
| --- | --- | --- | --- |
| [Autorité d’approbation] | [Nom] | [AAAA-MM-JJ] |  |

## 9. Références normatives

- ISO/IEC 27001:2022 et 27002:2022 — gestion des identités et des accès (5.15-5.18, 8.2, 8.3, 8.5 — numéros à confirmer au texte).

- NIST CSF 2.0 — catégorie PR.AA.

- CIS Controls v8 — Contrôle 5 et Contrôle 6.

- **LGGRI** (RLRQ c. G-1.03) et **Directive gouvernementale sur la sécurité de l’information (décret 1514-2021)** — applicables en tant qu’organisme public (cf. POL-SEC-001).

- **Loi 25** modifiant la **LPRPSP** (RLRQ c. P-39.1) et la **Loi sur l’accès** (RLRQ c. A-2.1).

- Filiation : pratiques GIA du MCN, transposées via le modèle CAG.

