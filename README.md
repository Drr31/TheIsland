# TheIsland
Projet Approche Orientée Objet – IATIC 3 – 2021/2022
rojet Approche Orientée Objet – IATIC 3 – 2021/2022 The Island
Dhekra ABOUDA (dhekra.abouda@gmail.com)
L'objectif de ce projet est de réaliser une version informatique du jeu de société The Island.
Ce sujet décrit les fonctionnalités attendues du jeu qui a été adapté pour le projet. Quand ce n'est pas explicitement imposé par l'énoncé, vous avez toute latitude de décider du choix le plus pertinent pour votre implémentation.
1Lejeu
Vous dirigez de valeureux explorateurs en mission sur une île dangereuse dissimulant de fabuleux trésors. Mais un volcan autrefois éteint a décidé de donner de la voix ! la terre se met à trembler et l’île s’enfonce dans la mer. Vous devez sauver un maximum de vos aventuriers pour remporter la partie.
1.1 Plateau de jeu
Le jeu se déroule sur un espace de jeu découpé en cases hexagonales. Un hexagone représente l'unité de lieu et est d'un certain type (plage, forêt, montagne, mer).
Le plateau initial (voir la figure 1) représente 4 plages (dans les 4 coins du plateau) et la mer au centre. 5 pions serpent de mer sont placés sur les cases du plateau dotées du symbole Serpent de mer.
Notez la présence d’une délimitation (certaines cases de mer sont entourées d’un trait noir plus épais) pour poser les tuiles (explication dans les prochains chapitres).
Figure 1 _ Plateau initial
1.2 Unités
- 1 plateau de jeu
- 40 tuiles de terrain : 16 tuiles Plage, 16 tuiles Forêt et 8 tuiles Montagne. Chaque tuile à une face
cachée comme suit :
 
   - 40 pions explorateur : 10 de chaque couleur (rouge, bleu, vert et jaune). Sous chaque pion explorateur figure un chiffre (pour chacune des séries les pions portent les numéro 1,1,1,2,2,3,3,4,5,6) :
-
- 5 pions Serpent de Mer, 6 pions Requin, 5 pions Baleine :
  
- 12 pions Bateau
- 1 dé de créature :
1.3 Préparation de la partie :
Toutes les tuiles terrain sont mélangées, et placées au hasard sur les cases de la mer entourées de noir, afin de former l’île. Chaque joueur récupère les pions de sa couleur et reçoit deux pions bateau (les autres bateaux, les pions requin & baleine sont mis de côté pour l’instant).
Il ne reste plus qu’à choisir le premier joueur et à mémoriser les nombres de 1 à 6 inscrits sous les pions explorateurs de chaque joueur. La valeur est importante puisque c’est elle qui vous dira le nombre de trésors transportés par l’explorateur. Chaque joueur, l’un après l’autre, place un pion explorateur sur une tuile de terrain déserte jusqu’à ce que ses 10 pions soient placés. Puis, on refait la même chose avec les pions bateaux qui seront placés sur des cases de mer inoccupées mais voisine d’une tuile terrain.
Les pions ne pourront plus être regardés par la suite, d’où l’intérêt de bien mémoriser les chiffres qui sont dessous.
  1.4 déroulement de la partie :
Les joueurs vont maintenant jouer chacun leur tour dans le sens des aiguilles d’une montre. Lors de votre tour de jeu, vous devez accomplir ces actions dans l’ordre :
– Jouer une tuile terrain de sa main : Si un joueur a obtenu une tuile terrain lors d’un précédent tour, et s’il le veut, il peut la jouer
– Déplacer les pions explorateur et/ou bateau : Il est possible de déplacer n’importe quel pion explorateur et/ou bateau. Mais vous n’avez que 3 cases de déplacement possibles. Donc soit 3 déplacements avec un seul pion, soit 2 déplacements avec l’un et 1 déplacement avec l’autre... Le but est que vos explorateurs rejoignent les bateaux pour les emmener sur une île proche.
– Retirer une tuile de terrain : le joueur doit retirer une tuile de terrain. Si un explorateur se trouvait dessus, il devient nageur. Le joueur peut regarder le verso de la tuile sans la montrer aux autres joueurs. Pour retirer une tuile, il faut qu’elle soit adjacente à une case de mer, mais il faut qu’elles soient enlevées dans un ordre précis : d’abord les tuiles plage, puis forêt et enfin montagne.
– Lancer le dé et déplacer une créature : le joueur lance le dé et déplace d’une ou plusieurs cases de mer un serpent de mer, une baleine ou un requin (selon le résultat du dé) à condition qu’une telle créature soit déjà sur le plateau. Utile pour aller attaquer un autre joueur ou protéger ses propres explorateurs. Chaque créature a ses propres caractéristiques et peut donc attaquer ou non !

