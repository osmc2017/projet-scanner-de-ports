# **DOCUMENTATION UTILISATEUR**

## **SOMMAIRE**

### :one: [Utilisation basique (Ubuntu)](https://github.com/WildCodeSchool/TSSR-2409-P1-G3-Scanner-de-ports/blob/main/USER_GUIDE.md#one-utilisation-basique-ubuntu-1)

### :two: [Utilisation avancée](https://github.com/WildCodeSchool/TSSR-2409-P1-G3-Scanner-de-ports/blob/main/USER_GUIDE.md#two--utilisation-avanc%C3%A9e-certaines-commandes-peuvent-n%C3%A9cessiter-dutiliser-sudo)
    
### :three: [Exemple et interprétation du résultat](https://github.com/WildCodeSchool/TSSR-2409-P1-G3-Scanner-de-ports/blob/main/USER_GUIDE.md#three--exemple-et-interpr%C3%A9tation-du-r%C3%A9sultat)

### :four:  [Scan personnalisé avec NSE](https://github.com/WildCodeSchool/TSSR-2409-P1-G3-Scanner-de-ports/blob/main/USER_GUIDE.md#four--scan-avanc%C3%A9-avec-nse)

---

### :one: Utilisation basique (Ubuntu)

Ces commandes fondamentales vous permettront de réaliser des scans initiaux, d'identifier les ports ouverts et de découvrir les services qui s'exécutent sur eux. Vous trouverez également les commandes donnant accés au manuel et à l'aide de Nmap.

#### - Accés aide et Manuel:
  * Manuel d'utilisation:
    
>    ` man nmap `
  * Aide pour les options:
    
>   `nmap --help`

#### - Commandes de base:

* Scan des 1000 ports les plus utilisés de l'ip cible

> `nmap [adresse ip cible]`

* Scan des ports d'un sous réseau

> `nmap [adresse ip cible]/24`

* Scan des 100 ports les plus utilisés de l'ip cible

> `nmap -F [adresse ip cible]`

* Scan de tous les ports les plus utilisés de l'ip cible

> `nmap -P 1-65535 [adresse ip cible]`

* Scan d'un seul port

> `nmap -P {port} [adresse ip cible]`

---

### :two:  Utilisation avancée: certaines commandes peuvent nécessiter d'utiliser `sudo`

Nmap offre également la possibilité d'obtenir des informations approfondies sur les dispositifs connectés. Ci-dessous, vous trouverez quelques exemples de commandes qui permettent de réaliser une analyse plus pointue d'un hôte

* Scan de Détection d'OS: tente d'identifier l'OS de l'hôte
  
>`nmap -O [adresse ip cible]`

* Scan agressif: scan complet incluant la détection des services, des versions et des systèmes

> `nmap -A [adresse ip cible]`

* Scan TCP connect: Etablit une connexion complète avec le port

> `nmap sT [adresse ip cible]`

* Scan tous les ports UDP

> `nmap -sU [adresse ip cible]`

---

### :three:  Exemple et interprétation du résultat

> ![capture cmd basique](https://github.com/WildCodeSchool/TSSR-2409-P1-G3-Scanner-de-ports/blob/8a152d6a65d29c57d7f1cd25c362bfda508c19d1/capture/Capture%20d'%C3%A9cran%202024-10-16%20123035.png)

- **Ligne 1** : Sur la ligne 1, nous voyons que l'utilisateur "wilder", depuis le client CLILIN01, lance une commande `nmap` vers un serveur ayant pour adresse IP `[172.16.10.10]`.
- **Ligne 2** : La ligne 2 indique le lancement du logiciel nmap, en précisant l'heure et la date.
- **Ligne 3** : Ici, il est annoncé que nous allons recevoir un rapport de scan des ports de l'adresse IP scannée.
- **Ligne 4** : Cette ligne fournit des informations concernant le délai de réponse du serveur (latence).
- **Ligne 5** : Cette ligne indique le nombre de ports fermés.
- **Lignes 6 à 10** : Ici, nous avons le détail des ports ouverts et des services associés à chacun d'eux.
- **Ligne 12** : Enfin, cette ligne nous informe que l'hôte a bien été scanné en 5,03 secondes.

---

### :four:  Scan avancé avec NSE 

Il est possible de rendre Nmap plus flexible et efficace en utilisant le moteur de script de Nmap (Nmap Scripting Engine - NSE). Effectivement, le NSE allie l'efficacité de Nmap dans le traitement du réseau à la souplesse d'un langage léger comme Lua, offrant ainsi une infinité d'opportunités. Nmap dispose d'environ 5000 scripts, consultable en suivant le chemin `/usr/share/nmap/scripts`:

> ![capture script](https://github.com/WildCodeSchool/TSSR-2409-P1-G3-Scanner-de-ports/blob/e238f0d65ec4ae3680aec890ae0ff8ef4e5ea9bf/capture/liste%20script.png)


Le but du NSE est de fournir à Nmap une infrastructure flexible pour étendre ses capacités et offrir à ses utilisateurs une manière simple de créer leurs propres tests personnalisés. Le cadre d'usage du NSE englobe (mais n'est pas limité à) :

* La détection de version évolué;
* La détection de Malware;
* La découverte du réseau et la collecte d'informations,...

Pour faciliter le choix des scripts et refléter leurs différents usages, chaque script est associé à une ou plusieurs catégories. Pour maintenir cette association, un fichier nommé `script.db` est inclus avec les scripts distribués. Par exemple, si vous souhaitez vérifier si une machine est infectée par un malware, Nmap vous fournit un script que vous pouvez utiliser avec la commande `nmap --script=malware ip-cible` pour analyser les résultats ultérieurement.

- **Exemple de scan du port de serveur DHCP avec utilisation d'un NSE:**

> ![capture commande avec script](https://github.com/WildCodeSchool/TSSR-2409-P1-G3-Scanner-de-ports/blob/8e8bda68cd305d254ca48e75d36ac4dda22c7865/capture/scan%20avec%20script.png)
  
- **Ligne 1** : Sur la première ligne, nous observons que l'utilisateur "wilder", à partir du client CLILIN01, exécute une commande `nmap` en visant un serveur dont l'adresse IP est `[172.16.10.10]`, tout en initiant le script `dhcp-discover`.
- **Ligne 2** : La seconde ligne indique le démarrage du logiciel `nmap`, en précisant l'heure et la date de l'exécution.
- **Ligne 3** : Ici, il est annoncé que nous allons recevoir un rapport détaillé sur le scan des ports de l'adresse IP ciblée.
- **Ligne 4** : Cette ligne fournit des informations sur le délai de réponse du serveur, également connu sous le nom de latence.
- **Lignes 5 et 6** : Nous y trouvons l'état des ports scannés, ainsi que les services qui y sont associés.
- **Ligne 7** : Cette ligne révèle que nous avons effectué une analyse approfondie de la machine hôte, incluant l'adresse MAC et le nom du périphérique réseau.
- **Ligne 8** : Enfin, cette ligne confirme que le scan de l'hôte a été réalisé en 5,54 secondes.


Une documentation plus complète du NSE (y compris ses API) est disponible sur le site de [Nmap](https://nmap.org/man/fr/man-nse.html).








