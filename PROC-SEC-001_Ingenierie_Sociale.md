---
title: "PROC-SEC-001 Ingenierie Sociale"
source: "PROC-SEC-001_Ingenierie_Sociale.docx"
---

Codification

PROC-SEC-001

Entrée en vigueur

Mars 2026

Mise à jour

[Date]

Procédure – Gestion des incidents d’ingénierie sociale

R. Remplacement

La présente procédure remplace PROC-SEC-001 v1.0 (Mars 2026), limitée au seul vecteur hameçonnage.

1. Objet

La présente procédure a pour objet de guider l’ensemble des employés, gestionnaires et partenaires dans la reconnaissance, le signalement et la gestion des incidents d’ingénierie sociale. Elle couvre l’ensemble des vecteurs d’attaque reposant sur la manipulation humaine, définis à la section 4.

Elle s’inscrit dans le cadre de la Politique de gestion des MVI (POL-SEC-001) et de la Directive de gestion des MVI (DIR-SEC-001), et est conforme aux obligations du Processus de gestion des menaces, vulnérabilités et incidents (GMVI) du Ministère de la Cybersécurité et du Numérique.

2. Champ d’application

La présente procédure s’applique à :

- tous les employés, contractuels, stagiaires et partenaires de l’organisation;

- tout appareil utilisé à des fins professionnelles, qu’il soit fourni par l’organisation ou personnel;

- tout canal de communication professionnel : courriel, SMS, appel téléphonique, code QR, messagerie instantanée.

3. Définitions

Terme

Définition

Ingénierie sociale

Technique d’attaque reposant sur la manipulation psychologique d’une personne plutôt que sur une exploitation technique, dans le but d’obtenir des informations, des accès ou des actions non autorisées.

hameçonnage (phishing)

Envoi massif de courriels frauduleux usurpant l’identité d’une organisation légitime.

harponnage (spear phishing)

Variante ciblée de l’hameçonnage visant un employé ou un cadre spécifique.

Fraude au président (BEC)

Usurpation de l’identité d’un dirigeant pour ordonner un virement ou obtenir des informations sensibles.

hameçonnage par SMS (smishing)

Attaque par message texte (SMS) frauduleux.

hameçonnage vocal (vishing)

Attaque par appel téléphonique frauduleux.

hameçonnage par QR (quishing)

Attaque par code QR malveillant redirigant vers un site frauduleux.

Usurpation d’identité interne

Imitation d’un employé ou d’un collègue pour obtenir un accès, une information ou un paiement.

Boîte Sécurité

Adresse de distribution centralisant les signalements d’incidents : securite@[organisation].ca.

COMSI

Coordonnateur Organisationnel des Mesures de Sécurité de l’Information – principal point de contact pour toutes les MVI. Rend compte au CSIO.

ROCD

Responsable opérationnel de cybersécurité du COCD – reçoit la déclaration du COMSI dès le niveau 2 GMVI.

Niveau GMVI

Niveau de coordination (1 à 4) défini par le processus GMVI, déterminant l’instance responsable et les obligations de déclaration.

4. Instructions

4.1 Vecteurs d’attaque couverts et signaux d’alerte

La présente procédure couvre les sept vecteurs suivants. La reconnaissance précoce d’un vecteur permet d’agir avant toute interaction.

Vecteur

Description

Signaux d’alerte typiques

hameçonnage (phishing)

Envoi massif de courriels frauduleux usurpant l’identité d’une organisation légitime.

Expéditeur mal épellé, urgence exagérée, lien suspect, pièce jointe inattendue.

harponnage (spear phishing)

Attaque ciblée et personnalisée visant un employé ou un cadre spécifique.

Message personnalisé avec informations réelles sur l’employé, ton familier, demande inhabituelle.

Fraude au président (BEC)

Usurpation de l’identité d’un dirigeant pour ordonner un virement ou divulguer des informations sensibles.

Demande urgente de virement, courriel de « direction » avec domaine légèrement modifié, pression temporelle.

hameçonnage par SMS (smishing)

Messages textes (SMS) frauduleux incitant à cliquer un lien ou à rappeler un numéro.

Numéro inconnu, lien courté (bit.ly), demande de confirm. de compte ou de livraison.

hameçonnage vocal (vishing)

Appels téléphoniques frauduleux visant à obtenir des informations sensibles ou accès à distance.

Appelant se présentant comme TI ou banque, demande de mot de passe ou d’accès à distance.

hameçonnage par QR (quishing)

Utilisation de codes QR malveillants redirigant vers des sites frauduleux.