Pour le déplacement des pions, il est possible de déplacer un explorateur sur terre du moment qu’il arrive sur une case adjacente ou sur un bateau. Mais attention, il ne faut pas plus de 3 personnes par bateau.
Une fois que l’explorateur a quitté l’île, il ne peut plus retourner sur le terrain.
Pour les explorateurs dans l’eau, ils deviennent nageurs lorsqu’ils sautent du bateau, lorsqu’ils tombent sur une case de mer, lorsqu’ils quittent l’île sans bateau, ou lorsqu’une baleine fait chavirer le bateau. Un nageur ne peut être déplacé que d’une seule case. Forcément, un nageur qui tombe sur un serpent de mer ou un requin est tout de suite retiré du jeu.
Pour les bateaux, lorsqu’il est vide, il peut être déplacé par n’importe quel joueur. Chaque bateau ne peut contenir que 3 explorateurs (peu importe la couleur des pions), mais si plusieurs sont dessus c’est le joueur majoritaire qui le contrôle. Quand plusieurs joueurs ont le même nombre d’explorateurs dans un bateau, chaque joueur contrôle le bateau.
Pour mettre à l’abri ses explorateurs il faut les débarquer sur une île proche, et le déplacement du bateau à l’île coûte un déplacement.
Les tuiles terrain retirées vous permettent de réaliser des actions immédiates, à jouer en début de tour ou en défense ! Par exemple, vous pourrez faire intégrer un requin ou une baleine, retirer du jeu tous les occupants de la tuile enlevée et de ses alentours, avoir l’aide d’un dauphin ou du vent, retirer un requin avant qu’il n’attaque votre nageur ...
(Plus d’explications dans la suite de l’énoncé)
Sous l’une des tuiles montagne, il y a un volcan ! Lorsque cette tuile est révélée, l’éruption volcanique détruit tout ce qu’il reste de l’île ainsi que les explorateurs encore en mer. On annonce la fin de la partie ! On retourne alors tous les pions explorateurs qui sont en lieu sûr, pour dévoiler les fameux chiffres mémorisés en début de partie. Une fois le total fait, c’est l’heure de faire les comptes. Celui qui a le plus de points gagne la partie et devient le meilleur explorateur !
1.5 Le résultat du dé
Les serpents de mer, les requins et les baleines n’ont aucun effet les uns sur les autres. Ils peuvent occuper la même case de mer. Si la créature en question n’es pas encore présente sur le jeu, il ne se passe rien.
- Serpent de mer : si le résultat du jet de dé est un serpent de mer, vous pouvez déplacer l’une de ces créatures d’une case de mer. Si le serpent de mer arrive dans une case de mer occupée par un bateau contenant des passagers, retirez celui-ci et ses occupants du jeu. Retirez également tous les nageurs occupant la case de mer. S’il s’agit d’un bateau vide, il reste en place.
- Requin : si le résultat du jet de dé est un requin, vous pouvez déplacer l’une de ces créatures d’une ou deux cases de mer. Si le requin entre sur une case de mer occupée par un ou plusieurs nageurs, le mouvement du requin s’achève. Retirez tous les nageurs de la case de mer ou le requin s’est arrêté. Si la case où il se trouve contient un bateau, le requin ne l’affecte pas
- Baleine : si le résultat du jet de dé est une baleine, vous pouvez déplacer l’une de ces créatures d’une à trois cases de mer. Si la baleine entre sur une case de mer occupée par un bateau contenant un ou plusieurs passagers, son mouvement s‘achève : le bateau est retiré du jeu et ses occupants deviennent des nageurs. Si la case de mer contient également un requin, les nageurs sont retirés du jeu. Une baleine n’affecte ni les nageurs, ni les bateau vide situés dans la même case de mer qu’elle.
1.6 Les explorateurs sur terre :
Vous pouvez déplacer un pion explorateur depuis une tuile de terrain vers une tuile de terrain adjacente, même si cette dernière est déjà occupée par un ou plusieurs pions.
Vous pouvez déplacer un pion explorateur depuis une tuile de terrain vers un bateau placé sur une case de mer adjacente.
Vous pouvez déplacer un pion explorateur depuis un bateau vers un autre bateau placé sur une case de mer adjacente.
Vous pouvez déplacer un pion explorateur dans un bateau déjà occupé par des explorateurs d’une autre couleur (pas plus de 3 personnes par bateau)
Vous ne pouvez pas déplacer les explorateurs d’un autre joueur

