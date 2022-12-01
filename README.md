# Découverte du HTML

> Découverte du HTML avec Fabien Simon formateur chez IT-AKADEMY.

## Découverte de l'IDE (Environnement de dévelopement gratuit)

Nous utilisons Visual Studio Code, un IDE créé par Microsoft et Open Source.
Il est utilisé ce jour (01/12/2022) pour concevoir une première web.

## Découvertes de la nomenclature d'un fichier HTML

Il faut se faire une analogie pour bien comprendre ce à quoi correspond le HTML du CSS et du JS (JavaScript).

- HTML (**Hypertext Markup Language**). Ce langage n'est pas un langage de **programmation** mais il s'agit d'un langage permettant de **structurer** nos pages web. Ainsi un navigateur va pouvoir traiter celui-ci correctement en fonction des "**TAGS**" appelés en français **BALISES**.

> L'importance d'utiliser un TAG correspondant à ce que l'on souhaite nous aidera se rapprocher des meilleurs places dans le référencements sur GOOGLE. **_Attention il ne s'agit pas de sélectionner que les bon tags, d'autres choses seront pris en compte et surtout qui influerons sur notre positionnement..._**.

Il faut l'imager comme le **SQUELETTE D'UN CORPS HUMAIN**.

- CSS (**Cascade Styles Sheets**). à éditer en fonction de ce qui sera dit.

Il faut à son tour imager celui-ci comme par exemple **LA PIGMENTATION DE LA PEAU D'UN CORPS HUMAIN**, il en existe de toutes sortent et vis à vis d'une page web, si on nous demande de concevoir un site à partir de simplement des informations écrites, il serait pratiquement **improbable** de retrouver un code strictement identique...

- JS (JavaScript). à éditer en fonction de ce qui nous aura été dit.

Enfin ici il faut l'imager comme si on avait la possibilité de donner vie à notre humain.
J'entends par là qu'il est possible qu'il marche, qu'il saute, qu'il nage et surtout qu'il parle.

## La structure d'un code HTML classique

```html
<!DOCTYPE html>
<html lang="en">
  <!-- Ici c'est tout ce qui fera références aux en-tête de notre page web -->
  <head>
    <!-- le charset UTF-8 permet d'interprêter les accents dans un navigateur -->
    <meta charset="UTF-8" />
    <!-- Pour EDGE (Internet Explorer) -->
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <!-- Pour optimiser le responsive -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <!-- Le title permet de définir le nom qui sera affiché dans notre onglet -->
    <title>Document</title>
  </head>
  <!-- Dans le Body c'est exactement tout ce qui sera visible à l'écran -->
  <body>
    <!-- Du code... -->
  </body>
</html>
```

## Les différentes tailles d'un titre

```html
<body>
  <!-- Il existe 6 niveau de titre -->
  <h1>Titre de Niveau h1</h1>
  <h2>Titre de Niveau h2</h2>
  <h3>Titre de Niveau h3</h3>
  <h4>Titre de Niveau h4</h4>
  <h5>Titre de Niveau h5</h5>
  <h6>Titre de Niveau h6</h6>
</body>
```

## La conception d'un paragraphe

```html
<body>
  <!-- Pour générer un paragraphe -->
  <p>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Provident porro ad
    eaque explicabo tempore ullam veniam totam temporibus optio tempora.
  </p>
</body>
```

- Bonus (Lorem ipsum)

> Saisissez dans votre IDE le mot clé **lorem** suivie d'un nombre **20** par exemple qui correspondrait aux nombre de mots que vous souhaitez générer en latin afin de compléter du contenu.

Le paragraphe précédent utilisait un **lorem20**

## Les listes

Les listes peuvent-être des listes à puces (**UL**) ou bien des liste ordonnées (**OL**).

