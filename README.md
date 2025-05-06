# Gouvernance-des-donn-es

# 🚗 TP-OC02 : Plateforme MQTT pour Véhicules Connectés

Ce dépôt regroupe les travaux pratiques réalisés dans le cadre du module IoT, autour de la conception, du déploiement et de la sécurisation d'une **plateforme MQTT** destinée aux véhicules connectés. Le projet se déroule en deux étapes :
![image](https://github.com/user-attachments/assets/6ef11ebc-b9c8-4519-bb33-68aeefe17857)


- **TP-OC02** : Mise en place d’une plateforme fonctionnelle MQTT
- **TP_OC02_Securite** : Sécurisation avancée de la plateforme

---

## 🧩 TP-OC02 – Mise en place d’une plateforme MQTT

Cette première partie vise à concevoir une plateforme permettant l’échange de données entre des véhicules connectés et un serveur d’infrastructure via le protocole MQTT.

### 🔧 Fonctionnalités implémentées

- Déploiement d’un broker **Mosquitto**
- Simulation de capteurs embarqués avec **Python (Paho-MQTT)**
- Transmission de données de télémétrie à l’aide de **topics hiérarchiques**
- Envoi de **commandes** vers les véhicules
- Traitement des messages côté serveur

---

## 🔐 TP_OC02_Securite – Sécurisation de la plateforme MQTT

Cette seconde partie porte sur la sécurisation du système afin de prévenir les menaces courantes en IoT (interception, accès non autorisé, etc.).

### ✅ Objectifs atteints

1. **Authentification utilisateur**
   - Configuration d’un fichier `passwd_mqtt`
   - Désactivation des connexions anonymes

2. **Chiffrement TLS**
   - Génération de certificats avec **OpenSSL**
   - Activation des connexions sécurisées (port 8883)
   - Intégration de `tls_set()` dans les scripts Python

3. **Contrôle d'accès (ACL)**
   - Mise en place d’une hiérarchie de topics restreints (`envirocar/telemetry/...`)
   - Attribution de permissions spécifiques à chaque utilisateur

4. **Modèle requête-réponse sécurisé**
   - Implémentation d’un échange de commandes avec retour via MQTT
   - Utilisation de timestamps, identifiants uniques et signatures simples

5. **Analyse de vulnérabilités**
   - Capture réseau avec **Wireshark**
   - Test d’accès non autorisé à des topics
   - Documentation des attaques possibles et des contre-mesures

---

## 💡 Réflexions et analyses

Des questions de réflexion ont été abordées tout au long des TP afin d’analyser les enjeux de sécurité et de structuration des données dans un système MQTT.

### Partie 1 – Gouvernance des données
- Avantages et limites du modèle **Publish/Subscribe**
- Organisation optimale des **topics** pour assurer une bonne hiérarchisation
- Risques de sécurité en l’absence d’authentification
- Bonnes pratiques pour l'échange de données sensibles entre dispositifs

### Partie 2 – Sécurité des échanges
- Comparaison entre **trafic MQTT non chiffré** (port 1883) et **sécurisé TLS** (port 8883)
- Démonstration des **attaques MitM** et rôle du **chiffrement TLS**
- Importance des **ACL** pour compartimenter les communications
- Rôle de la sécurité en couches dans une architecture IoT (défense en profondeur)

---

## 🔎 Technologies utilisées

- **Mosquitto** : broker MQTT open source
- **Paho-MQTT** : client Python MQTT
- **OpenSSL** : génération de certificats TLS
- **Wireshark** : analyse réseau
- **Python** : scripts de simulation et traitement des données

---


---

## ✍️ Auteur

👩‍💻 Belvine YEMDJO YOUMBI réalisé dans le cadre du Cloud & de la Gouvernance de la donnée

📚 Année : 2025

---




