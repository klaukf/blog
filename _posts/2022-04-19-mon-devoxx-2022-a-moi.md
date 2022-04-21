---
layout: post
title:  "Mon Devoxx 2022 à moi !"
author: fanny
categories: [ event ]
tags: [ devoxx ]
image: assets/images/devoxxFR2.png
---

*ENFIN !! je crois que c'est le mot qui résume le plus l'attente (3 ans quand même !), les retrouvailles, les allers et venues dans les couloirs Neuilly et Paris, l'arrêt aux stands, les discussions avec les copains et les copines... Que ça fait du bien !
Retour en images et en texte de cette spéciale 10 ans de DevoxxFR...

## Mardi 19 avril : prépa physique et mentale

Cela fait deux jours que le stress gagne chacun de mes organes vitaux et m'empêche de correctement dormir et manger.
Il y a quelques jours j'apprends que je donnerai ma conférence "Rendez l'agilité aux développeurs et développeuses !" en amphi bleu. Le grand amphi cleu. L'ENORME amphi bleu. Il n'y a plus qu'à espérer que les spots m'aveuglent suffisamment pour que je n'y voie rien !

Après un faux départ (oubli de chargeur de portable, c'eut été dommage...), en route pour Paris depuis Saint Pierre des Corps (à 4km de Tours 😜).

On retrouve les potos pour partager un repas sympathique et on oublie la pression, car commme dirait un grand homme, qui vit avec moi : "La pression ça se boit !"

## Mercredi 20 avril : tranquille !

### Ce que l'on retrouve

Par rapport aux autres éditions, il y a beaucoup de choses qui n'ont pas changé et qu'on aime retrouver (d'ailleurs, on vient surtout pour ça !) : les gilets rouges qui assurent, les "oh tiens tu es là toi ? ça va ? la famille ? imotep !", 

Il y a aussi la partie stand que j'affectionne particulièrement : il y a trois ans, lors de l'édition 2019, je cherchais, l'âme en peine, une solution à mon avenir professionnel. CV à la main, j'avais fureté sur les stands et énormément échangé sur la vision des équipes de dev alors. C'est là que l'arrivée de 10 techs en sweat Apside m'avait tapée dans l'oeil. Une année chargée d'émotions donc, qui me fera toujours aimer échanger avec les boîtes présentes.

### Ce qui change

Non mais vous avez vu ce stand d'accueil ?? Cette bannière magistrale, cette organisation impeccable, ces gilets rouges au top !
![Le site d'accueil pour retirer les pass]({{ site.url }}{{ site.baseurl }}/assets/images/devoxxFR.png)
C'est un bonheur de venir retirer son pass la veille !

Bien-sûr, n'ayant pas eu la chance de pouvoir participer à la session 9 3/4 , c'est ma première aventure Devoxx masquée. L'année prochaine je viens avec un loup ! (le masque, pas l'animal, ça ne serait pas très pratique...)

Les couloirs sont jonchés de photos souvenirs des années précédentes, depuis 2012 : je peux vous dire que personne n'a pris une ride !

### La révolution (wasm) est incroyable parce que vraie - Philippe CHARRIERE et Laurent DOGUIN

![Laurent et Philippe sont prêts]({{ site.url }}{{ site.baseurl }}/assets/images/wasm4.png)

Première université de 3h pour ce mercredi matin.
Ce que j'apprécie avec ces deux grands messieurs, c'est que ce sont des gens intelligents qui ne vous font pas sentir bêtes (merci à eux !) : je comprends quand ils m'expliquent quelque-chose 😁

Ca parle Flash, ActiveX, applets Java, bref, ça ravive des souvenirs lointains.
On arrive au Javascript mais en termes de design et de graphisme, c'est à parfaire => qu'est-ce qui peut nous sauver ?
EMScripten avec asm.js ? joli essai.
WebAssembly !! le fameux wasm : on va régler les soucis des navigateurs, sans remplacer javascript pour autant, ne confondons pas !
Il s'utilise partout, y compris sur JVM.

Wasm s'exécute partout : Javascript (navigatueur et Node.js) GraalVM, runtimes...
et parle toutes les langues : C/C++, Rust, Golang, Swift... et se voit dédié certains langages : AssemblyScript et Grain par exemple.
Je vous invite à regarder la slide 35 qui récapitule tout bien => j'indiquerai le lien vers la présentation ASAP.

Ensuite nous passons à la partie démo, vous la trouverez dans la vidéo youtube sur la chaîne DevoxxFR : à venir.
ça parle de pointeurs de mémoire (oups!), d'emojis 😉, d'accès au système d'exploit avec WASI (spoiler : jeu de mot pictural à suivre), wasmer, wasmtime, wasmedge... 

![WASI]({{ site.url }}{{ site.baseurl }}/assets/images/wasm5.png)

On passe un très bon moment : merci à tous les deux !

Pour suivre Laurent et Philippe sur twitter, ça se passe par là : [@ldoguin](https://twitter.com/ldoguin) et [@k33g_org](https://twitter.com/k33g_org)

![Nous sommes en salle Neuilly 252 AB et il y a beaucoup de monde]({{ site.url }}{{ site.baseurl }}/assets/images/wasm3.png)

### Architecturoplastie hexagonale d'un backend Node.js : Opération à coeur ouvert - Jordan NOURRY, Adrien JOLY et Julien TOPCU

Bienvenue à Shodopital, nos trois internes charcutent et décortiquent du code pour en tirer le plus de bénéfices possibles.
Première biopsie clean-codienne : on clarifie notre code !

![Les mains sont propres, on peut commencer l'opération dans le bloc]({{ site.url }}{{ site.baseurl }}/assets/images/nodejs1.png)

On précise nos paramètres, on refactore doucement mais sûrement, on reboote le patient (si ! si ! c'est possible !) et on redonne du sens pour éclaircir la compréhension du code.
Même les tests d'intégration présents sont piègeux ! et les changements en codebase ne sont pas trackés => comment faire ?

Non, on n'utilise pas un bistouri, on va casser l'ordinateur... Non, on va plutôt d'intéresser au comportement attendu des APIs et créer des approval tests. Et on teste régulièrement ! à chaque mmodification ! le pas à pas.
On supprime les undefined et les null.

Le nom des fonctions doit signifier ce que fait la fonction : on s'allège ainsi la charge mentale de relecture de tout le code pour le comprendre.

Enfin, on centralise le fonctionnel et sa complexité : on arrête de la disperser un peu partout dans notre architecture ! (à bon entendeur...)

Le but de l'architecture hesagonale, est donc d'inverser le sens de la dépendance entre la couche domain et la couche de persistence, normalement rencontré dans le modèle classique.

Controller ->use-> Domain <-use<- Persistence

Domain devient un hexagone où les objets métiers sont centralisés.

Pour suivre Jordan, Adrien et Julien, ça se passe par là : [@JkNourry](https://twitter.com/JkNourry) , [@adrienjoly](https://twitter.com/adrienjoly) et [@JulienTopcu](https://twitter.com/JulienTopcu)

![Nous sommes en salle Neuilly 252 AB et il y a beaucoup de monde.]({{ site.url }}{{ site.baseurl }}/assets/images/nodejs2.png)

Et n'oubliez pas, nous co-organisons, avec CraftsRecords et TADx, le Tremplin des speakers le 3 mai à Tours pour donner la chance à des speakers débutants de gagner une conférence au Camping des speakers, dans le Golfe du Morbihan les 9 & 10 juin 2022.
Inscriptions pour faire partie du public-jury du tremplin le 3 mai => https://www.eventbrite.fr/e/billets-le-tremplin-du-camping-des-speakers-306273120147


### Rendez l'agilité aux développeurs et développeuses ! - votre humble serviteuse

Le palpitant accélère petit à petit depuis la fin de la dernière université (peut-être même pendant). Trop pour me concentrer sur une autre conférence.
248 inscrits sur l'application Devoxx, syndrôme de l'imposteur au max, je pense à mon premier jury de guitare classique quand j'étais au CP : même envie irresistible de monter sur scène mais pour faire une blague et repartir aussitôt.

J'attends sagement mon tour, entourée des personnes adorables (Stéphane en premier mais aussi Jérémy, Faustine, Corentin, Yann-Thomas, Olivier, Christophe, Thibault, et j'en oublie ! pardon...). Je passe dans les mains du technicien (adorable aussi), Adrien et Arnaud me rassurent à la dernière minute : merci à tous !

![Allez, il faut y aller !]({{ site.url }}{{ site.baseurl }}/assets/images/rendez1.png)

J'ai adoré la prise de risque, j'ai aimé préparer, répéter, partager, rencontrer des gens grâce à ce partage... Un grand merci aux organisateurs et aux membres du comité de sélection de m'avoir offert cette occasion unique !


### Créer & distribuer un plugin pour Kubernetes en quelques minutes ? Easy ! - Aurélie VACHE et Gaëlle ACAS

Grâce à une super organisation des talks, j'ai pu assister à cette présentation péchue et accessible pour nous autres communs des mortels !

![En place]({{ site.url }}{{ site.baseurl }}/assets/images/kube1.png)

Des gophers et une partie théorique plus tard (ou on se rend compte que l'important dans kubectl, ce n'est pas de savoir le prononcer, mais bien de l'utiliser !), place à la pratique : live-coding !!
La présentation est fun et accessible : on apprend autant qu'on passe un bon moment.
Le bon conseil : ne pas hésitez à partager ses trouvailles par des index à défaut de pouvoir l'ajouter dans le Krew index : tout est utile !

![Gaelle et Aurélie]({{ site.url }}{{ site.baseurl }}/assets/images/kube2.png)

Et pour les commandes ou plugins utiles et les bonnes pratiques : revisionnez à souhait la présentation (vidéo bientôt disponible en lien ici) ou référez-vous aux sketchnotes d'Aurélie sur le sujet (lien ici bientôt).

J'ai beau avoir déjà vu la présentation à la [TADx](https://www.tadx.fr) de février 2021 à distance et au JugSummerCamp de septembre 2021, je ne me lasse pas : Gaëlle et Aurélie sont à voir et à connaître absolument !

Pour suivre Aurélie et Gaëlle, ça se passe par là : [@aurelievache](https://twitter.com/aurelievache) et [@Gaelleacas](https://twitter.com/Gaelleacas)

![Be jealous : j'ai un sticker collector]({{ site.url }}{{ site.baseurl }}/assets/images/kube3.png)


## Bilan de la première journée

Ouf ! sacrée journée ! je vais laisser la pression redescendre, participer au dîner des speakers, rencontrer encore plein de gens formidables, merci à toutes et tous !

![Sticker de speaker, et pas l'inverse]({{ site.url }}{{ site.baseurl }}/assets/images/repasspeak2.png)

On vous donne rendez-vous demain jeudi 21/04 à 20h pour le [BOF TADx](https://cfp.devoxx.fr/2022/talk/FIT-6322/Mais_au_fait_DevRel_c'est_vraiment_qu'un_lanceur_de_paillettes_%3F) - Tours Agile & DevOps experience à 20h autour de fabuleux DevRel !
(TADx, injustement non renommé PADx pour Paris Agile & DevOps experience pour l'occasion, mais j'aurai le dernier mot un jour...)