```html
<body>
  <!-- Conception d'une liste non ordonnée -->
  <ul>
    <li>Je suis un premier point</li>
    <li>Je suis un second point</li>
    <li>Je suis un troisième point</li>
  </ul>

  <!-- Conception d'une liste ordonnée -->
  <ol>
    <li>Je suis un premier point</li>
    <li>Je suis un second point</li>
    <li>Je suis un troisième point</li>
  </ol>
</body>
```

## Découverte des liens

Le lien permet de rediriger un élément spécifique vers une quelconque page de son site mais également sur un quelconque site externe.

> Ce qui est vachement important c'est de bien comprendre **les chemins dit relatif** et **les chemins absolue**.

- **Les chemins relatifs**
  - _Ils sont utilisées afin de pouvoir spécifier un élément spécifique de son site (une image, une autre page ou autre.)_
- **Les chemins absolue**

  - Il sont utilisées afin de rediriger vers une page externe de son site.

- **ATTRIBUT**
  1. **href** qui est insipensable, c'est là où l'on place notre lien.
  2. **target** qui permet de spécifier l'option **\_blank** afin d'ouvrir cette page dans un autre onglet de son navigateur.

```html
<body>
  <!-- Un lien RELATIF -->
  <a href="./contact.html" target="_blank">Contactez-moi<a />

  <!-- Un lien ABSOLUE -->
  <a href="https://www.google.fr" target="_blank">Google.fr<a />
</body>
```

## Les images

Pour une image, on utilise un **TAG ORPHELIN**, en effet il n'existe aucun **TAG DE FERMETURE**.
Deux attributs **SONT INDISPENSABLE**.

1. **src** qui correspond à la source du fichier. (_lien relatif ou absolue_)
2. **alt** qui sera utilisé au cas où si l'image n'est pas fonctionnel. Alors un message sera affiché avec le contenu du alt.

```html
<body>
  <!-- Un image -->
  <img src="" alt="" />
</body>
```

> Il est possible d'ajouter deux autres attributs qui sont **facultatif**.
> Ils sont utile si l'on ne connait pas le CSS et que l'on doit spécifier une plus petite taille que l'image de base.

1. **width** pour ce qui concerne la largeur.
2. **height** pour ce qui concerne la hauteur.

Par défaut le pixel sera utilisé et donc il est possible d'ommettre le sigle **px** après la valeur renseignée.

> Pour fabien il vaut mieux la saisir pour éviter un conflit avec un autre développeur qui n'a pas votre logique.

```html
<body>
  <!-- Un image avec les attributs indispensables -->
  <img
    src="./assets/images/plage.jpg"
    alt="Voici une superbe photo d'une plage libre de droit."
  />

  <!-- Un image avec les attributs indispensables et facultatifs -->
  <img
    src="./assets/images/plage.jpg"
    alt="Voici une superbe photo d'une plage libre de droit."
    width="600px"
    height="400px"
  />
</body>
```

**ATTENTION AVEC L'ATTRIBUT "HEIGHT", VOUS RISQUEZ TRÈS PROBABLEMENT DE DEFORMER VOTRE IMAGE.** On préfèrera définir les valeurs dans le CSS et y inclure ici les valeurs d'origine de l'image. (bonne pratique)

## Bonus un lien qui redirige vers google en cliquant sur une photo ou bien un paragraphe

**Sophie**, cherchait comment rediriger vers une page web quelconque en fonction d'un clic sur une quelconque image.

```html
<body>
  <!-- Un lien vers google au clic sur une image -->
  <a href="https://www.google.fr" target="_blank">
    <img
      src="./assets/images/plage.jpg"
      alt="Voici une superbe photo d'une plage libre de droit."
    />
  <a />

  <!-- Un lien vers google au clic sur un paragraphe -->
  <a href="https://www.google.fr" target="_blank">
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Provident porro ad
      eaque explicabo tempore ullam veniam totam temporibus optio tempora.
    </p>
  <a />
</body>
```

## Conception des tableaux

