##CSS id et CSS class
Chaque terme permet de créer des propriétés CSS personnalisées, que vous pouvez appliquer à vos balises, mais il existe des différences entre une classe (.toto) et un id (#toto)
---
###Une différence fondamentale
On peut utiliser indifféremment les attributs id et class pour appliquer des styles CSS aux éléments d'une page, mais...

un id s'applique à un objet unique : il ne peut pas y avoir deux mêmes id dans une page
une classe peut caractériser plusieurs objets (identiques ou non)

Par exemple il est possible d'avoir ce code:
```<div class="toto"></div>
<div class="toto"></div>
```


Mais il n'est pas correct d'avoir ce code:
```<div id="toto"></div>
<div id="toto"></div>
```

l'id ne doit désigner qu'un seul objet dans une page HTML même s'il est possible d'avoir plusieurs id dans la feuille de style.

Pour la feuille de style CSS, les règles seront écrites avec la syntaxe #nom_id pour les id et .nom_de_classe pour les class. Par exemple :
```/* L'élément unique id="header", par exemple <div id="header"> */
#header {
  background:red;
}

/* Tous les éléments de classe "liens" : <ul class="liens"> ou <a class="liens">... */
.liens {
  color:blue;
}

/* Tous les paragraphes de classe "article" : <p class="article"> */
p.article {
  text-align:justify;
}
```

Pour du code "rigoureux", ce qui est syntaxiquement le plus juste doit être privilégié. Utilisez les id en priorité lorsque vous le pouvez et les class lorsque vous ne pouvez pas. Une balise HTML peut posséder un id et une (ou plusieurs) class mais pas l'inverse. On peut ainsi cibler une balise particulière au sein d'un ensemble d'éléments possédant la même classe.

Par exemple : commencez à utiliser id systématiquement pour les objets unique pour faciliter la lecture du code. Donnez un id à votre body (pour ancre), à votre bloc en-tête, votre bloc gauche, droit, la navigation... Par contre pour les paragraphes ou listes de menu utilisez les classes lorsqu'il y aura plusieurs objets de ce type.

##Attributs
Un attribut est placé dans une balise HTML ouvrante. Il change la présentation du contenu de l'élément correspondant. Par exemple :
<p align="right">

La syntaxe d'un attribut comprend toujours le nom de l'attribut, suivi du signe = , et de la valeur de l'attribut.

L'utilisation des CSS permet de diminuer l'utilisation des attributs, voire de les éliminer totalement, ce qui a pour avantage de scinder le contenu de sa mise en forme.
