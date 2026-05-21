---
title: "PB-GEN-002 Playbook General"
source: "PB-GEN-002_Playbook_General.docx"
---

Codification

PB-GEN-002

Entrée en vigueur

Mars 2026

Mise à jour

[Date]

PLAYBOOK

Logiciels malveillants et exploitation technique – Playbook général unifié

Tous les acteurs

📋 Alignement cadre :  NIST CSF 2.0 / SP 800-61r3  │  ISO/IEC 27035:2023  │  CIS Controls v8 (Contrôle 17)

1. Architecture de la suite documentaire

POL-SEC-001

Politique – principes, menaces visées, cadre normatif GMVI

DIR-SEC-001

Directive – niveaux GMVI, obligations de déclaration, délais, RACI

PROC-SEC-002

Procédure – vecteurs, détection, consignes par situation (13 vecteurs)

PB-BUR-002

Service Bureautique – isolation, formulaire, actions techniques N1-N3

PB-SEC-002

Boîte Sécurité – forensique, triage, réponse par vecteur, notifications

PB-COMSI-002

COMSI – rend compte au CSIO (hiérarchie interne) | coordination, déclaration ROCD (N2+, flux GMVI externe), PCA, gestion vuln. GMVI

PB-CSIO-002

CSIO – PCA, rançon, communications, conformité GMVI

PB-GEN-002

Synthèse – cycle de vie, grille de triage, checklist universelle

2. Spécificités critiques de cette famille

🚨 Règle N° 1 — Isolation avant tout :  Pour tout logiciel malveillant (malware) actif ou exploitation technique : ISOLER DU RÉSEAU AVANT toute autre action. Avant de redémarrer, éteindre, scanner ou alerter. L’isolation est la seule action que l’employé effectue seul.

🚨 Règle N° 2 — Ne jamais éteindre sans autorisation :  Un éteignage détruit les traces mémoire essentielles. Exception : rançongiciel qui chiffre activement ET impossible d’isoler autrement, sur décision de la Boîte Sécurité.

🚨 Règle N° 3 — Rançongiciel = niveau 3 par défaut :  Tout incident impliquant un rançongiciel est classé N3 (GMVI) jusqu’à évaluation contraire. La déclaration au ROCD est immédiate et obligatoire. Ne jamais recommander le paiement sans consultation CGCD + Juridique.

3. Vecteurs couverts — spécificités opérationnelles clés

Vecteur

Point critique opérationnel

Rançongiciel

Isolation réseau IMMED. Ne pas éteindre. Ne pas payer sans CGCD + Juridique.

logiciel sans fichier (fileless malware)

Image mémoire AVANT isolation sinon preuves perdues définitivement.

Logiciel furtif (rootkit)

OS non fiable pour l’analyse. Outils forensiques spécialisés obligatoires.

logiciel espion (spyware) / enregistreur de frappes (keylogger)

Ne pas changer le mot de passe sur le système suspect — le enregistreur de frappes (keylogger) le capturera.

CVE exploitée

Ne pas appliquer un correctif (patcher) sans coordination — cela peut masquer les traces. Délai 14 jours CGCD.

Injection SQL / XSS

Bloquer la session/entrée, consigner logs, NE PAS corriger avant l’analyse forensique.

DoS / DDoS

Mitigation réseau d’abord. Évaluer PCA si services critiques impactés.

cryptominage non autorisé (cryptojacking)

Ne pas tuer les processus manuellement avant l’analyse — perte de preuves.

4. Cycle de vie intégré — Vue par acteur

L’isolation réseau apparaît en phase 2, avant même le signalement formel — c’est la seule action que l’employé effectue seul et immédiatement.

Phase

Employé

Svc Bureautique

Boîte Sécurité

COMSI

CSIO

1. Détection

Détecter comportement anormal

Recevoir alerte / signalement

Accuser réception

Aviser si N2+

(informé)

2. Isolation
immédiate

Isoler du réseau AVANT
tout le reste

Isoler physiquement + étiquette

Confirmer isolation élargie

Valider périmètre

(informé)

3. Signalement
&lt; 30 min

Signaler par téléphone

Transmettre formulaire

Ouvrir dossier MVI

Informer CSIO + Déclarer ROCD (N2+, flux GMVI)

Approuver décisions

4. Analyse
&lt; 1h (N2+)

Attendre instructions

Image mémoire + logs

Forensique, IOC, root cause

Coordonner + ROCD

Valider conclusions

5. Éradication

Ne pas utiliser système

Nettoyage sur instruction

Valider éradication complète

Superviser + gestion des correctifs (patch management)

Approuver reprise

6. Reprise

Recevoir système si requis

Reconfigurer + tester

Valider rétablissement

Autoriser reprise + PCA

Approuver retour

7. Clôture

