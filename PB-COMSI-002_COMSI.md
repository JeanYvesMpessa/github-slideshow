---
title: "PB-COMSI-002 COMSI"
source: "PB-COMSI-002_COMSI.docx"
---

Codification

PB-COMSI-002

Entrée en vigueur

Mars 2026

Mise à jour

[Date]

PLAYBOOK

Logiciels malveillants et exploitation technique – Coordination et déclaration GMVI

COMSI

📋 Alignement cadre :  NIST CSF 2.0 / SP 800-61r3  │  ISO/IEC 27035:2023  │  CIS Controls v8 (Contrôle 17)

1. Mandat et spécificités de cette famille

Pour les incidents de logiciels malveillants et d’exploitation technique, le COMSI doit agir dans des fenêtres de temps très courtes. Il rend compte au CSIO et déclare au ROCD (N2+) de façon simultanée et parallèle. La déclaration au ROCD est une obligation GMVI externe non substituable dès le niveau 2.

📌 Positionnement GMVI :  Hiérarchie interne OP : Boîte Sécurité → COMSI → CSIO
Obligation GMVI externe : COMSI déclare au ROCD (N2+) → CGCD (N3+)
Rançongiciel (ransomware) = niveau 3 présumé | Déclaration ROCD et notification CSIO : simultanées, sans délai

2. Déclencheurs d’activation

Niveau GMVI

Situation

Mode d’activation

1

logiciel malveillant (malware) en quarantaine, système unique, non propagé

Notification Boîte Sécurité. COMSI informe le ROCD.

2

logiciel malveillant (malware) actif, propagation, exploitation CVE, DoS

Notification téléphonique immédiate au CSIO. COMSI déclare au ROCD sans délai (flux GMVI externe simultané).

3 présumé

Rançongiciel, exfiltration, multi-systèmes

COMSI déclare ROCD + CSIO. Formulaire MVI. Évaluer PCA.

🔴 Rançongiciel = niveau 3 présumé :  Tout incident impliqué un rançongiciel est classé niveau 3 par défaut jusqu’à évaluation contraire. La déclaration au ROCD est immédiate et obligatoire.

3. Prise en charge initiale — dans les 30 minutes

1

Valider la classification GMVI

Confirmer ou réviser. Rançongiciel = N3 par défaut. Propagation confirmée = N2 minimum.

2

Vérifier l’isolation en cours

Tous les systèmes affectés sont-ils isolés? Partages réseau coupés?

3

Déclarer au ROCD (N2+)

Téléphone, puis courriel. Format SAR. Formulaire MVI si N3.

4

Informer le CSIO

Briéfing SAR : Situation – État actuel – Recommandation.

5

Évaluer le PCA

Services critiques affectés? Activation du Plan de Continuité si oui.

4. Déclaration au ROCD — format SAR

1. SITUATION

Quel type de logiciel malveillant (malware) / exploitation? Quels systèmes? Depuis quand?

2. ÉTAT ACTUEL

Isolation effectuée? Périmètre confirmé? Propagation stoppée?

3. IMPACT

Services impactés? Données exfiltrées? Renseignements personnels impliqués?

4. INCONNUES

Vecteur d’entrée initial? Étendue réelle de la compromission?

5. RECOMMANDATION

Action requise du ROCD ou du CSIO?

5. Gestion de crise — Niveau 3+ et rançongiciel

Le COMSI active la cellule de crise et assume le rôle de coordonnateur opérationnel. Composition minimale pour un incident N3 de cette famille :

- CSIO (responsable global).

- COMSI (coordonnateur opérationnel).

- Responsable TI / Service Bureautique.

- Responsable réseau et infrastructure.

- Responsable de la protection des renseignements personnels (si exfiltration).

- Conseiller juridique (si volet criminel ou paiement de rançon envisagé).

- Direction générale (si PCA activé ou impact médias).

📋 Rançon — position du COMSI :  Le COMSI ne recommande PAS le paiement. Cette décision, si jamais envisagée, relève exclusivement du CSIO en concertation avec le CGCD et le conseiller juridique.

6. Gestion des vulnérabilités — obligations GMVI

Rapport 14 jours civils

Informer le CGCD de l’état d’avancement de la remédiation (CVE). Fréquence : 14 jours civils.

Conformité CVSS

Appliquer les correctifs dans les délais prescrits selon le score CVSS communiqué par le ROCD.

Fermeture d’actif

Si le CGCD exige la fermeture d’un actif à préjudice élevé : obtempérer. Décision CSIO requise.

Bulletins CGCD/COCD

S’assurer que les avis reçus sont diffusés aux équipes internes concernées.

7. Notification réglementaire

Législation

Déclencheur

Délai

Responsable

Loi 25 (Québec)

Exfiltration de renseignements personnels

Sans délai

CSIO + RPRP → CAI

LPRPDE (fédéral)

Risque réel de préjudice grave

Dès que possible

CSIO + Juridique

Volet criminel

Rançongiciel, sabotage informatique

Sur conseil juridique

COMSI + Forces de l’ordre

8. Indicateurs de performance (KPI)

Indicateur

Cible

Fréquence

Déclaration au ROCD (N2+)

&lt; 30 min

Par incident

Isolation effective des systèmes (N2+)

&lt; 1 heure

Par incident

MTTD – Mean Time to Detect

&lt; 2 heures

Par incident

MTTR – Mean Time to Respond

&lt; 4 heures (N2)

Par incident

Rapport remédiation CVE (14 jours)

100 %

Par vulnérabilité

9. Contacts prioritaires

Boîte Sécurité

securite@[organisation].ca  |  Poste : [XXXX]

ROCD (COCD)

[Prénom Nom]  |  Poste : [XXXX]  |  Cell : [XXX-XXX-XXXX]

CSIO

[Prénom Nom]  |  Cell 24/7 : [XXX-XXX-XXXX]

RPRP

[Prénom Nom]  |  Poste : [XXXX]

Responsable réseau

[Prénom Nom]  |  Poste : [XXXX]

Conseiller juridique

[Prénom Nom]  |  [XXX-XXX-XXXX]

Partenaire forensique externe

[Fournisseur]  |  [XXX-XXX-XXXX]

Approbation

Fonction

Nom

Signature

Date

[Titre]

[Prénom Nom]

📎 Documents connexes :  POL-SEC-001  |  DIR-SEC-001  |  PROC-SEC-002  |  PB-SEC-002  |  PB-CSIO-002
