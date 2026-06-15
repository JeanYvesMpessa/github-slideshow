---
title: PROC-GIA-001 — Procédure de gestion des identités et des accès
code: PROC-GIA-001
niveau: Opérationnel
version: "0.1 (brouillon)"
status: draft
tags: [grc, cesi, gouvernance, procedure, gia, controle-acces, cycle-vie]
---

# Procédure de gestion des identités et des accès

**Fiche signalétique**

| Code | PROC-GIA-001 |
| --- | --- |
| Titre | Procédure de gestion des identités et des accès |
| Niveau | Opérationnel |
| Version | 0.1 (brouillon) |
| Classification | [À déterminer] |
| Cadre d’autorité | DIR-GIA-001 |
| Approbation | [Autorité d’approbation] |

## 1. Remplacement

Procédure nouvelle ; ne remplace aucun document antérieur de [organisation].

## 2. Objet

Décrire la **séquence opérationnelle** de gestion du cycle de vie des identités et des droits d’accès : demande, validation, octroi, usage, revue, mobilité et révocation, conformément à DIR-GIA-001.

## 3. Champ d’application

Tout traitement d’une demande d’identité ou d’habilitation visant un actif informationnel de [organisation], pour le personnel, les tiers et les entités.

## 4. Définitions

Se référer aux définitions de DIR-GIA-001. Acteurs clés : **Gestionnaire** (demandeur), **Responsable de l’identité et des accès** (traitement), **Détenteur / Mandataire** (autorisation), **Titulaire** (utilisateur).

## 5. Prérequis

- Profils d’accès (RBAC) définis par les mandataires

- **Registre des accès accordés** en place

- Canal de demande formel et traçable

- Système de gestion des identités opérationnel

## 6. Instructions — séquence opérationnelle

### Phase 1 — Demande

- Le **gestionnaire** soumet une demande formelle pour l’identité de son personnel ou d’une entité sous sa responsabilité.

- La demande précise : profil/fonction visée, actifs concernés, justification (besoin d’en connaître), durée si temporaire.

### Phase 2 — Validation

- Le **Responsable de l’identité et des accès** vérifie que la demande **provient du gestionnaire** de l’utilisateur et qu’elle est **complète**.

- Il valide la conformité au **profil défini par le mandataire**. En cas de discordance, il valide auprès du mandataire avant toute suite.

- Les demandes **non conformes** sont retournées ou escaladées au mandataire.

### Phase 3 — Octroi

- Création ou modification de l’identité et attribution des habilitations selon le **moindre privilège**.

- Délivrance d’un **authentifiant temporaire**, à modifier à la première authentification.

- Activation de la **MFA** si l’accès l’exige (distant, privilégié, fournisseur, RP/Protégé B).

- **Consignation au Registre des accès accordés** (demande + accès attribués).

### Phase 4 — Usage et surveillance

- Le titulaire n’utilise l’accès que pour ses tâches assignées et avise son gestionnaire lorsqu’un accès n’est plus nécessaire.

- Les **comptes à privilèges** font l’objet d’une surveillance ; toute activité anormale est signalée au détenteur.

### Phase 5 — Mobilité (changement de fonction)

- À tout changement de fonction, le gestionnaire **demande la modification/retrait** des accès devenus inutiles.

- Les droits sont réévalués selon le nouveau profil ; le cumul non justifié est retiré.

### Phase 6 — Revue et recertification

- Le Responsable de l’identité et des accès **soumet annuellement** aux mandataires la liste des identités et accès autorisés sur leurs actifs.

- Le mandataire/gestionnaire **recertifie** : accès à privilèges au moins trimestriellement, accès standards [semestriellement/annuellement].

- Tout droit non justifié est **retiré sans délai** ; la revue est consignée.

- Traitement du **rapport des comptes inactifs** (>6 mois).

### Phase 7 — Départ / absence prolongée (révocation)

- **Désactivation, verrouillage ou suspension sans délai** de toutes les identités associées (au plus tard [X h / jour ouvrable même]).

- Récupération des actifs (postes, jetons, supports).

- **Aucune réassignation** de l’identité à un autre utilisateur.

- **Conservation bornée (Loi 25)** : conservation le temps strictement nécessaire à la traçabilité, puis **destruction ou anonymisation** selon le calendrier de conservation.

### Phase 8 — Journalisation et clôture

- Journalisation de l’opération (création/modification/révocation).

- Mise à jour du Registre des accès accordés.

- En cas d’anomalie ou de tentative d’accès non autorisée : signalement à securite@[organisation].ca.

## 7. Rôles et responsabilités

| **Rôle** | **Responsabilités** |
| --- | --- |
| Gestionnaire | Phases 1, 5 ; demande modification/retrait. |
| Responsable de l’identité et des accès | Phases 2, 3, 6 ; tient le registre. |
| Détenteur / Mandataire | Définit les profils ; autorise ; recertifie (phase 6). |
| Titulaire (utilisateur) | Phase 4 ; signale anomalies et accès superflus. |
| Boîte Sécurité | Surveillance (phase 4), traitement des anomalies (phase 8). |

## 8. Mise à jour

Révision au moins annuelle ou sur changement significatif du processus.

## 9. Approbation

| **Fonction** | **Nom** | **Date** | **Signature** |
| --- | --- | --- | --- |
| [Autorité d’approbation] | [Nom] | [AAAA-MM-JJ] |  |

## Références croisées

- DIR-GIA-001 — cadre d’autorité

- POL-GIA-001 — principes

- POL-SEC-001 — PSI faîtière (principe 7.3)

- Registre des accès accordés (gabarit à produire — équivalent JOURN-TRF-001 pour la GIA)

