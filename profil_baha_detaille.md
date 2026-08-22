# Profil détaillé — Baha Eddine Belhaj Mouldi

> Document de synthèse compilé à partir de l'ensemble des CVs (.tex) du dossier CVtravaille et du profil LinkedIn (linkedin.com/in/bahamouldi).

---

## 1. Identité & positionnement général

**Nom complet :** Baha Eddine Belhaj Mouldi
**Diplôme :** Ingénieur, École Nationale d'Ingénieurs de Tunis (ENIT) — 2026, **mention Très Bien**
**Localisation :** El Manar, Gouvernorat Tunis, Tunisie
**Contact :** bahaeddine.belhajmouldi@gmail.com / bahamouldi123@gmail.com — +216 55 128 982
**LinkedIn :** linkedin.com/in/bahamouldi (500+ relations, 2 561 abonnés)
**Poste actuel :** Backend Developer (freelance) chez ZForm

### Positionnement stratégique observé

Votre dossier de candidature n'est pas un CV unique mais un **système de ~30 variantes de CV**, chacune calibrée pour un poste, une entreprise ou un pays précis. Cette stratégie de "micro-ciblage" est cohérente avec un profil hybride qui touche à la fois :
- la sécurité informatique (offensive, défensive, GRC, SOC)
- l'intelligence artificielle / machine learning appliqués à la sécurité
- le développement logiciel (fullstack, backend, data engineering)
- le DevOps / infrastructure cloud

Le point commun qui traverse presque tous les CVs est le **projet BeeWAF**, réutilisé comme preuve de compétence sous des angles différents selon l'axe visé.

---

## 2. Formation

| Établissement | Période | Détail |
|---|---|---|
| École Nationale d'Ingénieurs de Tunis (ENIT) | sept. 2023 – mai 2026 | Ingénieur, mention Très Bien. Compétences déclarées : J2EE Web Services, HTML5, +6 autres |
| Institut préparatoire aux études d'ingénieurs d'El Manar (IPEIEM) | sept. 2021 – juil. 2023 | Classes préparatoires, rang 62/700, spécialité Python |

### Certifications
- **NVIDIA** — Fundamentals of Deep Learning (réseaux de neurones, entraînement de modèles, applications pratiques)
- **NVIDIA** — Introduction to Transformer-Based Natural Language Processing (févr. 2025)
- **Cisco** — CCNA: Introduction to Networks (janv. 2025)

---

## 3. Expérience professionnelle (ordre chronologique inverse)

### ZForm — Backend Developer (freelance) — depuis août 2026
Plateforme GovTech. APIs REST en JavaScript/TypeScript, Node.js. Workflows de développement assisté par IA. Sprints Agile. Prise de relais sur un projet en production.

