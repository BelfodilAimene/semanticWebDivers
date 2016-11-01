Guide TP
========

### Etape 1 - Récupérer quelques URLs de Google Search
Pour cela nous avons fournis le petit script **querygoogle.sh** qui permet de récupérer les **URLs** retournés par **Google Sreach** en réponse d'une requête **Query**.

Vous pouvez utiliser pour cela le script [queryGoogle.sh](./queryGoogle.sh). Par exemple, la requête ```QUERY=michelle+obama OFFSET=10 ./queryGoogle.sh``` va donner une disaine d'**URLs** liées à la recherche **"michelle+obama"** à partir du **11ème** résultat selon le classement de **Google**.

### Etape 2 - Faire un déréférencement pour chaque URL Obtenu
Pour cela il suffit de récupérer le text contenu dans la page de l'**URL** en question. Nous fournissons deux manières de faire : 
 - **En utilisant la commande sed :** Pour cela vous pouvez utiliser le petit script améliorable [dereferenceURL.sh](./dereferenceURL.sh). Par exemple, pour faire le déréférencement de la page [https://www.whitehouse.gov/administration/first-lady-michelle-obama](https://www.whitehouse.gov/administration/first-lady-michelle-obama) on utilise ```URL=https://www.whitehouse.gov/administration/first-lady-michelle-obama ./dereferenceURL.sh```.
 - **En utilisant l'API Alchemy :** Une autre manière de faire est d'utiliser l'[API Alchemy](http://www.ibm.com/watson/developercloud/alchemy-language/api/v1/#text_cleaned) mais vous devez avoir une **apikey** de [http://www.alchemyapi.com/api/register.html](http://www.alchemyapi.com/api/register.html). Le petit script [dereferenceURLAlchemy.sh](./dereferenceURLAlchemy.sh) peut être utilisé de la manière suivante : ```APIKEY=your_api_key URL=https://www.whitehouse.gov/administration/first-lady-michelle-obama ./dereferenceURLAlchemy.sh```.

### Etape 3 - Récupérer les URI des entités DBpedia existantes dans le text

### Etape 4 - Explorer le graphe DBPedia à partir des URI obtenus
 