QR code apposé sur affiche, courriel ou document, redirigeant vers une page de connexion.

Usurpation d’identité interne

Un acteur malveillant se fait passer pour un employé ou un collègue pour obtenir un accès, une information ou un paiement.

Demande inhabituelle d’un « collègue » via un canal non habituel, urgence, demande de discrétion.

💡 Règle universelle :  En cas de doute sur la légitimité d’un message, d’un appel ou d’un code QR — quelle que soit la plateforme — ne pas interagir et signaler immédiatement.

4.2 Instruction 1 – Réception d’un message suspect sans interaction

Applicable à tout message reçu (courriel, SMS, messagerie) dont la légitimité est douteuse et sur lequel aucune action n’a été effectuée.

1

Ne pas interagir

Ne pas cliquer sur les liens ni ouvrir les pièces jointes.

Ne pas répondre au message et ne pas le transférer à des collègues.

Pour un code QR : ne pas scanner. Photographier le support pour transmission à la sécurité.

2

Signaler à la Boîte Sécurité

Transmettre le message original en pièce jointe (.eml ou .msg pour les courriels) à securite@[organisation].ca.

Ne pas copier-coller uniquement le texte — les métadonnées techniques sont essentielles.

Pour SMS ou appel : noter le numéro, l’heure et le contenu, puis transmettre par courriel à la Boîte Sécurité.

3

Signaler dans Outlook (pour les courriels)

Clic droit sur le message → Signaler → Hameçonnage.

Conserver le message jusqu’à confirmation de l’équipe sécurité.

4.3 Instruction 2 – Une interaction a été effectuée

🚨 Important :  Ne paniquez pas. Signalez immédiatement. Une intervention rapide limite considérablement les dommages.

1

Isoler l’appareil du réseau

Débrancher le câble réseau OU désactiver le Wi-Fi.

Ne pas éteindre l’appareil — les traces mémoire sont essentielles à l’analyse forensique.

Pour un appel en cours (vishing) : raccrocher immédiatement, noter le numéro.

2

Contacter immédiatement le Service Bureautique ou la Boîte Sécurité

Par téléphone (poste : [XXXX]) ou en personne si la connexion est coupée.

Indiquer le vecteur d’attaque (courriel, SMS, appel, code QR), les actions effectuées et les informations potentiellement divulguées.

3

Ne pas toucher à l’appareil

Attendre les instructions de l’équipe sécurité.

Ne pas supprimer de fichiers, ne pas redémarrer, ne pas tenter de résoudre seul.

4.4 Consignes spécifiques selon l’interaction effectuée

Situation

Consignes à appliquer

Clic sur lien — aucune saisie

Isoler l’appareil. Signaler au Service Bureautique. Ne pas redémarrer. Analyse antivirus sur instruction.

Identifiants ou mot de passe saisis

Isoler l’appareil. Signaler immédiatement. Ne pas changer le mot de passe seul — cela compromet l’analyse. L’équipe sécurité procédera à la réinitialisation.

Pièce jointe ouverte ou exécutée

Isoler l’appareil. Ne pas éteindre. Signaler en urgence. Préparer le poste pour prise en charge forensique.

Informations bancaires ou financières divulguées

Contacter immédiatement l’institution financière pour signaler et faire opposition. Informer la Boîte Sécurité parallèlement.

Virement bancaire effectué (fraude au président)

Contacter en urgence l’institution financière pour tenter le rappel du virement (fenêtre très courte). Informer immédiatement le COMSI et la direction. Conserver toutes les communications.

Accès à distance accordé (vishing)

Couper l’accès immédiatement si possible. Isoler l’appareil. Signaler en urgence. Ne pas réutiliser l’appareil.

Code QR scanné

Ne pas saisir d’informations sur la page ouverte. Fermer le navigateur. Signaler en indiquant l’URL affichée si visible.

Appel suspect reçu (vishing) — aucune info divulguée

Raccrocher. Signaler à la Boîte Sécurité en notant le numéro, l’heure, le contenu de l’appel.

4.5 Informations à fournir lors du signalement

Lors de tout signalement, fournir les informations suivantes dans la mesure du possible :

- Type de vecteur : courriel, SMS, appel téléphonique, code QR, messagerie.

- Adresse courriel, numéro de téléphone ou domaine de l’attaquant apparent.

- Date et heure de réception et, le cas échéant, de l’interaction.

- Description des actions effectuées (clic, saisie, téléchargement, appel retouré, virement).

- Informations potentiellement divulguées (type, non la valeur des mots de passe).

- Tout comportement anormal observé sur l’appareil après l’incident.