Les tableaux sont un ensemble de tag qui seront imbriqués les uns aux autres.

- **TR** correspond à une nouvelle ligne (_table row_)
- **TH** correspond à une mise en forme de type TITRE (_table head_)
- **TD** correspond à une nouvelle cellule (_table data_)

```html
<body>
  <!-- Conception d'un tableau d'une liste de courses -->
  <table>
    <tr>
      <th>Ref</th>
      <th>Nom</th>
      <th>Désignation</th>
      <th>Quantité(s)</th>
      <th>Prix unitaire</th>
      <th>Total</th>
    </tr>

    <tr>
      <td>1597534682</td>
      <td>Pain au chocolat</td>
      <td>
        Ce pain avec une barre en chocolat va te rendre tellement accro que tu
        en redemanderas.
      </td>
      <td>13</td>
      <td>0.75€</td>
      <td>9.75€</td>
    </tr>
    <tr>
      <td>9518526543</td>
      <td>Pizzas Triangulaire</td>
      <td>
        Tu découvriras cette pizzas avec une forme chelou... Mais vu la classe
        ça colle bien pour vous :d
      </td>
      <td>13</td>
      <td>8.00€</td>
      <td>104.00€</td>
    </tr>
    <tr>
      <td>4567891334</td>
      <td>Imac</td>
      <td>
        Putain quelle kiff de bosser sur des claviers mac aussi dégeulasse que
        ça...
      </td>
      <td>13</td>
      <td>49€</td>
      <td>637.00€</td>
    </tr>
    <tr>
      <!-- colspan permet de fusionner un certain nombre de colone (ici 5) -->
      <th colspan="5">Prix TVA 5.5%</th>
      <td>41.29€</td>
    </tr>
    <tr>
      <!-- colspan permet de fusionner un certain nombre de colone (ici 5) -->
      <th colspan="5">Prix HT</th>
      <td>750.75€</td>
    </tr>
    <tr>
      <!-- colspan permet de fusionner un certain nombre de colone (ici 5) -->
      <th colspan="5">Prix TTC</th>
      <td>792.04€</td>
    </tr>
    <tr></tr>
  </table>
</body>
```

## Les formulaires

Les formulaires sont utilisés de partout.
Un formulaire se compose d'un tag **FORM**.

Si aucun attribut n'est passé, par défaut celui-ci te redirigera vers la même page que là où tu te situe.

Si tu souhaite rediriger vers une toute autre page, tu définiras l'attribut **action** avec le chemin relatif ou tu veux rediriger l'utilisateur.

> **NE FAIT JAMAIS CONFIANCE A LA SAISIE D'UN QUELCONQUE UTILISATEUR !!!** > _moi le premier_ :P

```html
<body>
  <!-- Ouverture d'un formulaire sans rien dedans -->
  <form>
    <!-- Tout ce qui est en lien au formulaire doit se trouver dans cette partie -->
  </form>

  <!-- Redirection vers une autre page -->
  <form action="./contact.html">
    <!-- Imaginons que nous ayons soumis notre formulaire via un "button de type submit",
    alors les informations seront transmis par défaut en GET (méthode)
    et ils seront visible dans la barre d'adresse de ton navigateur. -->
  </form>
</body>
```

### Différents Input

```html
<body>
  <!-- Redirection vers une autre page -->
  <form action="./contact.html">
    <!-- FOR est directement lié à l'ID de l'input -->
    <label for="lastname">Nom:</label>
    <!-- NAME est le nom que l'on récupèrera lorsque l'on traitera 
    nos formulaire que ce soit en PHP ou bien en JAVASCRIPT -->
    <input type="text" placeholder="votre nom" id="lastname" name="lastname" />
  </form>
</body>
```

Il existe un bon nombre de type et très franchement le mieux étant de les rechercher par vous même ;)

#### LA SUITE DEMAIN AVEC LE CODE HTML CORRESPONDANT
