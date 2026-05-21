---
title: "PB-BUR-001 ServiceBureautique"
source: "PB-BUR-001_ServiceBureautique.docx"
---

Codification

PB-BUR-001

Entrée en vigueur

Mars 2026

Mise à jour

[Date]

PLAYBOOK

Incidents d’ingénierie sociale – Réception et qualification

Service Bureautique

📋 Alignement cadre :  NIST CSF 2.0 / SP 800-61r3  │  ISO/IEC 27035:2023  │  CIS Controls v8 (Contrôle 17)

1. Positionnement et mandat

Le Service Bureautique est le premier contact physique des utilisateurs lors d’un incident d’ingénierie sociale, quel que soit le vecteur (courriel, SMS, appel, code QR). Il reçoit, qualifie et achemine le signalement vers la Boîte Sécurité.

📌 Chaîne :  Utilisateur → Service Bureautique → Boîte Sécurité → COMSI → CSIO (hiérarchie interne OP) | COMSI → ROCD (obligation GMVI N2+)

2. Réception du signalement

2.1 Informations à collecter immédiatement — tout vecteur

✔

Signalement initial – tout incident d’ingénierie sociale

□

Nom, prénom et unité administrative de l’utilisateur

□

Vecteur de l’attaque : courriel / SMS / appel téléphonique / code QR / messagerie

□

Date et heure de réception

□

Date et heure de l’interaction, le cas échéant

□

Expéditeur apparent (adresse courriel, numéro de téléphone, domaine)

□

Objet ou contenu du message (résumé, sans retranscrire les liens)

□

Actions effectuées : clic / saisie / téléchargement / virement / accès accordé

□

Informations divulguées (type, pas la valeur des mots de passe)

□

Comportements anormaux observés depuis l’incident

□

Nom de machine (hostname) et adresse IP si applicable

2.2 Classification préliminaire GMVI

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

⚠️ Obligation GMVI :  Toute MVI de niveau 2 et plus doit être portée à la connaissance du CSIO (hiérarchie interne OP) ET déclarée au ROCD (obligation GMVI externe) sans délai par le COMSI, conformément à DIR-SEC-001. Ces deux obligations sont simultanées.

3. Transmission à la Boîte Sécurité

Transmettre à securite@[organisation].ca. Pour les courriels : joindre le message original en .eml ou .msg (ne pas copier-coller le texte seul).

📧 Objet standardisé :  [INCIDENT-IS] [N1/N2] – [Vecteur] – [Nom utilisateur] – [JJ-MM-AAAA]

Utilisateur

[Prénom Nom]  |  Unité : [XXX]

Vecteur

[Courriel / SMS / Appel / QR / Messagerie]

Date/heure réception

[JJ-MM-AAAA HH:MM]

Date/heure interaction

[JJ-MM-AAAA HH:MM] ou S/O

Expéditeur apparent

[adresse / numéro / domaine]

Actions effectuées

[détail précis]

Informations divulguées

[type uniquement]

Comportements anormaux

[Oui/Non – détail]

Niveau GMVI proposé

[1 / 2 / 3]

Pièce jointe

Message original (.eml/.msg) ou capture écran

4. Actions techniques par niveau

4.1 Niveau 1 — aucune interaction

✔

Actions N1 — message suspect sans interaction

□

Confirmer que l’utilisateur n’a effectué aucune action

□

Transmettre à la Boîte Sécurité avec le message original

□

Rassurer l’utilisateur — signaler est un acte responsable

4.2 Niveau 1-2 — clic ou interaction sans saisie

✔

Actions N1-2 — interaction sans divulgation d’information

□

Vérifier si l’antivirus a détecté une anomalie

□

Lancer une analyse antivirus rapide sur le poste

□

Vérifier les processus actifs inhabituels (Gestionnaire des tâches)

□

Documenter l’URL / numéro / domaine sans recontacter l’attaquant

□

Informer l’utilisateur de ne pas redémarrer le poste sans instruction

4.3 Niveau 2 — saisie d’informations, virement, ou accès accordé

✔

Actions N2 — URGENCE

□

Isoler physiquement le poste (débrancher RJ45 / désactiver Wi-Fi)

□

NE PAS éteindre le poste — préserve les traces mémoire

□

Apposer l’étiquette « EN ANALYSE – NE PAS UTILISER »

□

Notifier le COMSI immédiatement par téléphone

□

Documenter l’heure exacte d’isolation dans le ticket

□

Pour virement BEC : contacter d’urgence l’institution financière

□

Préparer le poste pour la prise en charge forensique

5. Support à l’utilisateur

1

Confirmer la prise en charge

Signalement reçu et transmis à l’équipe sécurité.

2

Rassurer

Signaler est un acte responsable. Aucune représaille pour un signalement de bonne foi.

3

Informer des étapes suivantes

Indiquer le délai de retour attendu. Proposer un poste de remplacement si le poste est isolé.

4

Confidentialité

Ne divulguer aucun détail de l’enquête sans autorisation de la Boîte Sécurité.

6. Contacts d’urgence

Boîte Sécurité

securite@[organisation].ca  |  Poste : [XXXX]

COMSI

[Prénom Nom]  |  Poste : [XXXX]  |  Cell : [XXX-XXX-XXXX]

CSIO (N3+)

[Prénom Nom]  |  Cell 24/7 : [XXX-XXX-XXXX]

Institution financière (BEC)

[Numéro urgence virement]

Approbation

Fonction

Nom

Signature

Date

[Titre]

[Prénom Nom]

📎 Documents connexes :  POL-SEC-001  |  DIR-SEC-001  |  PROC-SEC-001  |  PB-SEC-001  |  PB-COMSI-001
