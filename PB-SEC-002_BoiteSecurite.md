---
title: "PB-SEC-002 BoiteSecurite"
source: "PB-SEC-002_BoiteSecurite.docx"
---

Codification

PB-SEC-002

Entrée en vigueur

Mars 2026

Mise à jour

[Date]

PLAYBOOK

Logiciels malveillants et exploitation technique – Triage, analyse et coordination

Boîte Sécurité de l’Information

📋 Alignement cadre :  NIST CSF 2.0 / SP 800-61r3  │  ISO/IEC 27035:2023  │  CIS Controls v8 (Contrôle 17)

1. Positionnement et mandat

Pour cette famille, la Boîte Sécurité dirige l’analyse forensique, coordonne le confinement multi-systèmes et constitue le centre névralgique des décisions techniques. La rapidité et la rigueur de l’analyse dans les premières heures déterminent la portée réelle de l’incident.

⏰ Délai critique :  Pour les malwares actifs et le rançongiciel, le triage doit être complété dans les 30 minutes suivant le signalement. Chaque minute de propagation peut multiplier l’impact.

2. Analyse initiale du signalement

Étape

Vérification

Outil / Méthode

1

Confirmer le type de menace et le vecteur

Rapport antivirus / EDR / SIEM, description utilisateur

2

Vérifier l’étendue de la propagation

Journaux réseau, EDR centré, connexions actives

3

Analyser les IOC initiaux

Hash SHA-256 (VirusTotal), IPs (AbuseIPDB), domaines (WHOIS)

4

Corréler avec bulletins CGCD/COCD

Alertes reçues, CVE publiées, campagnes connues

5

Classifier selon niveaux GMVI

Grille DIR-SEC-001 — en cas de doute, niveau supérieur

6

Confirmer l’isolation des systèmes affectés

Vérification physique + logs réseau

3. Procédures de réponse par niveau GMVI

Niveau 1 – logiciel malveillant (malware) en quarantaine, système unique

1

Ouvrir le dossier MVI

Numéro INC-AAAA-XXXX. Statut : En analyse. Conserver la quarantaine.

2

Extraire et analyser les IOC

Hash SHA-256 du logiciel malveillant (malware), chemin de fichier, horodatage, clés de registre modifiées.

3

Vérifier la propagation

Autres systèmes avec le même hash ou comportement? Journaux réseau.

4

Valider la suppression

Confirmer l’éradication complète. Autoriser le redémarrage si tout est propre.

Niveau 2 – logiciel malveillant (malware) actif, propagation, exploitation

🚨 Urgence :  Triage en 30 minutes. Notifier le COMSI par téléphone immédiatement.

1

Confirmer et étendre l’isolation

Valider l’isolation avec le Svc Bureautique. Identifier tous les systèmes potentiellement touchés.

2

Image mémoire et forensique

Procéder à l’image de la mémoire vive avant toute autre action sur le système. Utiliser un outil certifié (FTK, Volatility).

3

Analyse des journaux

Auth logs, syslog, journaux d’application, logs proxy/pare-feu. Identifier le vecteur d’entrée initial.

4

Notifier COMSI

Téléphone + courriel. COMSI déclare au ROCD (GMVI N2). Préparer le briéfing SAR.

Niveau 3 présumé – Rançongiciel / Exfiltration / Multi-systèmes

🔴 CRITIQUE — Escalade immédiate :  Notifier COMSI + CSIO. COMSI déclare ROCD d’urgence. Formulaire MVI obligatoire. Évaluer Loi 25.

1

Isolation élargie — périmètre complet

Identifier et isoler TOUS les systèmes du périmètre de propagation. Journaliser chaque action.

2

Préserver les preuves — chaîne de custody

Image forensique des systèmes clés. Logs horodatés. Conserver les versions chiffrées (ransomware).

3

Identifier le vecteur d’entrée initial

Retrace des événements : comment l’attaquant est-il entré? Quelle CVE? Quel compte?

