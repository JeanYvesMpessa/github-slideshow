---
title: "PB-CSIO-002 CSIO"
source: "PB-CSIO-002_CSIO.docx"
---

Codification

PB-CSIO-002

Entrée en vigueur

Mars 2026

Mise à jour

[Date]

PLAYBOOK

Logiciels malveillants et exploitation technique – Gouvernance et décisions stratégiques

CSIO

📋 Alignement cadre :  NIST CSF 2.0 / SP 800-61r3  │  ISO/IEC 27035:2023  │  CIS Controls v8 (Contrôle 17)

1. Mandat stratégique — spécificités de cette famille

Les incidents de cette famille présentent le risque d’impact opérationnel le plus élevé. Le rançongiciel peut paralyser complètement l’organisation en quelques heures. Le CSIO doit être prêt à prendre des décisions stratégiques irréversibles rapidement.

📌 Positionnement :  Autorité interne ultime  |  Décision rançon : CSIO + CGCD  |  PCA/PRA : CSIO  |  Communications : CSIO  |  Notification Loi 25 : CSIO

2. Déclencheurs d’activation

Niveau GMVI

Critères

Délai notif.

Mode

N1

logiciel malveillant (malware) en quarantaine, système unique

Rapport périodique

Courriel COMSI

N2

Propagation, exploitation CVE, service dégradé

&lt; 30 min

Téléphone + courriel

N3

Rançongiciel, exfiltration, multi-systèmes

Immédiat

Téléphone direct 24/7

3. Prise en charge initiale — N3 (&lt; 30 min)

1

Recevoir le briéfing SAR du COMSI

Confirmer la classification. Valider l’isolation élargie en cours.

2

Décisions stratégiques immédiates

Voir section 4 pour la liste complète.

3

Activer la cellule de crise

Assigner les rôles. Évaluer les ressources externes (forensique spécialisée).

4. Décisions relevant exclusivement du CSIO

Activation du PCA / PRA

Si la disponibilité des services critiques est compromise. Décision irréversible à prendre rapidement.

Arrêt de systèmes additionnels

Si la propagation du rançongiciel (ransomware) ou du logiciel malveillant (malware) menace des systèmes non encore isolés.

Question du paiement de rançon

Décision prise en concertation avec le CGCD et le conseiller juridique. Ne jamais déléguer.

Notification Loi 25 / CAI

Exfiltration de renseignements personnels confirmée.

Communication publique / médias

Toute communication externe exige l’approbation du CSIO.

Recours à des experts forensiques externes

Capacités internes insuffisantes pour N3+.

Plainte aux autorités policières

Rançongiciel, sabotage informatique, espionnage.

Fermeture d’actif (CGCD)

Si le CGCD l’exige : obtempérer. Documenter la décision.

5. Position sur le paiement de rançon

🚫 Position institutionnelle :  Le paiement d’une rançon ne garantit pas la récupération des données, finance les attaquants et peut violer des règlements. Avant toute décision, consulter le CGCD, le conseiller juridique et évaluer si des sauvegardes saines sont disponibles.

Si le paiement est envisagé — liste de vérification minimale :

- Sauvegardes évaluées et confirmées non disponibles ou corrompues.

- Consultation du CGCD et du CERT/AQ obtenue.

- Avis juridique reçu sur la légalité du paiement.

- Risque pour la vie humaine ou services essentiels évalué.

- Approbation de la direction générale et du conseil d’administration.

6. Conformité GMVI — obligations de gouvernance

Déclaration ROCD validée

CSIO confirme que le COMSI a déclaré au ROCD (N2+).

Formulaire MVI (N3-N4)

CSIO s’assure de la production et de la transmission.

Rapport remédiation CVE

CSIO valide les rapports d’avancement de 14 jours au CGCD.

Bilan formel GMVI (30 j)

Co-présidé avec le COMSI. Transmis : COMSI, CSIO, ROCD, CDSI, CGSI.

Rapport firme externe

Remis au CERT/AQ dans les 2 semaines post-résolution.

Registre des événements (art. 16)

Maintenu et disponible au CGCD sur demande.

7. Tableau de bord stratégique

Indicateur

Cible

Reporting

Incidents par famille (logiciel malveillant (malware)/exploitation)

Tendance à la baisse

Trimestriel

Taux de couverture des correctifs (patch management)

&gt; 95 % sous 30 jours

Mensuel (COMSI)

Délai de déclaration ROCD (N2+)

100 % &lt; 30 min

Par incident

Taux de conformité remédiation CVE (14 jours)

100 %

Par vulnérabilité

Temps de reprise (PCA) testé

&lt; RTO défini

Annuel (exercice)

8. Contacts stratégiques

COMSI

[Prénom Nom]  |  Poste : [XXXX]  |  Cell : [XXX-XXX-XXXX]

ROCD (COCD)

[Prénom Nom]  |  Cell : [XXX-XXX-XXXX]

Direction générale

[Prénom Nom]  |  Poste : [XXXX]

Conseiller juridique

[Cabinet]  |  [XXX-XXX-XXXX]

CAI (Loi 25)

1-888-528-7741

Partenaire forensique externe

[Fournisseur]  |  [XXX-XXX-XXXX]

Centre canadien cybersécurité

1-833-CYBER-88

Approbation

Fonction

Nom

Signature

Date

[Titre]

[Prénom Nom]

📎 Documents connexes :  POL-SEC-001  |  DIR-SEC-001  |  PROC-SEC-002  |  PB-COMSI-002  |  PB-SEC-002
