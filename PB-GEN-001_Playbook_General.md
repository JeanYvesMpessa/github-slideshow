---
title: "PB-GEN-001 Playbook General"
source: "PB-GEN-001_Playbook_General.docx"
---

Codification

PB-GEN-001

Entrée en vigueur

Mars 2026

Mise à jour

[Date]

PLAYBOOK

Incidents d’ingénierie sociale – Playbook général unifié

Tous les acteurs

📋 Alignement cadre :  NIST CSF 2.0 / SP 800-61r3  │  ISO/IEC 27035:2023  │  CIS Controls v8 (Contrôle 17)

1. Architecture de la suite documentaire

Ce playbook général constitue la synthèse opérationnelle pour la gestion des incidents d’ingénierie sociale. Il couvre les sept vecteurs retenus par POL-SEC-001 et s’aligne sur le processus GMVI du MCN/CGCD.

POL-SEC-001

Politique – principes, menaces visées, cadre normatif GMVI

DIR-SEC-001

Directive – niveaux GMVI, obligations de déclaration, délais, RACI

PROC-SEC-001

Procédure employés – vecteurs, reconnaissance, consignes par situation

PB-BUR-001

Service Bureautique – réception, qualification, transmission, actions techniques

PB-SEC-001

Boîte Sécurité – triage, analyse, forensique, notifications GMVI

PB-COMSI-001

COMSI – rend compte au CSIO (hiérarchie interne) | coordination N1-N3, déclaration ROCD (N2+, flux GMVI externe), cellule de crise, KPI

PB-CSIO-001

CSIO – décisions stratégiques, communications, conformité GMVI

PB-GEN-001

Synthèse – cycle de vie, grille de triage, checklist universelle

2. Vecteurs couverts — famille Ingénierie sociale

Vecteur

Spécificité opérationnelle clé

hameçonnage (phishing)

Signaler .eml/.msg. Ne pas transférer à des collègues.

harponnage (spear phishing)

Attention accrue : contenu personnalisé peut tromper même les employés vigilants.

Fraude au président (BEC)

Rappel virement en urgence si virement effectué. Fenêtre très courte.

Hameçonnage par SMS (smishing)

Conserver le numéro. Signaler par courriel à la Boîte Sécurité.

Hameçonnage vocal (vishing)

Raccrocher. Ne jamais accorder un accès à distance à un appelant entrant.

Hameçonnage par QR (quishing)

Ne pas scanner un QR code d’origine inconnue. Photographier pour analyse.

Usurpation d’identité interne

Vérifier l’identité par un canal différent avant toute action inhabituélle.

3. Cycle de vie intégré — Vue par acteur

La matrice suivante présente les actions par phase et par acteur. Elle constitue la référence opérationnelle centrale. La colonne COMSI inclut les obligations GMVI de déclaration au ROCD.

Phase

Employé

Svc Bureautique

Boîte Sécurité

COMSI

CSIO

1. Détection

Identifier, ne pas interagir

Recevoir signalement

Accuser réception

Aviser si N2+

(informé)

2. Signalement
&lt; 30 min

Signaler — tout vecteur

Transmettre + formulaire

Ouvrir dossier MVI

(aviser si N2+)

(informé)

3. Triage
&lt; 1 h

Rester disponible

Assistance technique

Classifier GMVI, IOC

Valider classification

(informé)

4. Confinement

Ne pas utiliser le poste

Isoler si N2+

Coordonner analyse

Informer CSIO + Déclarer ROCD (N2+, flux GMVI)

Approuver décisions

5. Éradication

Attendre instructions

Soutien forensique

Analyse, root cause

Superviser + ROCD

Valider conclusions

6. Reprise

Recevoir poste si requis

Reconfigurer, tester

Valider rétablissement

Autoriser reprise

Approuver retour

7. Clôture

Répondre questionnaire

Documenter actions

Rapport 5 jours (N1-2)
Bilan 30 j (N3-4)

Revue post-incident

Approuver rapport

8. Amélioration

Suivre formation

MAJ procédures

MAJ playbooks + IOC

Proposer améliorations

Approuver MAJ

4. Grille de triage décisionnel GMVI

⚠️ Règle d’or :  En cas de doute sur la classification, appliquer le niveau supérieur. Un incident d’ingénierie sociale ne s’auto-résout jamais.

Situation détectée

Niveau GMVI

Action immédiate

Message suspect — aucune interaction

1 – OP interne

Signaler. Consigner. Informer ROCD.

Clic sur lien — aucune saisie / QR scanné sans saisie