1.7 Les explorateurs dans l’eau :
Les pions explorateurs deviennent des nageurs lorsqu’ils se déplacent dans une case mer à partir d’une tuile de terrain adjacente, quand ils sautent d’un bateau dans la case de mer où il se trouve, quand ils tombent dans une case de mer lorsqu’une tuile de terrain est retirée, ou quand une baleine chavire leur bateau et les fait tomber dans la case de mer qu’il occupait.
Vous ne pouvez déplacer un nageur que d’une case de mer à votre tour. Lorsqu’un nageur passe d’une tuile de terrain ou d’un bateau à une case de mer, ceci est considéré comme un déplacement d’une case de mer.
Vous ne pouvez déplacer un nageur sur un bateau que s’ils occupent tous deux la même case de mer. Une case de mer peut accueillir plusieurs nageurs.
1.8 Utiliser les informations d’une tuile de terrain
Les tuiles à jouer immédiatement (contour vert) :
Les tuiles à jouer au début de votre tour (contour rouge) :
       Prenez un pion requin mis de côté et placez sur la case de mer qu’occupait la tuile de terrain. Tout nageur occupant cette case de mer est retiré du jeu
       Prenez un pion baleine mis de côté et placez-le sur la case de mer qu’occupait la tuile de terrain
     Prenez un pion bateau mis de côté et placez-le sur la case de mer qu’occupait la tuile de terrain. Si cette case de mer contenait un ou plusieurs nageurs, placez-les à bord du bateau. Si la case de mer contenait plus de trois nageurs, c’est le joueur ayant révélé la tuile de terrain qui choisit lesquels montent à bord
      Tourbillon : retirez du jeu tous les nageurs, serpents de mer, requins, baleines, bateaux et explorateurs de la case de mer qu’occupait la tuile de terrain et de toutes les cases mer adjacentes.
       Eruption volcanique : Fin du jeu
         Un dauphin vient en aide à l’un de vos nageurs. Déplacez un de vos nageurs de 1 à 3 cases de mer.
    Les vents vous sont favorables. Déplacez un des bateaux que vous contrôlez de 1 à 3 cases de mer.
 
      Déplacez le serpent de mer de votre choix déjà présent sur le plateau de jeu sur n’importe quelle case de mer inoccupée
       Déplacez le requin de votre choix déjà présent sur le plateau de jeu sur n’importe quelle case de mer inoccupée.
      Déplacez la baleine de votre choix déjà présente sur le plateau de jeu sur n’importe quelle case de mer inoccupée
 Les tuiles à jouer en dehors de votre tour (en défense) (contour rouge) :
1.9Findujeu:
Dès que le volcan apparaît, il engloutit tous les personnages qui n'ont pas été sauvés. Chaque joueur récupère alors ses explorateurs ayant atteint une île pour dévoiler et additionner la valeur de leur trésor. Le joueur doté du plus gros butin remporte la partie. En cas d'égalité, le joueur ayant sauvé le plus d'explorateurs est désigné vainqueur.
2 Le projet
Ce projet va donc consister à proposer une version du jeu jouable sur ordinateur.
2.1 Jeu multi-joueurs
Le jeu doit permettre de jouer à plusieurs joueurs humains, ces derniers joueront leur tour l'un après l'autre. Le programme fonctionnera sur une seule machine (pas en réseau).
       Quand un autre joueur déplace un requin dans une case de mer occupée par l’un de vos nageurs, vous pouvez jouer cette tuile de terrain pour retirer le requin du jeu. Tous les nageurs demeurent dans la case mer.
     Quand un autre joueur déplace une baleine dans une case de mer occupée par un bateau que vous contrôlez, vous pouvez jouer cette tuile de terrain pour retirer la baleine du jeu. Votre bateau demeure dans la case de mer.
 
2.2 Interface utilisateur
Peu de choses sont imposées au niveau de l'interface graphique. Néanmoins, un soin particulier devra être apporté à sa clarté et à son ergonomie. Une aide devra être proposée au joueur débutant pour l'aider à assimiler les règles du jeu lors de ses premières parties. La forme que prendra cette aide n'est pas imposée.
Le programme aura également pour rôle de vérifier les actions des joueurs humains. Seules les actions valides seront possibles.
2.3 Contraintes techniques
Le projet sera réalisé en langage Java. Les fonctionnalités disponibles dans le langage (collections, exceptions,) devront être utilisées au mieux. L'interface graphique utilisera la bibliothèque Swing. L'utilisation de bibliothèques tierce est autorisée (Google Guava, . . .). Le code source devra respecter les conventions de codage de SUN. La documentation du code sera conforme à l'outil standard javadoc. Le projet final devra fonctionner et se compiler en dehors de tout IDE (avec l'outil Maven par exemple). Idéalement, le projet sera fourni sous la forme d'une archive au format jar et « exécutable ».
3 Organisation et évaluation
Ce projet est à réaliser par groupe de 5 en moyenne avec au moins une fille par groupe.
Trois supports seront à rendre sous forme électronique par mail :
Support de soutenance Il présentera d’une façon macro votre travail en termes de répartition des tâches, organisation du travail, outils de travail, problèmes rencontrés et solutions trouvées.
Code source le code entier avec un exécutable permettant de lancer le jeu sans passer par un éditeur
Rapport final Il décrira l'implémentation du programme : il comprendra une description de l'implémentation, un manuel de l'utilisateur (avec captures d'écran), le planning et la répartition des tâches, ...
Les règles de nommage suivantes sont à respecter pour chaque échange :
- Le Titre du mail : Projet_POO_GoupeX
- Les pièces jointes : GroupeX_ Description (ex : GroupeX_Rapport_Final)
Le barème final prend en compte le respect des règles de nommage et des délais d’envoi des documents. Des points seront retirés en cas de non-respect.
La liste des groupes doit être partagée au plus tard le 22 Avril 2022 par le délégué de la classe.
4 Dates importantes
- 12 Avril 2022 : Lancement du projet
- 23 Mai 2022 : Remise du rapport final, du code source du projet, des binaires et du support de la
présentation
- 25 Mai 2022 : soutenances