4

Évaluation Loi 25 et LPRPDE

Données personnelles exfiltrées ou accessibles? Alerter immédiatement le CSIO et le RPRP.

5

Rapport de situation toutes les heures

Statut, périmètre, actions en cours, prochaine étape.

4. Procédures spécifiques par vecteur

Vecteur

Procédure spécifique complémentaire

Rançongiciel

Identifier la famille (ID rançongiciel (ransomware) tool). Vérifier si déchiffrement gratuit disponible (NoMoreRansom.org). NE PAS recommander le paiement — décision CSIO + CGCD.

logiciel sans fichier (fileless malware)

Image mémoire prioritaire avant isolation (sinon preuves perdues). Analyse avec Volatility.

Logiciel furtif (rootkit)

Outils forensiques avancés requis (GMER, Logiciel furtif (rootkit) Revealer). Le système OS ne peut être considéré fiable pour l’analyse.

CVE exploitée

Identifier le CVE ID. Rapporter au ROCD + informer le CGCD. Délai remédiation 14 jours civils.

Injection SQL

Analyser les logs applicatifs et la base de données. Identifier les tables accédées ou exfiltrées.

DoS / DDoS

Coordonner avec le fournisseur d’accès internet et l’équipe réseau. Activer le filtre anti-DDoS si disponible.

5. Collecte de preuves — Chaîne de custody (ISO/IEC 27037)

Type de preuve

Méthode de collecte

Conservation

Image mémoire vive

Volatility, WinPmem, LiME — AVANT toute autre action

Chaîne de custody. Min. 2 ans.

Image disque forensique

FTK Imager, dd, Autopsy. Hash MD5+SHA256.

Chaîne de custody documentée.

Journaux système

Export horodaté signé. Windows Event Logs, syslog.

Min. 2 ans.

Journaux réseau/proxy

Export brut + filtres. NetFlow, pare-feu.

Corrélé au dossier MVI.

Rapport antivirus/EDR

Export complet avec hashes et chemins.

Archivé avec le dossier.

Fichiers en quarantaine

Ne pas supprimer. Conserver avec hash.

Accès restreint. Min. 1 an.

Captures réseau (PCAP)

Wireshark si disponible. Avant isolation si réalisable.

Archivé avec le dossier.

6. Notifications internes et gouvernementales

Destinataire

Niveau GMVI

Délai

Canal

Service Bureautique

1 et +

&lt; 30 min

Courriel + tél.

COMSI

1 et +

&lt; 30 min (N2+ : immédiat)

Tél. + courriel

CSIO

2 et +

&lt; 30 min

Via COMSI

ROCD (COCD) — via COMSI

2 et +

Sans délai

COMSI déclare

RPRP (si PRP impliquées)

Tout niveau

&lt; 1 h

Courriel + appel

CERT/AQ — via ROCD

2 et +

Via ROCD

Écosystème GMVI

7. Rapport de clôture

Dans les 5 jours ouvrables (N1-N2). Dans les 30 jours pour les niveaux 3-4 (bilan formel GMVI). Inclure :

- Résumé exécutif avec niveau GMVI, vecteur d’attaque, impact confirmé.

- Chronologie de l’incident depuis le vecteur d’entrée jusqu’à la clôture.

- IOC complets (hashes, IPs, domaines, chemins de fichiers, CVE ID).

- Propagation : nombre de systèmes touchés, vecteur de mouvement latéral.

- Analyse root cause : vulnérabilité exploitée, contrôle défaillant.

- Actions de confinement, éradication et reprise.

- Leçons apprises et recommandations (patch, segmentation, contrôles).

Approbation

Fonction

Nom

Signature

Date

[Titre]

[Prénom Nom]

📎 Documents connexes :  POL-SEC-001  |  DIR-SEC-001  |  PROC-SEC-002  |  PB-BUR-002  |  PB-COMSI-002
