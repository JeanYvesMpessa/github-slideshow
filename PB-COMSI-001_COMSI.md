---
title: "PB-COMSI-001 COMSI"
source: "PB-COMSI-001_COMSI.docx"
---

Codification

PB-COMSI-001

Entrée en vigueur

Mars 2026

Mise à jour

[Date]

PLAYBOOK

Incidents d’ingénierie sociale – Coordination et déclaration GMVI

COMSI

📋 Alignement cadre :  NIST CSF 2.0 / SP 800-61r3  │  ISO/IEC 27035:2023  │  CIS Controls v8 (Contrôle 17)

1. Mandat et autorité

Le COMSI est le principal point de contact de l’organisme public (OP) pour toutes les MVI. Il coordonne la réponse interne, rend compte au CSIO pour toutes les MVI. Il déclare au ROCD dès le niveau 2 (obligation GMVI externe), et constitue le pivot entre les équipes opérationnelles de l'OP et la chaîne gouvernementale.

📌 Positionnement GMVI :  Hiérarchie interne OP : Boîte Sécurité → COMSI → CSIO
Obligation GMVI externe : COMSI déclare au ROCD (N2+) → CGCD (N3+)
Autorité décisionnelle interne : N1-N3 | Escalade au CSIO : N2+ (information) / N3+ (décision)

2. Déclencheurs d’activation par niveau GMVI

Niveau GMVI

Situation

Mode d’activation du COMSI

1

MVI gérée entièrement à l’interne

Notification de la Boîte Sécurité. COMSI informe le ROCD.

2

Divulgation d’infos, virement, accès accordé, plusieurs employés

Notification tél. immédiate. COMSI déclare au ROCD sans délai.

3

Impact multi-OP, données gouvernementales, propagation

COMSI déclare ROCD + informe CSIO. Formulaire MVI obligatoire.

🔴 Obligation absolue :  Toute MVI de niveau 2 et plus doit être déclarée au ROCD sans délai, même si l’information est partielle ou préliminaire. La déclaration ne peut être remplacée par une escalade interne uniquement.

3. Prise en charge initiale — dans les 30 minutes

1

Valider la classification GMVI

Confirmer ou réviser à la hausse. En cas de doute, niveau supérieur.

2

Vérifier le confinement en cours

Isolation poste confirmée? Réinitialisation des accès en cours?

3

Déclarer au ROCD (N2+)

Par téléphone, puis courriel. Transmettre le formulaire MVI si N3.

4

Informer le CSIO

Brièfing SAR : Situation – État actuel – Recommandation.

5

Ouvrir la session de coordination

Appel ou salle dédiée. Affecter les tâches. Éviter les doublons d’effort.

4. Déclaration au ROCD — format SAR

1. SITUATION

Que s’est-il passé? Quel vecteur? Qui est touché? Quand?

2. ÉTAT ACTUEL

Quelles actions ont été prises? Quels systèmes sont isolés? Accès réinitialisés?

3. IMPACT POTENTIEL

Quelles données ou systèmes pourraient être affectés? Renseignements personnels impliqués?

4. INCONNUES

Qu’est-ce qui n’est pas encore confirmé?

5. RECOMMANDATION

Quelle décision ou action est requise du ROCD ou du CSIO?

5. Gestion de crise — Niveau 3+ (cellule de crise)

Si le ROCD ou le CGCD classe la MVI au niveau 3 ou plus, le COMSI active la cellule de crise et assume le rôle de coordonnateur opérationnel.

- CSIO (responsable global).

- COMSI (coordonnateur opérationnel).

- Responsable TI / Service Bureautique.

- Responsable des communications (si disponible).

- Responsable de la protection des renseignements personnels (si PRP impliquées).

- Conseiller juridique (si volet criminel ou Loi 25).

📋 Formulaire MVI obligatoire — N3-N4 :  Le formulaire MVI officiel du GMVI doit être transmis conformément à l’Annexe 2 du processus GMVI (MCN/CGCD).

6. Notification réglementaire

Législation

Déclencheur

Délai

Responsable

Loi 25 (Québec)

Atteinte aux renseignements personnels — risque sérieux de préjudice

Sans délai

CSIO + RPRP → CAI

LPRPDE (fédéral)

Risque réel de préjudice grave

Dès que possible

CSIO + Juridique

BEC / fraude

Virement frauduleux confirmé

Immédiat

COMSI + Institution financière

Volet criminel

Usurpation d’identité, fraude électronique

Sur conseil juridique

COMSI + Forces de l’ordre

7. Indicateurs de performance (KPI)

Indicateur

Cible

Fréquence

Délai de déclaration au ROCD (N2+)

Sans délai (&lt; 30 min)

Par incident

MTTD – Mean Time to Detect

&lt; 2 heures

Par incident

MTTR – Mean Time to Respond

&lt; 4 heures (N2)

Par incident

Taux de signalement

100 % des incidents N1+

Mensuel

Conformité délais d’escalade

&gt; 95 %

Mensuel

8. Contacts prioritaires

Boîte Sécurité

securite@[organisation].ca  |  Poste : [XXXX]

ROCD (COCD)

[Prénom Nom]  |  Poste : [XXXX]  |  Cell : [XXX-XXX-XXXX]

CSIO

[Prénom Nom]  |  Poste : [XXXX]  |  Cell : [XXX-XXX-XXXX]

RPRP

[Prénom Nom]  |  Poste : [XXXX]

Conseiller juridique

[Prénom Nom]  |  [XXX-XXX-XXXX]

Institution financière (urgences)

[Numéro urgence]

Forces de l’ordre (si criminel)

911 ou ligne dédiée

Approbation

Fonction

Nom

Signature

Date

[Titre]

[Prénom Nom]

📎 Documents connexes :  POL-SEC-001  |  DIR-SEC-001  |  PROC-SEC-001  |  PB-SEC-001  |  PB-CSIO-001
