# lab2-Rooting_Android
Application testée : DIVA (Damn Insecure and Vulnerable App)
Version : 1.0 (Beta)
AVD : android 9 (Émulateur Memu)
Objectif du TP : Comprendre les mécanismes du rooting.

# Rooter l'AVD
<img width="799" height="412" alt="Image" src="https://github.com/user-attachments/assets/fe156721-062d-4900-86a7-0468a0fe6746" />

<img width="882" height="425" alt="Image" src="https://github.com/user-attachments/assets/bbfa5b7b-3c1e-4904-aab5-e63463fb5f9a" />


<img width="838" height="563" alt="Image" src="https://github.com/user-attachments/assets/9bcc2fbb-5066-4a6f-9830-452c80b21497" />
# Démarrer un AVD PROPRE
<img width="694" height="71" alt="Image" src="https://github.com/user-attachments/assets/9839c9a6-735d-48f5-a3ad-91fb9e6202af" />

<img width="389" height="826" alt="Image" src="https://github.com/user-attachments/assets/43da7e8b-9af8-4681-bbc9-c0b57f1e6e7f" />
# Installer et lancer DIVA
<img width="995" height="300" alt="Image" src="https://github.com/user-attachments/assets/d51bf374-66e3-4e80-b35e-226d7ed6264b" />

<img width="1011" height="81" alt="Image" src="https://github.com/user-attachments/assets/cdd03891-a468-4f9a-b297-4d132cddfaa8" />

<img width="435" height="794" alt="Image" src="https://github.com/user-attachments/assets/52b6f6ca-1f94-4b86-a1ba-8f3ee7bbddf7" />
# 3 scénarios simples
Rechercher un item Sélection du module " INSECURE LOGGING"
<img width="411" height="712" alt="Image" src="https://github.com/user-attachments/assets/8650d188-a99b-45b9-b168-4eb106a140b8" />

Ouvrir un détail
<img width="415" height="693" alt="Image" src="https://github.com/user-attachments/assets/b7099a29-4242-4ccb-a2cd-5c5063fc1dd3" />

problémes d'accées

<img width="402" height="763" alt="Image" src="https://github.com/user-attachments/assets/fe6369dc-f59c-4da7-80cd-8496c63c952f" />

# Sécurité Android : Vue d’Ensemble
Android s’appuie sur une conception de sécurité en plusieurs niveaux afin d’assurer la protection des données et la fiabilité du système.Chaque application est isolée grâce au mécanisme de sandboxing, qui empêche toute interaction directe non autorisée entre processus.Le modèle de permissions contrôle strictement l’accès aux ressources critiques (stockage, caméra, contacts, etc.).Par ailleurs, l’intégrité du système empêche les modifications non légitimes des composants essentiels de l’OS.
Lorsque le système est rooté, ces mécanismes fondamentaux sont affaiblis, car l’accès super-utilisateur permet de contourner les restrictions natives et d’obtenir un contrôle global sur l’environnement Android.

#Verified Boot
L’appareil utilisé fonctionne sous Android 9, version prenant en charge le mécanisme Verified Boot.
Cependant, la propriété système associée n’est pas disponible. Cette absence suggère fortement que le bootloader est déverrouillé, ce qui rend impossible la consultation fiable de l’état de sécurité.

# Rooting : Définition et Impact
Le rooting correspond à l’obtention des privilèges super-utilisateur (UID 0).
Ce niveau d’accès permet un contrôle complet du système Android.

En conséquence :
Les protections natives comme Verified Boot peuvent être contournées.Le sandboxing peut être neutralisé.La confiance accordée à l’intégrité du système est profondément altérée.
Un environnement rooté contrôlé permet d’analyser en profondeur la sécurité d’une application.
Grâce aux privilèges élevés, il devient possible d’examiner des éléments internes normalement inaccessibles, notamment au niveau du stockage interne et des fichiers système.
Cette approche facilite l’identification de faiblesses structurelles ou de mauvaises pratiques de sécurité.

#Analyse des Risques
Travailler sur un système rooté implique plusieurs risques :L’intégrité globale du système ne peut plus être garantie.Les résultats des tests peuvent être influencés par la modification de l’environnement.Si l’appareil sort du cadre du laboratoire, la surface d’attaque devient beaucoup plus large.Le dispositif devient potentiellement vulnérable aux malwares et aux attaques externes.Mesures de Sécurisation du Laboratoire
Afin de limiter ces risques, plusieurs précautions ont été appliquées :Isolation réseau complète pour empêcher toute communication non autorisée.Utilisation exclusive de données fictives afin d’éviter toute fuite réelle.Support dédié uniquement aux expérimentations.Absence de comptes personnels sur l’appareil de test.Installation d’APK provenant de sources vérifiées.Documentation systématique de chaque étape à l’aide de captures d’écran horodatées.

# Référentiel OWASP MASVS
Le standard OWASP MASVS définit les exigences de sécurité applicables aux applications mobiles.
L’exigence MASVS-STORAGE-1 stipule que toute donnée sensible (mots de passe, clés API, tokens) doit être chiffrée avant d’être stockée localement.

#Référentiel OWASP MASTG
Le MASTG complète le MASVS en proposant des méthodologies techniques d’audit.Deux types de tests ont été effectués :
1. Test de stockageInspection directe du répertoire :/data/data/jakhar.aseem.diva/shared_prefs/
L’accès root a permis de constater la présence d’identifiants stockés en clair.

2. Analyse dynamiqueUtilisation de la commande adb logcat afin de surveiller les flux en temps réel.
Cette analyse a révélé des fuites d’informations dans les journaux système.

# Traçabilité de l’Audit
Informations Générales :Auditeur : BOUDHIH HAJAR ,Date : 14 Février 2026 ,Environnement : MEmu Android Emulator,Système : Android 9,Application testée : DIVA

Éléments de Preuve:
Des captures d’écran ont été réalisées pour documenter :Le lancement de l’application, L’activation du mode root ,L’état du Verified Boot, La consultation des données sensibles

# État Final
Les tests ont été réalisés dans un environnement virtualisé, dépourvu des protections standards actives.

# Remise à Zéro de l'Environnement


<img width="703" height="398" alt="Image" src="https://github.com/user-attachments/assets/7c3eb46f-3ca8-4994-860a-e23017f06b2d" />

<img width="718" height="553" alt="Image" src="https://github.com/user-attachments/assets/10df6e14-4a5d-4338-9753-ad2283cf2985" />

<img width="454" height="806" alt="Image" src="https://github.com/user-attachments/assets/5d884224-0760-41be-9637-12bad333e5c5" />
