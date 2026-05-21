---
title: "PB-BUR-002 ServiceBureautique"
source: "PB-BUR-002_ServiceBureautique.docx"
---

Codification

PB-BUR-002

Entrée en vigueur

Mars 2026

Mise à jour

[Date]

PLAYBOOK

Logiciels malveillants et exploitation technique – Réception et actions techniques

Service Bureautique

📋 Alignement cadre :  NIST CSF 2.0 / SP 800-61r3  │  ISO/IEC 27035:2023  │  CIS Controls v8 (Contrôle 17)

1. Positionnement et mandat

Pour cette famille, le Service Bureautique joue un rôle technique immédiat plus important qu’en ingénierie sociale : il est souvent le premier à intervenir physiquement sur le système affecté. Son action dans les premières minutes détermine la capacité d’analyse forensique et limite la propagation.

📌 Chaîne :  Utilisateur / Outil auto → Svc Bureautique → Boîte Sécurité → COMSI → CSIO (hiérarchie interne OP) | COMSI → ROCD (obligation GMVI N2+)

🚨 Règle absolue N° 1 :  Ne JAMAIS éteindre un système suspect avant autorisation de la Boîte Sécurité. Exception : rançongiciel qui chiffre activement ET impossible d’isoler autrement.

2. Réception du signalement

2.1 Informations à collecter immédiatement

✔

Signalement initial – logiciel malveillant (malware) ou exploitation technique

□

Nom, prénom et unité administrative de l’utilisateur ou source de l’alerte

□

Nature du comportement détecté (symptôme, message d’alerte, outil ayant signalé)

□

Date et heure de détection ou du premier comportement anormal

□

Nom de machine, adresse IP, systèmes potentiellement affectés

□

Actions déjà effectuées avant le signalement (redémarrage, scan, suppression)

□

Données ou services potentiellement impactés

□

Alertes générées par les outils (antivirus, EDR, SIEM)

2.2 Classification préliminaire GMVI

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

⚠️ Obligation GMVI :  Toute MVI de niveau 2 et plus doit être déclarée au ROCD sans délai par le COMSI. Le rançongiciel en propagation est présumé niveau 3 jusqu’à preuve du contraire.

3. Actions techniques par niveau

3.1 Tout niveau — isolation réseau en priorité

✔

Isolation immédiate — toujours en premier

□

Débrancher le câble RJ45 ET désactiver le Wi-Fi simultanément

□

Pour les serveurs : couper le port de commutation sur instruction de la Boîte Sécurité

□

Documenter l’heure exacte d’isolation dans le ticket

□

Apposer l’étiquette « EN ANALYSE – NE PAS UTILISER »

3.2 Niveau 1 — logiciel malveillant (malware) en quarantaine, système unique

✔

Actions N1 — après isolation

□

Confirmer que l’antivirus a placé la menace en quarantaine

□

Consigner le rapport d’alerte complet (nom du logiciel malveillant (malware), hash, chemin de fichier)

□

Transmettre à la Boîte Sécurité sans supprimer la quarantaine

□

Ne pas redémarrer sans instruction

3.3 Niveau 2 — logiciel malveillant (malware) actif, propagation ou exploitation

✔

Actions N2 — URGENCE

□

Isolation réseau immédiate (voir 3.1)

□

NE PAS éteindre le système — préserve mémoire vive et artefacts

□

NE PAS appliquer de correctif (patch) ou lancer de scan sans instruction de la Boîte Sécurité

□

Notifier le COMSI par téléphone immédiatement

□

Préparer le système pour image forensique (ne rien modifier)

□

Pour DoS/DDoS : contacter l’équipe réseau pour mise en oeuvre des mesures de mitigation

3.4 Niveau 3 présumé — rançongiciel en propagation ou exfiltration

✔

Actions N3 — CRITIQUE

□

Isolation réseau de TOUS les systèmes potentiellement affectés

□

Couper les partages réseau (SMB, NFS) si techniquement possible et sur instruction

□

NE PAS éteindre sauf dernier recours absolument justifié

□

Notifier le COMSI ET le CSIO immédiatement par téléphone

□

Évaluer l’activation du PCA avec le COMSI

□

Documenter le périmètre exact des systèmes isolés

4. Signaux d’alerte spécifiques à surveiller

Vecteur

Signal d’alerte critique

Rançongiciel

Extensions de fichiers modifiées, fichiers README_DECRYPT, impossibilité d’ouvrir des documents

logiciel sans fichier (fileless malware)

PowerShell ou WMI en exécution anormale, processus légitimes avec trafic réseau inhabituel

cryptominage non autorisé (cryptojacking)

CPU à 100 % en permanence, surchauffe, lenteur système généralisée

Logiciel furtif (rootkit)

Outils de sécurité dysfonctionnels, comportements inexplicables, système instable

DoS / DDoS

Service complètement inaccessible, trafic entrant massif, alertes pare-feu

Injection SQL

Erreurs SQL dans logs, requêtes contenant OR 1=1, accès à des tables non autorisées

5. Transmission à la Boîte Sécurité

📧 Objet standardisé :  [INCIDENT-TECH] [N1/N2/N3] – [Type menace] – [Système] – [JJ-MM-AAAA]

Système(s) affecté(s)

[hostname(s) / IP(s)]

Nature de la menace

[rançongiciel (ransomware) / logiciel malveillant (malware) / CVE / DoS / injection / ...]

Heure détection

[JJ-MM-AAAA HH:MM]

Heure isolation

[JJ-MM-AAAA HH:MM]

Outil ayant détecté

[Antivirus / EDR / SIEM / Utilisateur / ...]

Alertes générées

[Nom logiciel malveillant (malware), hash, CVE ID si connu]

Actions effectuées

[Isolation, quarantaine, etc.]

Propagation observée

[Oui/Non – nombre de systèmes affectés]

Niveau GMVI proposé

[1 / 2 / 3]

6. Contacts d’urgence

Boîte Sécurité

securite@[organisation].ca  |  Poste : [XXXX]

COMSI

[Prénom Nom]  |  Poste : [XXXX]  |  Cell : [XXX-XXX-XXXX]

CSIO (N3+)

[Prénom Nom]  |  Cell 24/7 : [XXX-XXX-XXXX]

Équipe réseau (DoS/DDoS)

[Prénom Nom]  |  Poste : [XXXX]

Approbation

Fonction

Nom

Signature

Date

[Titre]

[Prénom Nom]

📎 Documents connexes :  POL-SEC-001  |  DIR-SEC-001  |  PROC-SEC-002  |  PB-SEC-002  |  PB-COMSI-002
