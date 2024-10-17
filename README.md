# TSSR-2409-P1-G3-Scanner-de-ports

# **README**

## **SOMMAIRE**

### 1. [Présentation du projet et des objectifs finaux](https://github.com/WildCodeSchool/TSSR-2409-P1-G3-Scanner-de-ports/blob/main/README.md#1-pr%C3%A9sentation-du-projet-et-des-objectifs-finaux-1)

### 2. [Introduction: mise en contexte](https://github.com/WildCodeSchool/TSSR-2409-P1-G3-Scanner-de-ports/blob/main/README.md#2--introduction-mise-en-contexte)
    
### 3. [Membres du groupe et rôle (s1 et s2)](https://github.com/WildCodeSchool/TSSR-2409-P1-G3-Scanner-de-ports/blob/main/README.md#3-membres-du-groupe-et-r%C3%B4le-s1-et-s2-1)
    
### 4. [Méthode choisie pour la mission]
    
### 5. [Nmap c'est quoi](https://github.com/WildCodeSchool/TSSR-2409-P1-G3-Scanner-de-ports/blob/main/README.md#6-nmap-cest-quoi)

---
### 1. Présentation du projet et des objectifs finaux

L'objectif de ce projet est de trouver les failles de sécurité d'un serveur en utilisant la métohde de scan de ports.  
Pour mener à bien ce projet, nous aurons recours au logiciel Nmap, qui va nous permettre de scanner les ports d'un serveur déterminé.  
Une fois ces failles repérées via le logiciel Nmap, il sera primordial de prendre les mesures nécessaires afin de les corriger, dans un soucis de sécurité.

---

### 2.  Introduction: mise en contexte

intro ici:

*
*
*
---

### 3. Membres du groupe et rôle (s1 et s2)  

Notre groupe est composé de 4 personnes : Elsa, Yohann, Lionel et Souhail.  
Voici les tâches et les rôles qui ont été affectés pour le premier et le deuxième sprint :  
> ### Premier sprint :
* **Yohann** : Occupant le rôle de *Scrum Master* sur le premier sprint, le rôle de Yohann a été d'organiser les réunions, de contribuer à la gestion du backlog product et de mener des rétrospectives.
Les tâches qui lui ont été affectées étaient les suivantes : faire des recherches sur Netcat et Nmap, comparer les deux logiciels afin de choisir lequel serait utilisé pour notre projet, installer Nmap et effectuer les premiers tests du logiciel.

* **Souhail** : Son rôle pour ce premier sprint a été *Product Owner*. Il était l'intermédiaire entre son équipe et le Product owner, il encourageait l'équipe et étant garant du bon déroulement de ce premier sprint.
Quant à ses tâches, il lui ont été confiés l'installation et le paramétrage du serveur (modification du nom, du groupe et de l'adresse Ip)

* **Elsa** : Pour ce premier sprint, Elsa a été chargée de plusieurs tâches techniques cruciales, parmi lesquelles l'installation complète d'un client sur l'environnement dédié. Cette installation devait être réalisée en respectant les spécifications définies en amont afin d'assurer un fonctionnement optimal. Une fois le client installé, elle a également pris en charge le paramétrage détaillé, qui comprenait notamment la création d'une session utilisateur dédiée, la définition des droits d'accès appropriés, ainsi que la configuration du mot de passe pour garantir la sécurité des accès. En plus de cela, Elsa a été responsable du paramétrage de l'adresse IP, en s'assurant qu'elle soit correctement configurée pour permettre la communication réseau fluide et sécurisée entre le client et le reste de l'infrastructure. L'ensemble de ces tâches nécessitait une attention particulière aux détails pour éviter tout problème potentiel lors de l'utilisation du client


* **Lionel** : Lionel avait pour mission de prendre en charge plusieurs tâches importantes dans le cadre du projet, notamment la rédaction complète de la documentation pour Nmap. Cela impliquait non seulement de fournir une description de l'outil, mais aussi d'expliquer son utilisation et ses options de configuration. En parallèle, Lionel devait également installer le logiciel sur l'environnement client, veillant à ce que l'installation se déroule sans encombre, en respectant les exigences techniques spécifiques de la plateforme du client. Une fois l'installation réalisée, il devait ensuite procéder à une série de tests approfondis afin de vérifier que Nmap fonctionnait correctement et répondait aux besoins du client.

> ### Deuxième sprint :
* **Lionel** : Sur ce deuxième sprint, Lionel a remplacé Souhail pour le rôle de *Product Owner*.  
Il lui a été attribuée comme tâche la finalisation de la rédaction du livrable "USER_GUIDE.md", ce qui permettra à n'importe quel utilisateur n'ayant jamais manipulé Nmap d'avoir une documentation complète sur son utilisation.  

* **Yohann** : La tâche confiée à Yohann consistait à rédiger le livrable intitulé 'INSTALL.md', qui avait pour objectif de documenter de manière précise et détaillée toutes les étapes à suivre pour l'installation du logiciel Nmap. Cette documentation devait inclure non seulement les instructions de base pour installer Nmap sur différents systèmes d'exploitation, mais également les prérequis nécessaires, les configurations spécifiques à certains environnements, ainsi que les éventuelles étapes de dépannage en cas de difficultés rencontrées lors de l'installation. Yohann devait veiller à ce que ce document soit exhaustif, clair et accessible à la fois pour des utilisateurs novices et expérimentés, afin de garantir une installation fluide et sans erreur pour toute personne souhaitant utiliser cet outil.


* **Elsa et Souhail** : La responsabilité de la rédaction du document 'README.md' a été attribuée à Elsa et Souhail dans le cadre de ce deuxième sprint. Ils auront pour mission de s'assurer que toutes les informations nécessaires sont incluses dans ce livrable, de manière à garantir une compréhension claire des aspects essentiels du projet pour l'ensemble des membres de l'équipe ainsi que pour les parties prenantes externes. Concernant le rôle de Scrum Master sur ce deuxième sprint, c'est Elsa qui l'a occupé.

--- 

### 4. Difficultés techniques rencontrés

ici

* probleme de ping entre serveur et client : ! Yohann a déjà rédigé quelque chose; à voir
* ports fermés  
*
*

---

### 5. Solutions trouvées

ici

*
*
*
---

### 6. Nmap c'est quoi

Nmap est un outil essentiel pour la reconnaissance de réseau et les audits de sécurité. Lancé en 1997, il s’est rapidement imposé comme l’un des outils de cybersécurité les plus fondamentaux et utilisés aujourd'hui. À l'origine conçu comme un scanner de ports avancé, Nmap a évolué pour devenir un outil multifonctionnel, offrant une large gamme d’applications, telles que la détection de mots de passe faibles, le scan d'adresses IPv6, la géolocalisation d'adresses IP et l’identification de vulnérabilités.

En tant qu’outil open source, Nmap est un atout précieux pour les professionnels de la sécurité, les équipes de mise en réseau, les administrateurs systèmes et d'autres spécialistes de l'informatique. Il permet d'analyser divers environnements, y compris des hôtes, des réseaux, des applications, des ordinateurs centraux, des systèmes Unix et Windows, ainsi que des systèmes de contrôle et d’acquisition de données, et des systèmes de contrôle industriel.



