---
title: "PB-SEC-001 BoiteSecurite"
source: "PB-SEC-001_BoiteSecurite.docx"
---

Codification

PB-SEC-001

Entrée en vigueur

Mars 2026

Mise à jour

[Date]

PLAYBOOK

Incidents d’ingénierie sociale – Triage, analyse et coordination

Boîte Sécurité de l’Information

📋 Alignement cadre :  NIST CSF 2.0 / SP 800-61r3  │  ISO/IEC 27035:2023  │  CIS Controls v8 (Contrôle 17)

1. Positionnement et mandat

La Boîte Sécurité est le coeur opérationnel de la réponse. Elle reçoit tous les signalements d’ingénierie sociale, effectue le triage, coordonne l’analyse et notifie les parties prenantes internes et gouvernementales.

📌 Chaîne :  Svc Bureautique / Utilisateurs → Boîte Sécurité → COMSI → CSIO (hiérarchie interne OP) | COMSI → ROCD (obligation GMVI N2+)

⏰ Délai de prise en charge :  Tout signalement doit être accusé de réception ET classifié dans un délai maximal de 1 h (jours ouvrables) et 2 h (hors heures pour N2+).

2. Analyse initiale du signalement

Pour chaque signalement, effectuer l’analyse structurée suivante dans l’heure suivant la réception.

Étape

Vérification

Outil / Méthode

1

Confirmer le vecteur d’attaque

Courriel, SMS, appel, QR, messagerie — déterminer la nature exacte

2

Vérifier l’en-tête du message (courriel)

Headers SMTP : Received, Return-Path, DKIM, SPF, DMARC

3

Analyser les URLs / liens / domaines

VirusTotal, URLScan.io, WHOIS, Google Safe Browsing (sans cliquer)

4

Analyser les pièces jointes

VirusTotal (hash SHA-256), environnement isolé (sandbox) — Hybrid Analysis

5

Corréler avec incidents connus et veille

IOC antérieurs, bulletins CGCD/COCD, journaux de la semaine

6

Classifier selon niveaux GMVI

Grille DIR-SEC-001 — en cas de doute, niveau supérieur

3. Procédures de réponse par niveau GMVI

Niveau 1 – OP interne, aucune interaction ou interaction sans divulgation

1

Ouvrir le dossier MVI et consigner

Statut : Surveillé. Numéro INC-AAAA-XXXX. Conserver les preuves en évidence.

2

Extraire les IOC

Adresses IP, URLs, domaines, hash SHA-256. Mettre à jour les filtres de messagerie.

3

Vérifier la propagation

Autres employés ont-ils reçu le même message? Recherche dans les journaux.

4

Informer le COMSI

Via rapport périodique. COMSI informe le ROCD (GMVI N1).

Niveau 2 – Interaction avec divulgation d’information ou virement

🚨 Urgence :  Délai de réponse : moins d’une heure. Notifier le COMSI immédiatement par téléphone.

1

Isolation immédiate du poste

Confirmer avec le Service Bureautique. Ne pas éteindre l’appareil.

2

Réinitialisation forcée des accès compromis

En coordination avec TI. Documenter l’heure exacte de réinitialisation.

3

Analyse forensique

Image mémoire, logs, artefacts. Vérifier la propagation latérale sur le réseau.

4

Notifier le COMSI

Téléphone + courriel dans les 30 minutes. COMSI déclare au ROCD (GMVI N2).

5

BEC seulement : déclencher le rappel du virement

Contacter d’urgence l’institution financière. Fenêtre de rappel très courte.

Niveau 2-3 – Propagation, données sensibles, impact multi-employés

🔴 CRITIQUE :  Escalade immédiate au COMSI et au CSIO. COMSI déclare au ROCD. Évaluer Loi 25.

1

Isolation élargie

Isoler tous les systèmes potentiellement affectés. Établir le périmètre avec le COMSI.

2

Préserver les preuves

Chaîne de custody conforme ISO/IEC 27037. Logs, images forensiques, captures.

3

Évaluer l’obligation Loi 25

Données personnelles impliquées? Alerter le CSIO et le RPRP. Délai de déclaration CAI.

4. Collecte de preuves – Chaîne de custody

Type de preuve

Méthode de collecte

Conservation

Message original

.eml ou .msg avec métadonnées SMTP complètes

Chiffré, accès restreint, min. 1 an

Capture d’écran / photo QR

Horodatée

Archivée avec le dossier MVI

Journaux système

Export CSV/TXT signé avec hash SHA-256

Min. 2 ans

Image forensique poste

Outil certifié (FTK, Autopsy, dd)

Chaîne de custody documentée

Enregistrement d’appel (si disponible)

Export système téléphonie

Archivé avec le dossier MVI

Journaux réseau / proxy

Export brut + filtres appliqués

Corrélé au dossier MVI

5. Notifications internes et gouvernementales

Destinataire

Niveau GMVI

Délai

Canal

Service Bureautique

1 et +

&lt; 30 min

Courriel

COMSI

1 et +

&lt; 1 h / &lt; 30 min (N2)

Courriel + tél. (N2+)

CSIO

2 et +

&lt; 1 h

Via COMSI

ROCD (COCD)

2 et + — via COMSI

Sans délai

COMSI déclare au ROCD

RPRP (si PRP impliquées)

Tout niveau

&lt; 2 h

Courriel + appel

6. Rapport de clôture

Dans les 5 jours ouvrables suivant la résolution (N1-N2). Dans les 30 jours pour les niveaux 3-4 (bilan formel GMVI). Le rapport comprend :

- Résumé exécutif à destination du COMSI et du CSIO.

- Chronologie détaillée des événements et du vecteur d’attaque.

- IOC identifiés (domaines, IPs, hashes, numéros de téléphone).

- Actions de confinement, réinitialisation et éradication.

- Analyse de la cause profonde.

- Leçons apprises et recommandations.

Approbation

Fonction

Nom

Signature

Date

[Titre]

[Prénom Nom]

📎 Documents connexes :  POL-SEC-001  |  DIR-SEC-001  |  PROC-SEC-001  |  PB-BUR-001  |  PB-COMSI-001