Répondre questionnaire

Documenter actions

Rapport 5j (N1-2)
Bilan 30j (N3-4)

Revue post-incident

Approuver rapport

8. Amélioration

Formation

MAJ procédures

MAJ playbooks + IOC

Patch + contrôles

Approuver MAJ

5. Grille de triage décisionnel GMVI

⚠️ Obligation GMVI :  Toute MVI de niveau 2 et plus doit être déclarée au ROCD sans délai par le COMSI. Le rançongiciel en propagation est présumé niveau 3 jusqu’à preuve du contraire.

Situation détectée

Niveau GMVI

Action immédiate

logiciel malveillant (malware) détecté et mis en quarantaine auto — système unique

1

Signaler. Consigner. COMSI informe ROCD.

logiciel malveillant (malware) actif non contenu — système unique

1 ou 2

Isolation. Signaler. Évaluer propagation.

Propagation détectée — plusieurs systèmes

2

Isolation élargie. COMSI déclare ROCD.

Rançongiciel actif / chiffrement en cours

3 présumé

ISOLATION IMMED. Ne PAS éteindre. COMSI déclare ROCD. PCA.

Exfiltration de données confirmée

2 ou 3

Isolation. COMSI déclare ROCD. Loi 25 évaluation.

Exploitation CVE — système compromis

2

Isolation. Forensique. COMSI déclare ROCD.

DoS / DDoS actif — service indisponible

2 ou 3

Mitigation réseau. PCA si critique. COMSI déclare ROCD.

Injection SQL / XSS confirmée — app web

2

Bloquer session/entrée. Consigner logs. COMSI déclare ROCD.

Infrastructure gouvernementale affectée

3 ou 4

COMSI déclare ROCD d’urgence. Formulaire MVI obligatoire.

6. Chronologie des délais obligatoires

Délai

Action requise

Responsable

Référence

Immédiat

Isolation réseau du système affecté

Employé + Svc Bureautique

PROC-SEC-002

&lt; 30 min

Signalement + triage + notification COMSI

Boîte Sécurité

PB-SEC-002

Sans délai (N2+)

Déclaration au ROCD par le COMSI

COMSI

GMVI – DIR-SEC-001

&lt; 1 heure (N2+)

Image mémoire + analyse initiale

Boîte Sécurité

PB-SEC-002

Toutes 2 h (N3+)

Mise à jour journal d’incident

Boîte Sécurité

DIR-SEC-001

14 jours civils

Rapport avancement remédiation CVE au CGCD

COMSI

GMVI – DIR-SEC-001

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

7. Checklist universelle de réponse

✔

Phase

Action

Responsable

□

Isolation

Débrancher réseau AVANT TOUT (N1+)

Employé

□

Préserver

Ne pas éteindre, ne pas modifier le système

Employé

□

Signaler

Téléphone au Svc Bureautique ou Boîte Sécurité

Employé

□

Qualifier

Recueillir infos, classifier GMVI

Svc Bureautique

□

Transmettre

Formulaire standardisé à Boîte Sécurité

Svc Bureautique

□

Triage forensique

Image mémoire + logs + IOC

Boîte Sécurité

□

Déclaration ROCD

Sans délai si N2+ (via COMSI)

COMSI

□

PCA (si requis)

Évaluer et activer si services critiques impactés

CSIO + COMSI

□

PRP impliquées

Évaluer Loi 25 / CAI si exfiltration

CSIO + RPRP

□

Éradication

Nettoyage validé par Boîte Sécurité. Patch applé.

TI + Boîte Sécu.

□

Reprise

Test avant remise en service

Svc Bur. + COMSI

□

Rapport 14j (CVE)

Avancement remédiation au CGCD

COMSI

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

MAJ playbooks, gestion des correctifs (patch management), IOC

COMSI + CSIO

8. Principes fondamentaux

🚫 Principe 1 :  L’isolation réseau est la première action — avant de signaler, avant d’analyser. Elle limite la propagation et préserve les preuves.

🚫 Principe 2 :  Ne jamais éteindre un système suspect sans autorisation. La mémoire vive contient des preuves irremplçables.

🚫 Principe 3 :  La déclaration au ROCD (N2+) est non négociable. Le COMSI ne peut y substituer une escalade interne.

🚫 Principe 4 :  Ne jamais recommander le paiement d’une rançon. Cette décision appartient au CSIO en concertation avec le CGCD et le conseiller juridique.

Approbation

Fonction

Nom

Signature

Date

[Titre]

[Prénom Nom]

📎 Suite documentaire complète :  POL-SEC-001  |  DIR-SEC-001  |  PROC-SEC-002  |  PB-BUR-002  |  PB-SEC-002  |  PB-COMSI-002  |  PB-CSIO-002  |  PB-GEN-002
