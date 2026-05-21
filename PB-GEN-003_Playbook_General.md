---
title: "PB-GEN-003 Playbook General"
source: "PB-GEN-003_Playbook_General.docx"
---

Codification

PB-GEN-003

Entrée en vigueur

Mars 2026

Mise à jour

[Date]

PLAYBOOK

Données, accès et appareils – Playbook général unifié

Tous les acteurs

📋 Alignement cadre :  NIST CSF 2.0 / SP 800-61r3  │  ISO/IEC 27035:2023  │  CIS Controls v8 (Contrôle 17)

1. Architecture de la suite documentaire

POL-SEC-001

Politique – principes, menaces visées, cadre normatif GMVI

DIR-SEC-001

Directive – niveaux GMVI, obligations de déclaration, délais, RACI

PROC-SEC-003

Procédure – 8 vecteurs, consignes par situation, obligations Loi 25

PB-BUR-003

Service Bureautique – qualification, actions techniques ciblées par vecteur

PB-SEC-003

Boîte Sécurité – triage, forensique, évaluation PRP, notifications

PB-COMSI-003

COMSI – rend compte au CSIO (hiérarchie interne) | coordination, déclaration ROCD (N2+, flux GMVI externe), obligations Loi 25, incidents internes

PB-CSIO-003

CSIO – décision CAI, incidents internes, conformité GMVI + Loi 25

PB-GEN-003

Synthèse – cycle de vie, grille de triage, checklist universelle

2. Spécificités critiques de cette famille

🚨 Différence fondamentale vs familles 1 et 2 :  Cette famille se caractérise par la nature silencieuse des incidents. Le premier réflexe n’est PAS l’isolation mais le SIGNALEMENT et la QUALIFICATION. La première question est : des renseignements personnels sont-ils impliqués?

🚨 Double obligation N2+ :  1° Hiérarchie interne : informer le CSIO sans délai | 2° GMVI externe : déclarer au ROCD sans délai | 3° Loi 25 : si PRP impliquées, informer CSIO + RPRP pour évaluation et déclaration CAI sans délai si préjudice sérieux.

🚨 Incident interne — règle absolue :  Ne jamais confronter un employé suspecté sans coordination RH + Juridique. Préserver les preuves avant toute action disciplinaire.

3. Vecteurs couverts — spécificités opérationnelles clés

Vecteur

Point critique opérationnel

Fuite de données (erreur)

Signaler. Ne pas tenter de rappeler seul. Évaluer Loi 25 immédiatement.

Fuite malveillante (employé)

Préserver les preuves. Contacter Sécurité + RH + Juridique avant toute action.

Accès non autorisé

Révoquer accès. Consigner logs AVANT réinitialisation. Évaluer Loi 25.

Destruction de données

NE PAS restaurer avant forensique. Identifier sauvegardes saines.

Intrusion réseau active

Isoler le segment. Signaler. Forensique réseau.

Compte compromis

Révoquer session. Forensique du compte. Évaluer impact.

Compte admin compromis / abus

SUSPENDRE immédiatement. COMSI déclare ROCD d’urgence.

Appareil perdu non chiffré + données

Effacement MDM. COMSI déclare ROCD. Évaluer Loi 25.

Appareil perdu chiffré

Effacement MDM précautionnel. Signaler. Consigner. N1.

Wi-Fi non sécurisé

Changer MdP des services accédés. Signaler. Consigner.

4. Cycle de vie intégré — Vue par acteur

La phase 5 (Obligation Loi 25) est propre à cette famille et n’a pas d’équivalent dans les familles 1 et 2.

Phase

Employé

Svc Bureautique

Boîte Sécurité

COMSI

CSIO

1. Découverte

Découvrir et NE PAS modifier

Recevoir signalement

Accuser réception

Aviser si N2+

(informé)

2. Signalement
immédiat

Signaler — ne pas résoudre seul

Qualifier impact + PRP

Ouvrir dossier MVI

Informer CSIO + Déclarer ROCD (N2+, flux GMVI)

Informer RPRP si PRP

3. Analyse
&lt; 2h

Fournir informations

Forensique accès + comptes

Qualifier PRP, volume, impact

Valider classification

Évaluer Loi 25

4. Containment
(si requis)

Suspendre l’usage suspecté

Révoquer accès + effac. MDM

Coordonner containment

Valider actions

Approuver décisions

5. Obligation
Loi 25

Éventuellement informé

Preuves pour RPRP

Documenter pour CAI

Coordonner RPRP + CSIO

Déclarer CAI + notifier

6. Reprise

Recevoir accès rétabli

Rétablir accès + tester

Valider rétablissement

Autoriser reprise

Approuver retour

7. Clôture

Répondre questionnaire

Documenter actions

Rapport 5j / Bilan 30j

Revue post-incident

Approuver rapport

8. Amélioration

Formation

MAJ procédures

MAJ playbooks, IAM

Principe moindre privilège

Approuver MAJ

5. Grille de triage décisionnel GMVI