### Digital Power Consulting — Ingénieur Sécurité IA / WAF (stage) — févr. 2026 à juin 2026
**Projet phare : BeeWAF** (voir section 4 pour le détail complet). Stage effectué aux Berges du Lac 1, sur site, encadré par Mme Oueslati Rihem (Digital Power Consulting) et Mme Aida Ben Chehida Douss (ENIT). Ce stage constitue le PFE (Projet de Fin d'Études), soutenu le 25 juin avec mention Très Bien.

### Streamlink — Stagiaire Détection de menaces SAP (stage) — juil. 2025 à sept. 2025 (3 mois)
- SAP BASIS & Infrastructure Security
- Administration système SAP, environnement S/4HANA
- Conception de rôles à privilège minimal (least-privilege)
- Revues de séparation des tâches (Segregation of Duties — SoD) sur des transactions SAP sensibles
- Détection de menaces sur l'infrastructure SAP

### Tunisie Telecom — Stagiaire Sécurité réseau (stage) — juil. 2024 à août 2024 (2 mois)
Sécurité des infrastructures réseau (détails limités dans les CVs disponibles).

### VMate — Chef de projet technique (indépendant) — janv. 2024 à juin 2024 (6 mois)
Rôle de gestion de projet technique en indépendant.

---

## 4. Projet phare : BeeWAF

Le projet central de tout votre positionnement professionnel, développé pendant le PFE chez Digital Power Consulting / Beehive Entreprises. Contexte : remplacer des solutions commerciales de WAF (F5, Imperva — coûtant des dizaines de milliers d'euros/an et jugées trop rigides) par une solution interne sur mesure.

### Caractéristiques techniques
- **Pipeline de 27 modules d'inspection** empilés
- **9 800 à 10 041 règles regex** (le chiffre varie légèrement selon les CVs)
- **Moteur Machine Learning** : Random Forest + Gradient Boosting
  - 92,3 % d'accuracy
  - 98,2 % de precision
  - Entraîné et validé sur le dataset **CSIC 2010**
- **Virtual patching** de 37 à 80 CVE selon la variante de CV
- **Conformité continue** vérifiée en temps réel sur 7 référentiels de sécurité :
  - OWASP
  - PCI DSS
  - GDPR
  - SOC2
  - NIST
  - ISO 27001
  - HIPAA
- **Infrastructure de déploiement** :
  - Production sur **Kubernetes**
  - Pipeline CI/CD **Jenkins + ArgoCD** (approche GitOps)
  - Monitoring **Prometheus / Grafana** + **ELK stack**
- **Performance** : latence médiane ajoutée **< 20 ms**
- **Résultats de tests de sécurité** :
  - 100 % des attaques OWASP Top 10 bloquées lors des tests
  - Anecdote marquante : lancement de **sqlmap** contre BeeWAF, message obtenu : *"it appears that you have been blocked by the target server"*
- **En production** : filtre le trafic réel de deux applications d'entreprise

### Utilisation dans les différents CVs
BeeWAF est mentionné et adapté dans la quasi-totalité de vos CVs de sécurité, avec un angle de présentation différent selon le poste ciblé :
- Angle **IA/ML** pour les postes "AI/ML Security Engineer"
- Angle **AppSec/pentest** pour les postes de sécurité applicative
- Angle **DevSecOps** pour les postes cloud/CI-CD
- Angle **SOC** pour les postes d'analyste sécurité opérationnelle
- Angle **conformité/GRC** pour les postes de gestion des risques

---

## 5. Projets académiques marquants

### WebSec Scanner (PFA2 — projet de fin d'année 2)
Application web de détection et vérification automatique de vulnérabilités.

**Stack technique :**
- Frontend : **Angular 18** — composants modulaires, `SafeHtmlPipe` pour rendu sécurisé, guide utilisateur intégré
- Backend : **Spring Boot 3.4.2 (Java 21)** — architecture RESTful, Spring Security (JWT, rôles, CSRF), Spring Data JPA + MySQL, Spring WebSocket, iText (html2pdf)

**Fonctionnalités :**
- Détection automatique : SQL Injection, XSS, CSRF et autres vulnérabilités web
- Scans asynchrones avec cache local — temps de scan réduit à 8-10 minutes
- Alertes temps réel via WebSocket et email
- Rapports HTML & PDF générés dynamiquement avec recommandations
- Authentification JWT + BCrypt, gestion de rôles (USER / ADMIN)
- Planification de scans (quotidien, hebdomadaire, personnalisé)
- Interface responsive (Chrome, Firefox, Edge)

**Tests réalisés :**
- Scans de validation sur **DVWA** et **bWAPP**
- Tests fonctionnels API avec **Postman**
- Tests de charge avec **JMeter** (500 utilisateurs simulés)
- Temps de réponse moyen : 200 ms
- Compatibilité multi-navigateurs vérifiée

Encadrant : M. Hamza Hammami.

### AIDLINK (projet Génie Logiciel / Agile)
Application de gestion de dons pour une association (mobilier, électroménager, articles ménagers).
- Méthodologie Agile/Scrum en équipe (rôle non spécifié comme dev — collègue Hassine BEKEY était Scrum Master)
- Prototype Figma interactif : gestion des dons, suivi de stock temps réel, module de recherche, tableau de bord statistiques
- Outils : Trello (sprint planning), Figma (prototypage UI/UX)

### Analyse de sécurité Wi-Fi (Kali Linux)
Tutoriel/démonstration pédagogique en collaboration avec un collègue (Slim Hassen) :
- Utilisation d'**aircrack-ng** et **aireplay-ng**
- Capture de handshake WPA, tentative de crack avec wordlist filtrée (rockyou.txt)
- Objectif déclaré : sensibilisation à la sécurité Wi-Fi et pentest éthique/autorisé

---

## 6. Cartographie complète des CVs par domaine

### 6.1 Sécurité IA / Machine Learning / Data-AI

| Fichier | Langue | Cible / Positionnement |
|---|---|---|
| `cv_baha_ai_ml_security.tex` / `_fr.tex` | EN / FR | AI/ML Security Engineer — WAF intelligent, ML adversarial, RAG/LangChain, architectures multi-agents (doublon EN/FR) |
| `cv_baha_data_ai.tex` / `_fr.tex` | EN / FR | Data & AI Engineer — pipelines de données (900K+ enregistrements), dashboards BI, RAG, web sémantique (doublon EN/FR) |
| `cv_baha_ia_langgraph.tex` | FR | Ingénieur IA — spécialisation LangGraph, RAG, LLM, orchestration multi-agents |
| `cv_baha_medius.tex` | EN | AI Software Engineer — RAG/LLM, FastAPI, automatisation finance/back-office, AI-assisted coding |

### 6.2 Sécurité applicative / DevSecOps

| Fichier | Langue | Cible / Positionnement |
|---|---|---|
| `cv_baha_devsecops.tex` / `_fr.tex` | EN / FR | DevSecOps / Cloud Security Engineer — Docker/K8s, CI/CD, ELK, WAF, sécurité web/API (doublon EN/FR) |
| `cv_baha_medius_security.tex` | EN | Web Application Security Engineer (Medius) — AppSec, pentest, BeeWAF (10 041 règles), OWASP/API/LLM Top 10 |
| `cv_baha_sap_security.tex` / `_fr.tex` | EN / FR | SAP BASIS & Security Engineer — niche SAP BASIS + sécurité, Fiori, détection de menaces (doublon EN/FR) |

### 6.3 SOC / Sécurité opérationnelle

| Fichier | Langue | Cible / Positionnement |
|---|---|---|
| `cv_baha_sagemcom_soc.tex` | FR | Analyste SOC Junior (Sagemcom) — SOC + Python + IA/ML sécurité + DevSecOps, profil junior polyvalent |
| `cv_baha_uib_soc.tex` | FR | Ingénieur Sécurité SOC (UIB) — cycle SOC complet, AD/Windows/Linux, PKI/MFA/PAM/IAM, BeeWAF |
| `cv_salt_junior_cybersecurity.tex` / `_fr.tex` | EN / FR | Junior Cybersecurity Specialist (Salt) — SIEM, triage d'alertes, tests web/API, jeune diplômé (doublon EN/FR) |

### 6.4 GRC / Gestion des risques

| Fichier | Langue | Cible / Positionnement |
|---|---|---|
| `cv_baha_grc_risk_belgium.tex` | EN | Cyber Security Risk / GRC Consultant (Bruxelles) — ISO 27001, NIST, gestion de risques/vulnérabilités, IAM. **CV déjà envoyé à Hannah Moriarty (Strativ), en attente de réponse depuis le 18 août** |

### 6.5 Sécurité offensive

| Fichier | Langue | Cible / Positionnement |
|---|---|---|
| `cv_baha_hilti_offensive_security.tex` | EN | Cybersecurity Intern — Offensive Security — pentest, WAF, gestion de vulnérabilités (profil stage) |

### 6.6 DevOps / Infrastructure Cloud

| Fichier | Langue | Cible / Positionnement |
|---|---|---|
| `cv_baha_neoshore_devops_infra.tex` | FR | Ingénieur DevOps Senior — Infra (Neoshore) — ton "senior infrastructure/cloud", ⚠️ incohérent avec le reste du profil junior |
| `cv_baha_symolia_devops.tex` | FR | Ingénieur DevOps/Backend (Symolia) — Python/Kubernetes/Azure |
| `cv_baha_xefort_devops.tex` | EN | DevOps Engineer (Xefort) — Cloud/CI-CD/K8s/Terraform/AWS |

### 6.7 Fullstack / Développement Java Enterprise

| Fichier | Langue | Cible / Positionnement |
|---|---|---|
| `cv_baha_bhct_fullstack_java_react.tex` | FR | Développeur Full Stack Java/ReactJS (BHCT) — Java/Spring Boot + React, ⚠️ "3+ ans d'expérience" incohérent avec profil jeune diplômé |
| `cv_baha_talan_java_angular.tex` | FR | Full Stack Java/Angular (Talan) — Spring Boot/Kafka/Angular/microservices |
| `cv_baha_clevertech_java_spring.tex` | FR | Ingénieur Java Spring Backend/Fullstack (Clevertech) — Kafka event-driven, SOLID, Angular/React |

### 6.8 Fullstack moderne / Data Engineering

| Fichier | Langue | Cible / Positionnement |
|---|---|---|
| `cv_baha_fullstack.tex` / `_en.tex` | FR / EN | Ingénieur Full-Stack — React/Next.js/Python (doublon FR/EN) |
| `cv_baha_fullstack_security.tex` / `_fr.tex` | EN / FR | Full Stack/Backend Engineer — Security-Oriented (doublon EN/FR) |
| `cv_baha_fullstack_KUWAIT.tex` | EN | Full-Stack Developer — Security-Oriented, variante géographique Koweït, ⚠️ pas de PDF généré |
| `cv_baha_speedykom_data_fullstack.tex` | FR | Data Engineer/Full-Stack (Speedykom) — Python/SQL/Next.js/ClickHouse/Airflow |
| `cv_baha_zform.tex` | EN | Backend Developer (ZForm) — JS/TS + Python, GovTech, AI-assisted dev (poste actuel) |

### 6.9 Niche

| Fichier | Langue | Cible / Positionnement |
|---|---|---|
| `cv_baha_shindan.tex` | FR | Fullstack Developer TypeScript (Shindan) — TypeScript + composante sécurité mobile |

### 6.10 Lettres de motivation associées
`lettre_baha_sofrecom`, `lettre_baha_speedykom_data_fullstack`, `lettre_baha_symolia_devops`, `lettre_baha_talan_java_angular`, `lettre_baha_vneuron_cybersecurity_analyst`, `lettre_baha_zform`, `lettre_baha_deloitte_junior_analyst`, `lettre_baha_hilti_offensive_security`, `lettre_baha_uib_soc`

---

## 7. Compétences techniques consolidées (vue transversale)

### Sécurité
Pentest web/API, OWASP Top 10 / API Top 10 / LLM Top 10, conception et exploitation de WAF, SIEM, gestion des identités et des accès (IAM/PAM/MFA/PKI), GRC (ISO 27001, NIST CSF, PCI DSS, GDPR, SOC2, CIS, HIPAA), SAP Basis & Fiori security, sécurité réseau, Kali Linux / aircrack-ng.

### Intelligence artificielle / Machine Learning
RAG (Retrieval-Augmented Generation), LangChain / LangGraph, LLM, architectures multi-agents, FastAPI, Random Forest, Gradient Boosting, NLP / Transformers, deep learning (NVIDIA-certifié).

### Développement logiciel
- Backend : Java/Spring Boot, Node.js/TypeScript, Python, FastAPI
- Frontend : Angular (14 à 18), React, Next.js
- Messaging/event-driven : Kafka
- Bases de données : MySQL, ClickHouse, JPA

### Data Engineering
Pipelines de données à grande échelle (900K+ enregistrements), Airflow, dashboards BI, web sémantique.

### DevOps / Cloud
Docker, Kubernetes, Jenkins, ArgoCD (GitOps), Terraform, AWS, Azure, GCP, Prometheus, Grafana, ELK Stack.

### Réseaux
CCNA (Cisco) — fondamentaux réseau.

---

## 8. Activité et visibilité LinkedIn

- **102 vues de profil**, **1 229 impressions de posts** (7 derniers jours), **28 apparitions dans les recherches**
- Post le plus performant : annonce du PFE/BeeWAF — **1 181 impressions**, 21 réactions
- Post "Nouveau portfolio en ligne" (bahamouldi.github.io) — **2 554 impressions**
- Republication d'une recruteuse (Zayneb Jebali) présentant activement votre profil comme "Ingénieur Cybersécurité & Intelligence Artificielle" recherchant une opportunité
- **Section "Résumé" absente** — LinkedIn signale que les profils avec résumé reçoivent jusqu'à 3,9x plus de vues

### Candidature en cours de suivi
- **Hannah Moriarty** (Strativ, recruteuse IT Infra & Cyber Security Europe) — candidature envoyée le 18 août pour un poste **Cyber Security Risk / GRC Consultant à Bruxelles** (hybride, freelance), CV `cv_baha_grc_risk_belgium.pdf` joint. **Aucune réponse à ce jour.**

---

## 9. Incohérences et points d'attention identifiés

1. **7 paires de CVs quasi-identiques EN/FR** (ai_ml_security, data_ai, devsecops, fullstack_security, fullstack, sap_security, salt_junior_cybersecurity) — cohérent si l'objectif est le bilinguisme, mais à vérifier que les deux versions restent synchronisées à chaque mise à jour.

2. **Incohérence de séniorité** : la majorité des CVs présentent un profil jeune diplômé/stagiaire, mais `cv_baha_bhct_fullstack_java_react.tex` et `cv_baha_neoshore_devops_infra.tex` affichent "3+ ans d'expérience" / "Senior" — à clarifier si volontaire (CV pour un poste où l'on gonfle l'expérience) ou erreur de template copié-collé.

3. **`cv_baha_fullstack_KUWAIT.tex`** n'a pas de PDF généré correspondant — potentiellement non compilé ou abandonné.

4. **Dispersion du positionnement** : avec 5 identités professionnelles différentes (sécurité IA, SOC, GRC, DevOps, Fullstack), le message envoyé aux recruteurs peut manquer de netteté. Un recruteur spécialisé en SOC pourrait percevoir le profil comme "pas assez SOC pur" et inversement pour chaque axe.

5. **BeeWAF comme pièce unique** : c'est votre meilleure preuve de compétence concrète (métriques précises, production réelle, conformité vérifiée), mais c'est aussi votre seule expérience professionnelle substantielle en sécurité — le reste du parcours (stages plus courts) vient en appui.

---

*Document généré automatiquement à partir de l'analyse des fichiers .tex du dossier CVtravaille et du profil LinkedIn public de Baha Mouldi.*
