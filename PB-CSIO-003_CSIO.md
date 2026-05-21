---
title: "PB-CSIO-003 CSIO"
source: "PB-CSIO-003_CSIO.docx"
---

Codification

PB-CSIO-003

Entrée en vigueur

Mars 2026

Mise à jour

[Date]

PLAYBOOK

Données, accès et appareils – Gouvernance, Loi 25 et décisions stratégiques

CSIO

📋 Alignement cadre :  NIST CSF 2.0 / SP 800-61r3  │  ISO/IEC 27035:2023  │  CIS Controls v8 (Contrôle 17)

1. Mandat stratégique — spécificités de cette famille

Pour cette famille, le CSIO assume deux responsabilités stratégiques simultanées : la gouvernance de la réponse à l’incident et la responsabilité de la déclaration à la CAI en vertu de la Loi 25. Ces deux volets ont des délais très courts et des conséquences légales en cas de non-conformité.

📌 Positionnement :  Autorité interne ultime  |  Décision CAI : CSIO + RPRP  |  Incident interne : CSIO + RH + Juridique  |  Communications : CSIO

2. Déclencheurs d’activation

Niveau GMVI

Critères

Délai notif.

Mode

N1

Incidents isolés sans PRP ni données sensibles

Rapport périodique

Courriel COMSI

N2

PRP impliquées, compte admin compromis, exfiltration

&lt; 30 min

Téléphone + courriel

N3

Exfiltration massive de PRP, destruction de données critiques

Immédiat

Téléphone direct 24/7

3. Décisions relevant exclusivement du CSIO

Déclaration à la CAI (Loi 25)

Si risque sérieux de préjudice. SANS DÉLAI dès confirmation. En concertation avec le RPRP.

Notification des personnes concernées

Si risque sérieux de préjudice (Loi 25). Avant les médias.

Déclaration LPRPDE (fédéral)

Si risque réel de préjudice grave.

Communication publique / médias

Toute communication externe exige l’approbation du CSIO.

Mesures disciplinaires / légales (incident interne)

En concertation avec RH et conseiller juridique.

Plainte aux autorités policières

Vol de données, espionnage, sabotage.

Activation PCA / PRA

Si destruction de données critiques compromet les opérations.

Recours à des experts forensiques externes

Incidents de grande envergure ou volet judiciaire.

4. Loi 25 — processus décisionnel du CSIO

📋 Référence légale :  Loi sur l’accès aux documents des organismes publics et sur la protection des renseignements personnels – Sections 63.7 à 63.11. CAI : 1-888-528-7741

1

Recevoir le rapport du RPRP

Nature des PRP atteintes. Volume. Catégories de personnes concernées.

2

Évaluer le risque de préjudice sérieux

Sensibilité des données, probabilité d’utilisation malveillante, conséquences potentielles.

3

Décider de la déclaration CAI

Si préjudice sérieux : déclarer SANS DÉLAI. Pas d’exception.

4

Notifier les personnes concernées

Si déclaration CAI requise : notifier les personnes avant les médias.

5

Communication externe

Approuver le message. Vérifier avec Juridique.

5. Gestion des incidents internes — cadre décisionnel

⚠️ Position stratégique :  Un incident impliquant un employé interne comporte trois dimensions simultanées : sécurité (preuves), légale (droit du travail) et réglementaire (Loi 25 si PRP). Le CSIO coordonne ces trois dimensions avec RH, Juridique et RPRP.

Preuves

Forensique complète avant toute action disciplinaire. Journaux, accès, exports.

Droit du travail

Consulter RH avant toute confrontation ou suspension. Risque de contestation.

Loi 25

Si PRP impliquées : obligation de déclaration CAI indépendamment du statut de l’employé.

Volet pénal

Si fraude ou vol confirmé : consulter Juridique pour dépôt de plainte.

6. Conformité GMVI — obligations de gouvernance

Déclaration ROCD validée

CSIO confirme que le COMSI a déclaré au ROCD (N2+).

Formulaire MVI (N3-N4)

CSIO s’assure de la production et de la transmission.

Bilan formel GMVI (30 j)

Co-présidé avec le COMSI. Transmis : COMSI, CSIO, ROCD, CDSI, CGSI.

Rapport firme externe

Remis au CERT/AQ dans les 2 semaines post-résolution.

Registre des événements (art. 16)

Disponible au CGCD sur demande.

Registre des atteintes (Loi 25)

Tenu par le RPRP. Consultable par la CAI.

7. Tableau de bord stratégique

Indicateur

Cible

Reporting

Incidents impliquant des PRP

Tendance à la baisse

Trimestriel

Conformité déclarations CAI (si requis)

100 %

Par incident

Taux de chiffrement des appareils

100 % appareils organisationnels

Mensuel (COMSI)

Taux d’application du moindre privilège

&gt; 98 %

Mensuel (COMSI)

Délai de revocation des accès (départ employé)

&lt; 24 h après départ

Mensuel (COMSI)

8. Contacts stratégiques

COMSI

[Prénom Nom]  |  Poste : [XXXX]  |  Cell : [XXX-XXX-XXXX]

RPRP

[Prénom Nom]  |  Poste : [XXXX]

Ressources humaines

[Prénom Nom]  |  Poste : [XXXX]

Conseiller juridique

[Cabinet]  |  [XXX-XXX-XXXX]

CAI (Loi 25)

1-888-528-7741

Commissaire fédéral (LPRPDE)

1-800-282-1376

ROCD (COCD)

[Prénom Nom]  |  Cell : [XXX-XXX-XXXX]

Approbation

Fonction

Nom

Signature

Date

[Titre]

[Prénom Nom]

📎 Documents connexes :  POL-SEC-001  |  DIR-SEC-001  |  PROC-SEC-003  |  PB-COMSI-003  |  PB-SEC-003  |  Loi 25 (art. 63.7 à 63.11)
