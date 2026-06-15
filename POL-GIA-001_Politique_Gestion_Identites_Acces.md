---
title: POL-GIA-001 — Politique de gestion des identités et des accès
code: POL-GIA-001
niveau: Administratif
version: "0.1 (brouillon)"
status: draft
tags: [grc, cesi, gouvernance, politique, gia, controle-acces, identite]
---

# Politique de gestion des identités et des accès

**Fiche signalétique**

| Code | POL-GIA-001 |
| --- | --- |
| Titre | Politique de gestion des identités et des accès |
| Niveau | Administratif |
| Version | 0.1 (brouillon) |
| Classification | [À déterminer] |
| Document parent | POL-SEC-001 — Politique de sécurité de l’information (principe directeur 7.3) |
| Documents enfants | DIR-GIA-001 (Directive), PROC-GIA-001 (Procédure) |
| Approbation | [Autorité d’approbation] |

## 1. Remplacement

Politique nouvelle ; ne remplace aucun document antérieur de [organisation].

## 2. Contexte

La gestion des identités et des accès (GIA) est un contrôle de sécurité de **première importance** : elle détermine qui accède à quelle information, et pendant combien de temps. Comme les habilitations s’accumulent au fil du temps (mobilités, projets, exceptions), une gestion rigoureuse du cycle de vie est nécessaire. À défaut, [organisation] s’expose notamment à : l’utilisation illicite d’un accès après un départ, la destruction ou la modification de données non autorisée, la fuite de renseignements confidentiels, et l’usurpation d’identité.

La présente politique découle de la PSI faîtière POL-SEC-001 (principe directeur 7.3 — Gestion des accès). Elle est opérationnalisée par DIR-GIA-001 et PROC-GIA-001.

## 3. Objet

Établir les **principes directeurs**, le périmètre et les responsabilités macro encadrant la gestion des identités numériques et des droits d’accès aux actifs informationnels de [organisation], tout au long de leur cycle de vie.

## 4. Champ d’application

Toutes les identités (personnel, tiers, entités, comptes de service) et tous les droits d’accès aux actifs informationnels — systèmes, applications, réseaux, données, environnements infonuagiques — sous la responsabilité de [organisation]. Les règles de comportement de l’utilisateur (usage acceptable) relèvent de DIR-UTI-TEC-001.

## 5. Définitions

| **Terme** | **Définition** |
| --- | --- |
| Identité | Ensemble d’informations associé à un utilisateur ou à une entité, représenté par un identifiant. |
| Habilitation / droit d’accès | Permissions techniques octroyées à une identité. À ne pas confondre avec le « droit d’accès » LPRPSP (droit de la personne concernée à ses renseignements personnels). |
| Moindre privilège | Accès limité au strict minimum requis par la fonction. |
| Besoin d’en connaître | Accès à l’information réservé à ceux dont les fonctions l’exigent. |
| Séparation des tâches (SoD) | Répartition des responsabilités empêchant un contrôle total d’un processus sensible par une seule entité. |
| Détenteur | Personne ayant la garde d’un actif informationnel ; autorise les accès à celui-ci. |
| Mandataire | Personne désignée par le détenteur pour gérer les accès à l’actif. |

## 6. Principe général

L’accès aux actifs informationnels de [organisation] est accordé **uniquement selon le nécessaire à l’exercice des fonctions**, à des **identités uniques et imputables**, sous l’autorisation du détenteur, et fait l’objet d’une **revue régulière** depuis la création de l’identité jusqu’à sa désactivation et sa destruction.

## 7. Principes directeurs

- **Identité unique et imputable** — chaque identité est nominative ; toute action est rattachable à un titulaire responsable. Pas de comptes génériques ou partagés par défaut.

- **Moindre privilège et besoin d’en connaître** — droits attribués au strict nécessaire, via des profils (RBAC).

- **Séparation des tâches** — les rôles d’autorisation, d’utilisation et de surveillance des accès sont répartis entre des entités distinctes.

- **Gouvernance des accès par le détenteur** — tout accès est préalablement autorisé par le détenteur de l’actif ou son mandataire.

- **Authentification proportionnée au risque** — la force d’authentification (jusqu’à la MFA) est fonction de la sensibilité de l’information et du contexte (accès distant, privilégié, fournisseur, Protégé B).

- **Revue et recertification** — les habilitations sont revues périodiquement ; tout droit non justifié est retiré.

- **Traçabilité** — les opérations sur les identités/accès et l’usage des comptes à privilèges sont journalisés et conservés.

- **Conformité Loi 25** — l’accès aux renseignements personnels est limité au nécessaire ; les identités sont conservées de façon bornée puis détruites ou anonymisées lorsque la finalité est atteinte.

- **Amélioration continue** — la GIA repose sur quatre volets : encadrement, gestion, contrôle, surveillance (reddition de comptes aux autorités).

- **Pas de mécanisme « maison »** pour l’authentification — recours aux mécanismes éprouvés et conformes.

## 8. Rôles et responsabilités

| **Rôle** | **Responsabilités** |
| --- | --- |
| CSIO | Porte la politique ; s’assure de l’existence d’un processus formel de GIA. |
| COMSI | Responsable de l’application et de la mise à jour. |
| Détenteur / Mandataire | Autorisent et gouvernent les accès à leurs actifs. |
| Gestionnaire | Garantit le moindre privilège et la SoD pour son personnel. |
| Utilisateur | Respecte la politique ; protège ses authentifiants. |
| Direction de l’audit interne (si applicable) | Vérifie la conformité. |

## 9. Mise à jour

Révision au moins annuelle ou sur changement significatif.

## 10. Approbation

| **Fonction** | **Nom** | **Date** | **Signature** |
| --- | --- | --- | --- |
| [Autorité d’approbation] | [Nom] | [AAAA-MM-JJ] |  |

## Annexe — Chaîne normative

POL-SEC-001 (PSI faîtière) -> POL-GIA-001 -> DIR-GIA-001 -> PROC-GIA-001

Cadre légal (organisme public) : LGGRI (G-1.03) · Directive 1514-2021 · Loi 25 (LPRPSP P-39.1 + Loi sur l’accès A-2.1)

Référentiels : ISO/IEC 27002:2022 (5.15-5.18) · NIST CSF 2.0 (PR.AA) · CIS v8 (C5, C6)

Filiation : pratiques GIA du MCN -> modèle CAG -> transposition [organisation]