1 ou 2

Analyse poste. Évaluer niveau. COMSI avise ROCD.

Identifiants / MdP saisis

2

Isolation. Réinit. MdP. COMSI déclare ROCD.

Pièce jointe exécutée / accès distance accordé

2

Isolation. Forensique. COMSI déclare ROCD.

Virement effectué (BEC)

2 ou 3

Rappel virement (urgence). COMSI déclare ROCD.

Données sensibles / personnelles exfiltrées

2 ou 3

Isolation. COMSI déclare ROCD + évalue Loi 25.

Plusieurs employés / systèmes touchés

2 ou 3

COMSI déclare ROCD. Évaluer niveau 3 si propagation.

5. Chronologie des délais obligatoires

Délai

Action requise

Responsable

Référence

Immédiat

Isolation de l’appareil (si interaction N2+)

Employé + Svc Bureautique

PROC-SEC-001

Sans délai

Signalement + déclaration ROCD (N2+)

Employé + COMSI

GMVI – DIR-SEC-001

&lt; 30 min

Transmission Boîte Sécurité + dossier MVI ouvert

Service Bureautique

PB-BUR-001

&lt; 1 heure

Triage + classification GMVI confirmée

Boîte Sécurité

PB-SEC-001

&lt; 1 heure

Notification CSIO (N2+)

COMSI

PB-COMSI-001

Toutes 2 h

Mise à jour journal d’incident

Boîte Sécurité

DIR-SEC-001

5 jours ouvr.

Rapport de clôture interne (N1-N2)

Boîte Sécu. + COMSI

DIR-SEC-001

30 jours

Bilan formel GMVI (N3-N4)

COMSI + CSIO + Instance GMVI

GMVI

2 semaines

Rapport firme externe au CERT/AQ

COMSI / CSIO

GMVI

6 mois

Vérification application recommandations

COMSI

GMVI

6. Checklist universelle de réponse

Aide-mémoire rapide pour tout acteur. Ne remplace pas les playbooks spécifiques par rôle.

✔

Phase

Action

Responsable

□

Détection

Identifier le vecteur et ne pas interagir

Employé

□

Signalement

Contacter Svc Bureautique ou Boîte Sécurité

Employé

□

Isolation (N2+)

Déconnecter l’appareil du réseau

Employé + Svc Bur.

□

Collecte initiale

Recueillir infos + message/numéro/QR

Svc Bureautique

□

Transmission

Formulaire standardisé à Boîte Sécurité

Svc Bureautique

□

Triage GMVI

Classifier et ouvrir le dossier MVI

Boîte Sécurité

□

Analyse technique

IOC, URL, hash, forensique si N2+

Boîte Sécurité

□

Déclaration ROCD

Sans délai si N2+ (via COMSI)

COMSI

□

BEC uniquement

Rappel virement — urgence institution financière

COMSI + CSIO

□

PRP impliquées

Évaluer obligation Loi 25 / CAI

CSIO + RPRP

□

Réinitialisation

Réinitialiser identifiants compromis (N2+)

TI + Boîte Sécu.

□

Reprise

Vérifier avant remise en service

Svc Bur. + COMSI

□

Rapport clôture

5 jours (N1-N2) / 30 jours (N3-N4)

Boîte Sécu. + COMSI

□

Revue PIR

Post-incident dans les 10 jours (N2+)

COMSI + CSIO

□

Amélioration

MAJ playbooks, formation, IOC

COMSI + CSIO

7. Principes fondamentaux

🚫 Principe 1 :  Les cadres et la direction sont des cibles prioritaires (BEC, harponnage). Aucun niveau hiérarchique ne confère l’immunité.

🚫 Principe 2 :  Signaler est un acte responsable. Aucune représaille pour un signalement de bonne foi.

🚫 Principe 3 :  La déclaration au ROCD (N2+) n’est pas une escalade optionnelle — c’est une obligation GMVI. Le COMSI ne peut y substituer une escalade interne.

🚫 Principe 4 :  Pour la fraude au président : la fenêtre de rappel d’un virement est extrêmement courte. Tout signalement de BEC est traité comme une urgence absolue.

Approbation

Fonction

Nom

Signature

Date

[Titre]

[Prénom Nom]

📎 Suite documentaire complète :  POL-SEC-001  |  DIR-SEC-001  |  PROC-SEC-001  |  PB-BUR-001  |  PB-SEC-001  |  PB-COMSI-001  |  PB-CSIO-001  |  PB-GEN-001
