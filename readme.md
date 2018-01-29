

# Je t'explique les fondamentaux de Rails en utilisant des métaphores

_J'ai décidé d'éviter le jargon et de prendre des images très simples et très parlantes pour démystifier Ruby On Rails. J'espère t'avoir aidé ! N'hésite pas à me faire savoir ce que tu en penses !_

---

### 1. La différence entre un site statique et un site dynamique

Un site statique, c'est un peu comme un tableau exposé au musée. Disons Mona Lisa. __C'est la même image pour tout le monde, tout le temps.__ Et cette image ne changera jamais : elle est figée et on veut qu'elle le reste. Un site statique s'affiche donc toujours de la même façon : quel que soit celui qui le consulte, le contenu reste le même et s'affiche de la même façon.

À l'inverse, un site dynamique c'est un peu comme regarder son reflet dans un miroir. __À chacun de nos mouvements, l'image que nous renvoie le miroir s'adapte pour être la plus fidèle possible à ce qui se passe.__ Le site dynamique renvoie donc une page très personnalisée : le contenu s'inspire de nos centres d'intérêts, de l'occurence de nos interactions avec d'autres utilisateurs, etc. Grâce à cette mémoire, la page s'adapte à l'usage que nous avons d'Internet en général.

---

### 2. Model View Controler

Monsieur Felix veut se marier. Il a besoin d'une bague avec un beau rubis. Il va voir Monsieur Charles, un bijoutier spécialisé.  Monsieur Charles comprend ce que Monsieur Felix recherche : une bague avec un rubis exceptionnel. À partir de là, il sait à qui il va adresser la demande : dans son répertoire, il a le numéro de Madame Marie, il sait que c'est la plus à même à répondre correctement aux attentes de Monsieur Felix. Une fois qu'elle a eu le coup de fil de Monsieur Charles, elle commence par se mettre en quête du rubis. Elle appelle Monsieur Fred. Monsieur Fred a l'habitude de parcourir les mines de rubis et en a plein en stock. Ils discutent en termes de pureté de la pierre. Elle lui demande de lui ramener sa pierre la plus indiquée. Une fois que Madame Marie a récupéré le rubis brute, elle s'adresse à Madame Juliette. Elle est spécialiste dans le montage de pierres sur anneaux et sur la personnalisation de cadeaux. Madame Marie lui parle de l'effet final attendu, du rafinement du bijou aux petites attentions pour bien le présenter et toucher la dulcinée de Felix. Elle polit le rubis, travaille l'anneau, monte la pierre sur l'anneau, emballe précautionneusement le bijou et l'accompagne d'un poème dédié à l'amour. Elle donne le tout à Madame Marie, qui donne le tout à Monsieur Charles, qui donne le paquet à Monsieur Felix.

Le MVC est un modèle qui permet, lorsqu'une requête est faite par un utilisateur via un navigateur web, __d'y répondre de façon adéquate.__ Chaque élément joue un rôle précis : 
* _le routeur_ (Charles) fait une première interprétation de la requête, il fait appel au contrôleur adéquat pour piloter la manoeuvre et répondre le mieux possible aux attentes de _l'utilisateur_ (Félix).
* _le contrôleur_ (Marie) sert de référent au sein de l'application Rails, il fait des requêtes au modèle (Fred) et à la vue (Juliette)
* _le modèle_ (Fred) est le référent base de données : c'est lui seul qui peut aller y chercher la donnée brute (le rubis) correspondant à la requête utilisateur
* _la vue_ (Juliette) quant à elle intègre cette donnée brute dans le template html/ css prévu à cet effet (le bijou monté, dans son paquet cadeau avec le poème) avant de renvoyer le tout au routeur (Charles), qui renvoie le résultat à l'utilisateur (Félix).

___

### 3. Les routes

Imaginons les routes comme une sorte de carte ou de GPS. En fonction de la destination que l'on veut atteindre, __la carte nous indique la marche à suivre pour nous y rendre.__ Les routes, dans le cas de Rails, jouent exactement le même rôle : elles renseignent la procédure complète pour réussir les actions.

___

### 4. Les Bases de Données

Une base de données, c'est un peu comme __une grande bibliothèque__ où sont stockés de nombreux ouvrages de types différents (encyclopédies, romans, essais, manuels, etc.) et de disciplines différentes (développement informatique, langues, mathématiques, sciences humaines et sociales, etc.). Lorsque nous avons besoin d'une information, nous pouvons aller chercher le livre le plus pertinent pour nous aider à la retrouver. La recherche est facilitée par les règles qui permettent de ranger correctement les livres : par auteur, par discipline, par collection etc. Ces clés nous font gagner du temps. On peut consulter les livres que la bibliothèque a en stock, mais on peut également en ajouter pour la compléter.

___ 

### 5. GET / POST

Reprenons l'image utilisée précédemment pour parler des bases de données, c'est-à-dire notre bibliothèque. GET, c'est la requête que nous faisons au/ à la bibliothécaire __lorsque nous voulons emprunter un livre.__ Cela lui permet d'aller nous chercher le précieux grimmoire dans la tonne d'autres grimoires. 

À l'inverse, POST, c'est la requête qui nous permet de dire au bibliothécaire que nous avons retrouvé dans notre cave ce livre obscure qui nous semble tout de même intéressant pour les personnes qui fréquentent sa bibliothèque. Nous lui indiquons que nous souhaitons participer à la diffusion des savoirs __en faisant don du livre à la bibliothèque.__ Le livre se retrouve désormais stocké avec les autres dans la bibliothèque. 

___

### 6. Le concept de migration

Continuons avec la métaphore de la bibliothèque. Imaginons que l'on veut ajouter un rayon sur la méditation car les développeurs sont trop stressés par les bugs. Ce rayon n'existait pas auparavant dans notre bibliothèque. On ne rajoute pas un rayon à une bibliothèque en un claquement de doigts. On prend des précautions, on prépare l'intégration en indiquant le nom du nouveau rayon, ce que l'on veut y trouver, comment s'y repérer, etc. Et une fois qu'on est prêt, qu'on est sûr qu'on ne va perdre aucun livre, on lance l'ajout du rayon. La migration c'est cela. Lorsque l'on __manipule la structure de notre base de données__ pour y ajouter ou en supprimer des informations, on effectue une migration.

___

### 7. Les relations entre les models des BDD

___

### 8. Les fonctions du CRUD

Les fonctions CRUD, c'est-à-dire un gros mot pour dire Create Read Update Delete, est une forme de __cycle de vie d'un objet dans une application Rails.__ Ce cycle de vie correspond à toutes les actions possibles sur cet objet. Pour rendre ces actions possibles, nous avons besoin de définir des manières de procéder pour chaque cas :

* _La création_, soit la naissance de l'objet : on va définir la marche à suivre pour donner naissance à un objet.
* La consultation, c'est notre capacité à mobiliser l'objet en cas de besoin pour accéder aux informations qu'il contient : on décide comment il faut s'y prendre. C'est un peu comme quand tes parents t'appellent pour débugger leur ordinateur.
* _La modification, la mise à jour_ nous permet de nous assurer que les informations disponibles dans l'objet sont toujours pertinentes. Un peu comme quelqu'un qui se forme en continue, qui actualise ses savoirs, même/ surtout une fois sorti de l'école.
* _La supression, l'effacement_ est la destination finale, lorsque l'objet n'a plus de raison d'être, on doit pouvoir l'effacer. Un peu comme lorsque quelqu'un finit par céder sa place sur Terre.

Suivre ce schéma, c'est s'assurer que l'on crée des objets avec lesquels on pourra interagir pleinement.