⚠️ Obligation GMVI :  Toute MVI de niveau 2 et plus doit être portée à la connaissance du CSIO (hiérarchie interne OP) ET déclarée au ROCD (obligation GMVI externe) sans délai par le COMSI. Ces deux obligations sont simultanées. La présence de renseignements personnels déclenche systématiquement l’évaluation Loi 25.

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

6. Processus d’évaluation Loi 25 — arbre décisionnel

Question

Si OUI — action requise

Des renseignements personnels ont-ils été accédés, divulgués, copiés ou volés?

Informer le RPRP et le CSIO immédiatement.

L’atteinte est-elle susceptible de causer un préjudice sérieux?

Déclarer à la CAI SANS DÉLAI (Loi 25, art. 63.8).

Des personnes physiques sont-elles identifiables?

Notifier les personnes concernées sans délai.

L’atteinte est-elle consignée au registre?

Obligation systématique, même sans préjudice sérieux (RPRP).

7. Chronologie des délais obligatoires

Délai

Action requise

Responsable

Référence

Immédiat

Révoquer accès si admin compromis / intrusion active

Svc Bureautique

PROC-SEC-003

Sans délai

Signalement + déclaration ROCD (N2+)

Employé + COMSI

GMVI – DIR-SEC-001

&lt; 2 heures

Qualifier la présence de PRP

Boîte Sécurité

Loi 25

Sans délai dès qualification

Informer RPRP si PRP présentes

CSIO

Loi 25

Sans délai dès confirmation

Déclarer à la CAI (si préjudice sérieux)

CSIO + RPRP

Loi 25, art. 63.8

Toutes 2 h (N3+)

Mise à jour journal d’incident

Boîte Sécurité

DIR-SEC-001

5 jours ouvr.

Rapport de clôture interne (N1-N2)

Boîte Sécu. + COMSI

DIR-SEC-001

30 jours

Bilan formel GMVI (N3-N4)

COMSI + CSIO

GMVI

2 semaines

Rapport firme externe au CERT/AQ

COMSI / CSIO

GMVI

6 mois

Vérification recommandations prioritaires

COMSI

GMVI

8. Checklist universelle de réponse

✔

Phase

Action

Responsable

□

Découverte

Signaler immédiatement — ne pas résoudre seul

Employé

□

Exception active

Suspendre compte admin / isoler réseau si actif

Svc Bureautique

□

Préserver preuves

Ne pas supprimer, modifier ni confronter avant Sécurité

Tous

□

Qualification

Identifier type, données, comptes, systèmes

Svc Bureautique

□

Transmettre

Formulaire standardisé à Boîte Sécurité

Svc Bureautique

□

Triage GMVI

Classifier et ouvrir le dossier MVI

Boîte Sécurité

□

PRP présentes?

Qualifier dans les 2 h. Alerter CSIO + RPRP.

Boîte Sécurité

□

Déclaration ROCD

Sans délai si N2+ (via COMSI)

COMSI

□

CAI (si requis)

Déclarer sans délai si préjudice sérieux

CSIO + RPRP

□

Incident interne

Coordonner RH + Juridique avant toute action

COMSI + CSIO

□

Appareil perdu

Effacement MDM + révocation accès + inventaire

Svc Bureautique

□

Containment

Révoquer accès, bloquer canaux de fuite, isoler

Boîte Sécu. + Svc Bur.

□

Reprise

Vérifier avant rétablissement des accès

Svc Bur. + COMSI

□

Rapport clôture

5 jours (N1-N2) / 30 jours (N3-N4)

Boîte Sécu. + COMSI

□

Revue PIR

Dans les 10 jours (N2+)

COMSI + CSIO

□

Amélioration

MAJ playbooks, IAM, chiffrement, moindre privilège

COMSI + CSIO

9. Principes fondamentaux

🚫 Principe 1 :  Signaler d’abord, qualifier ensuite. La première action pour cette famille n’est pas l’isolation mais le signalement et la qualification de l’impact.

🚫 Principe 2 :  La Loi 25 s’applique même aux erreurs non malveillantes. Un courriel mal envoyé contenant des renseignements personnels est une atteinte au sens de la loi.

🚫 Principe 3 :  La déclaration au ROCD (N2+) et la déclaration à la CAI (si préjudice sérieux) sont deux obligations indépendantes avec des délais distincts. Les deux doivent être gérées simultanément.

🚫 Principe 4 :  Ne jamais confronter un employé suspecté sans coordination avec RH et le conseiller juridique. Une action prématurée peut détruire les preuves et exposer l’organisation.

Approbation

Fonction

Nom

Signature

Date

[Titre]

[Prénom Nom]

📎 Suite documentaire complète :  POL-SEC-001  |  DIR-SEC-001  |  PROC-SEC-003  |  PB-BUR-003  |  PB-SEC-003  |  PB-COMSI-003  |  PB-CSIO-003  |  PB-GEN-003  |  Loi 25 (art. 63.7 à 63.11)
