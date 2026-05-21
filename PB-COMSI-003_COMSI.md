---
title: "PB-COMSI-003 COMSI"
source: "PB-COMSI-003_COMSI.docx"
---

Codification

PB-COMSI-003

Entrée en vigueur

Mars 2026

Mise à jour

[Date]

PLAYBOOK

Données, accès et appareils – Coordination et déclaration GMVI

COMSI

📋 Alignement cadre :  NIST CSF 2.0 / SP 800-61r3  │  ISO/IEC 27035:2023  │  CIS Controls v8 (Contrôle 17)

1. Mandat et spécificités de cette famille

Pour les incidents de la famille Données, accès et appareils, le COMSI doit gérer simultanément deux obligations critiques : la déclaration GMVI au ROCD et le déclenchement du processus Loi 25 lorsque des renseignements personnels sont impliqués. Ces deux obligations ont des délais distincts et des destinataires différents.

📌 Positionnement GMVI :  Hiérarchie interne OP : Boîte Sécurité → COMSI → CSIO
Obligation GMVI externe (N2+) : COMSI déclare au ROCD
Si PRP impliquées : RPRP → CSIO → CAI (Loi 25) (si PRP + préjudice sérieux)

2. Déclencheurs d’activation

Niveau GMVI

Situation

Mode d’activation

1

Appareil chiffré perdu, accès non autorisé minor, Wi-Fi non sécurisé

Notification Boîte Sécurité. COMSI informe le ROCD.

2

Exfiltration de données, compte admin compromis, PRP, intrusion active

Notification téléphonique immédiate au CSIO. COMSI déclare au ROCD sans délai (flux GMVI externe simultané).

3

Exfiltration massive de PRP, intrusion multi-OP, destruction de données critiques

COMSI déclare ROCD + CSIO. Formulaire MVI obligatoire.

🔴 Double obligation N2+ :  1° Informer le CSIO (hiérarchie interne OP) | 2° Déclarer au ROCD (GMVI, flux externe N2+) | 3° Si PRP impliquées : informer le CSIO + RPRP pour évaluation Loi 25 et déclaration CAI

3. Prise en charge initiale — dans les 30 minutes

1

Valider la classification GMVI et la présence de PRP

PRP impliquées? Si oui : déclencher le processus Loi 25 parallèlement.

2

Déclarer au ROCD (N2+)

Format SAR. Sans délai même si l’information est partielle.

3

Informer le CSIO et le RPRP (si PRP)

Briéfing SAR. RPRP évalue l’obligation de déclaration à la CAI.

4

Coordonner la réponse technique

Révocation des accès, effacement MDM, containment. En collaboration avec la Boîte Sécurité.

5

Si incident interne (employé suspecté)

Ne pas confronter l’employé sans coordination avec RH et juridique. Préserver les preuves en priorité.

4. Déclaration au ROCD — format SAR

1. SITUATION

Quel type d’incident? Quelles données? Quel compte? Quel système? Depuis quand?

2. ÉTAT ACTUEL

Accès révoqué? Appareil effacé? Intrusion stoppée? Forensique en cours?

3. IMPACT

Renseignements personnels impliqués? Volume de données? Systèmes touchés?

4. INCONNUES

Origine de la compromission? Données accessibles vs exfiltrées?

5. RECOMMANDATION

Décision ou action requise du ROCD ou du CSIO?

5. Gestion des incidents impliquant un employé interne

⚠️ Règle absolue :  Tout incident impliquant un employé interne suspecté (fuite malveillante, abus de privilèges) doit être coordonné avec les Ressources humaines et le conseiller juridique avant toute confrontation ou mesure disciplinaire. Une action prématurée peut compromettre les preuves et exposer l’organisation à des risques légaux.

Protocole pour les incidents internes :

- Contacter les Ressources humaines immédiatement après la qualification.

- Contacter le conseiller juridique pour évaluer les options légales.

- Préserver les preuves (journaux, accès) AVANT toute action disciplinaire.

- Si risque de destruction de preuves imminente : révoquer les accès immédiatement, puis informer RH.

- Ne pas informer l’employé suspect avant d’avoir consulté RH et Juridique.

6. Obligations Loi 25 — tableau de référence

Obligation

Déclencheur

Délai

Responsable

Informer le RPRP

Dès qu’une atteinte impliquant des PRP est identifiée

Sans délai

CSIO via COMSI

Déclaration à la CAI

Si risque sérieux de préjudice (Loi 25, art. 63.8)

Sans délai dès confirmation

CSIO + RPRP

Notification personnes concernées

Si risque sérieux de préjudice

Sans délai

CSIO + RPRP

Registre des atteintes

Toute atteinte, même sans préjudice sérieux

Dès l’incident

RPRP

7. Notification réglementaire — tableau de référence

Législation

Déclencheur

Délai

Responsable

Loi 25 (Québec)

Atteinte aux renseignements personnels

Sans délai

CSIO + RPRP → CAI

LPRPDE (fédéral)

Risque réel de préjudice grave

Dès que possible

CSIO + Juridique

Volet criminel

Abus de privilèges, vol de données, espionnage industriel

Sur conseil juridique

COMSI + Forces de l’ordre

8. Indicateurs de performance (KPI)

Indicateur

Cible

Fréquence

Déclaration ROCD (N2+)

&lt; 30 min

Par incident

Qualification PRP (présente ou non)

&lt; 2 h après signalement

Par incident

Délai d’alerte RPRP (si PRP)

Sans délai dès qualification

Par incident

Délai de déclaration CAI (si requis)

Sans délai dès confirmation préjudice

Par incident

Taux de conformité des accès privilégiés

&gt; 98 % (moindre privilège)

Mensuel

9. Contacts prioritaires

Boîte Sécurité

securite@[organisation].ca  |  Poste : [XXXX]

ROCD (COCD)

[Prénom Nom]  |  Cell : [XXX-XXX-XXXX]

CSIO

[Prénom Nom]  |  Cell 24/7 : [XXX-XXX-XXXX]

RPRP

[Prénom Nom]  |  Poste : [XXXX]

Ressources humaines

[Prénom Nom]  |  Poste : [XXXX]

Conseiller juridique

[Prénom Nom]  |  [XXX-XXX-XXXX]

CAI (Loi 25)

1-888-528-7741

Approbation

Fonction

Nom

Signature

Date

[Titre]

[Prénom Nom]

📎 Documents connexes :  POL-SEC-001  |  DIR-SEC-001  |  PROC-SEC-003  |  PB-SEC-003  |  PB-CSIO-003  |  Loi 25
