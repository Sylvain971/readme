

#Je t'explique les fondamentaux de Rails en utilisant des métaphores

_J'ai décidé d'éviter le jargon et de prendre des images très simples et très parlantes pour démystifier ruby. J'espère t'avoir aidé ! N'hésite pas à me faire savoir ce que tu en penses_

---

###1. La différence entre un site statique et un site dynamique

Un site statique, c'est un peu comme un tableau exposé au musée. Disons Mona Lisa. C'est la même image pour tout le monde, tout le temps. Et cette image ne changera jamais : elle est figée et on veut qu'elle le reste. Un site statique s'affiche donc toujours de la même façon : quel que soit celui qui le consulte, le contenu reste le même et s'affiche de la même façon.

À l'inverse, un site dynamique c'est un peu comme regarder son reflet dans un miroir. À chacun de nos mouvements, l'image que nous renvoie le miroir s'adapte pour être la plus fidèle possible à ce qui se passe. Le site dynamique renvoie donc une page très personnalisée : le contenu s'inspire ducorrespond aux informations liées à nos navigations passées pur, mais également yer une page adaptée à nos centres d'intérêt, à nos demandes et à nos interactions. Le site peut avoir une mémoire : il peut se rappeler que nous sommes avons recherché plusieurs fois une information

---

###2. Model View Controler

Monsieur Felix veut se marier. Il a besoin d'une bague avec un beau rubis. Il va voir Monsieur Charles, un bijoutier spécialisé.  Monsieur Charles comprend ce que Monsieur Felix recherche : une bague avec un rubis exceptionnel. À partir de là, il sait à qui il va adresser la demande : dans son répertoire, il a le numéro de Madame Marie, il sait que c'est la plus à même à répondre correctement aux attentes de Monsieur Felix. Une fois qu'elle a eu le coup de fil de Monsieur Charles, elle commence par se mettre en quête du rubis. Elle appelle Monsieur Fred. Monsieur Fred a l'habitude de parcourir les mines de rubis et en a plein en stock. Ils discutent en termes de pureté de la pierre. Elle lui demande de lui ramener sa pierre la plus indiquée. Une fois que Madame Marie a récupéré le rubis brute, elle s'adresse à Madame Juliette. Elle est spécialiste dans le montage de pierres sur anneaux et sur la personnalisation de cadeaux. Madame Marie lui parle de l'effet final attendu, du rafinement du bijou aux petites attentions pour bien le présenter et toucher la dulcinée de Felix. Elle polit le rubis, travaille l'anneau, monte la pierre sur l'anneau, emballe précautionneusement le bijou et l'accompagne d'un poème dédié à l'amour. Elle donne le tout à Madame Marie, qui donne le tout à Monsieur Charles, qui donne le paquet à Monsieur Felix.

Le MVC est un modèle qui permet, lorsqu'une requête est faite par un utilisateur via un navigateur web, d'y répondre de façon adéquate. Chaque élément joue un rôle précis : 
*le routeur (Charles) fait une première interprétation de la requête, il fait appel au contrôleur la page et la procédure associée les plus pertinents à ses yeux pour répondre aux attentes de l'utilisateur (Félix).
*le contrôleur (Marie) sert de référent au sein de l'application rails, il fait des requêtes au modèle (Fred) et à la vue (Juliette)
*le modèle (Fred) est le référent base de données : c'est lui seul qui peut aller y chercher la donnée brute correspondante (le rubis)
*la vue (Juliette) quant à elle intègre cette donnée brute dans le template html/ css prévu à cet effet (le bijou monté, dans son paquet cadeau avec le poème) avant de renvoyer le tout au routeur (Charles), qui renvoie le résultat à l'utilisateur (Félix).

___

###3. Les routes

Imaginons les routes comme une sorte de carte ou de GPS. En fonction de la destination que l'on veut atteindre, la carte nous indique la marche à suivre pour nous y rendre. Les routes, dans le cas de Rails, jouent exactement le même rôle : elles renseignent la procédure complète pour réussir les actions.

___

###4. Les Bases de Données

Une base de données, c'est un peu comme une grande bibliothèque où sont stockés de nombreux ouvrages de types différents (encyclopédies, romans, essais, manuels, etc.) et de disciplines différentes (développement informatique, langues, mathématiques, sciences humaines et sociales, etc.). Lorsque nous avons besoin d'une information, nous pouvons aller chercher le livre le plus pertinent pour nous aider à la retrouver. La recherche est facilitée par les règles qui permettent de ranger correctement les livres : par auteur, par discipline, par collection etc. Ces clés nous font gagner du temps. On peut consulter les livres que la bibliothèque a en stock, mais on peut également en ajouter pour la compléter.

___ 

###5. GET / POST

Reprenons l'image utilisée précédemment pour parler des bases de données, c'est-à-dire notre bibliothèque. GET, c'est la requête que nous faisons au/ à la bibliothécaire lorsque nous voulons emprunter un livre. Cela lui permet d'aller nous chercher le précieux grimmoire dans la tonne d'autres grimoires. 

À l'inverse, POST, c'est la requête qui nous permet de dire au bibliothécaire que nous avons retrouvé dans notre cave ce livre obscure qui nous semble tout de même intéressant pour les personnes qui fréquentent sa bibliothèque. Nous lui indiquons que nous souhaitons participer à la diffusion des savoirs en faisant don du livre à la bibliothèque. Le livre se retrouve désormais stocké avec les autres dans la bibliothèque. 

___

###6. Le concept de migration

Continuons avec la métaphore de la bibliothèque. Imaginons que l'on veut ajouter un rayon sur la méditation car les développeurs sont trop stressés par les bugs. Ce rayon n'existait pas auparavant dans notre bibliothèque. On ne rajoute pas un rayon à une bibliothèque en un claquement de doigts. On prend des précautions, on prépare l'intégration en indiquant le nom du nouveau rayon, ce que l'on veut y trouver, comment s'y repérer, etc. Et une fois qu'on est prêt, qu'on est sûr qu'on ne va perdre aucun livre, on lance l'ajout du rayon. La migration c'est cela. Lorsque l'on manipule la structure de notre base de données pour y ajouter ou en supprimer des informations, on effectue une migration.

___

###7. Les relations entre les models des BDD

___

###8. Les fonctions du CRUD

Les fonctions CRUD, c'est-à-dire un gros mot pour dire Create Read Update Delete, c'est une forme de cycle de vie d'un objet dans une application Rails. Ce cycle de vie correspond à toutes les actions possibles sur cet objet. Pour rendre ces actions possibles, nous avons besoin de définir des manières de procéder pour chaque cas :

* La création, c'est un comme une naissance, on crée quelque chose à partir de rien. On va donc définir des procédés pour donner naissance à un objet.
* La consultation, c'est notre capacité à mobiliser l'objet en cas de besoin, pour accéder aux informations qu'il contient.
* La modification, la mise à jour nous permet de nous assurer que les informations disponibles dans l'objet sont toujours pertinentes. Un peu comme quelqu'un qui se forme en continue, qui actualise ses savoirs.
* La supression, l'effacement est la destination finale, lorque l'objet n'a plus de raison d'être, on doit pouvoir l'effacer. Un peu comme lorsque quelqu'un finit par céder sa place sur Terre.

Suivre ce schéma, c'est s'assurer que l'on crée des objets avec lesquels on pourra interagir pleinement.