- Capture d’écran ou photo du message / code QR si réalisable sans risque supplémentaire.

📬 Contacts – Boîte Sécurité :  securite@[organisation].ca  |  Poste interne : [XXXX]  |  Lundi au vendredi, 8 h – 17 h

4.6 Situations nécessitant un signalement systématique

Les situations suivantes exigent un signalement à la Boîte Sécurité, même en l’absence d’interaction :

- Réception de tout message suspect, quel que soit le canal.

- Doute sur la légitimité d’un appel téléphonique reçu.

- Découverte d’un code QR dont l’origine est incertaine.

- Toute interaction effectuée, même minime, avec un contenu suspect.

- Comportement inhabituel d’un système après réception d’un message.

- Signalement par un collègue du même message ou appel.

- Réception d’une demande inhabituelle prétendant provenir de la direction ou d’un collègue.

4.7 Classification GMVI et obligations de déclaration

La Boîte Sécurité classe chaque incident selon les niveaux du processus GMVI. Les niveaux déterminent les obligations de déclaration gouvernementale :

Niveau GMVI

Critères de déclenchement

Première action de déclaration

Niveau 1

Incident géré entièrement à l’interne (ex. : courriel suspect sans interaction, clic sans saisie).

COMSI informe le CSIO. COMSI déclare au ROCD (flux GMVI externe). Documentation au registre.

Niveau 2

Incident dépassant les capacités internes, touchant plusieurs employés ou systèmes, ou nécessitant coordination externe.

COMSI déclare au ROCD sans délai. Formulaire MVI transmis.

Niveau 3-4

Impact gouvernemental élargi, données sensibles de plusieurs OP, propagation confirmée.

COCD déclare au CGCD. Formulaire MVI obligatoire. CGCD coordonne.

⚠️ Obligation GMVI :  Toute MVI de niveau 2 et plus doit être portée à la connaissance du CSIO (hiérarchie interne OP) ET déclarée au ROCD (obligation GMVI externe) sans délai par le COMSI, conformément à DIR-SEC-001. Ces deux obligations sont simultanées.

4.8 Rappels importants

🚫 Rappel 1 :  Aucune organisation légitime ne vous demandera jamais votre mot de passe par courriel, SMS, téléphone ou code QR.

🚫 Rappel 2 :  Signaler un incident suspect n’est pas une faute. L’erreur serait de ne pas signaler. Votre vigilance protège toute l’organisation.

🚫 Rappel 3 :  Les attaques d’ingénierie sociale sont conçues pour contourner le jugement humain. Même un employé expérimenté peut être ciblé. Ne vous jugez pas : agissez.

5. Rôles et responsabilités

Acteur

Responsabilités

Tous les employés

Reconnaître les vecteurs d’ingénierie sociale, ne pas interagir avec les contenus suspects, signaler immédiatement selon la présente procédure.

Gestionnaires

S’assurer que les membres de leur équipe connaissent la procédure. Encourager le signalement sans crainte de représailles. Signaler eux-mêmes tout incident, y compris les tentatives de fraude au président.

Service Bureautique

Recevoir et consigner les signalements, effectuer la qualification initiale, transmettre à la Boîte Sécurité avec les informations structurées. Effectuer les premiers gestes techniques selon le niveau.

Boîte Sécurité

Analyser les signalements, effectuer le triage et la classification GMVI, coordonner la réponse technique, notifier le COMSI selon le niveau détecté.

COMSI

Rendre compte au CSIO de toutes les MVI. Déclarer toute MVI de niveau 2 et plus au ROCD (obligation GMVI externe, simultanée).

CSIO

Responsable de la prise en charge de toutes les MVI au niveau de l’OP. Approuver les décisions stratégiques et les communications. Notifier la CAI en cas d’atteinte aux renseignements personnels (Loi 25).

MAJ. Mise à jour

Ce document est placé sous la responsabilité du COMSI et doit être révisé :

- Annuellement, après tout incident de niveau 3 ou supérieur, ou lors de toute modification du processus GMVI ou de l’évolution des vecteurs d’attaque

- Après tout changement organisationnel majeur affectant les rôles décrits.

- Lors de toute évolution significative du cadre réglementaire applicable.

A. Approbation

Fonction

Nom

Signature

Date

[Titre]

[Prénom Nom]

📎 Documents connexes :  POL-SEC-001  |  DIR-SEC-001  |  PB-BUR-001  |  PB-SEC-001  |  PB-COMSI-001  |  PB-CSIO-001  |  PB-GEN-001  |  Processus GMVI (MCN/CGCD)
