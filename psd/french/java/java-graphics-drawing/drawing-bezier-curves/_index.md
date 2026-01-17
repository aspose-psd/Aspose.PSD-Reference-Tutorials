---
date: 2026-01-17
description: Apprenez à créer une image de courbe de Bézier en Java avec Aspose.PSD.
  Ce guide étape par étape couvre les techniques de dessin de courbes de Bézier en
  Java, les réglages de l'épaisseur du crayon et l'exportation du résultat.
linktitle: How to Create Bezier Curve Image in Java
second_title: Aspose.PSD Java API
title: Comment créer une image de courbe de Bézier en Java
url: /fr/java/java-graphics-drawing/drawing-bezier-curves/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment créer une image de courbe de Bézier en Java

## Introduction
Si vous devez **créer une image de courbe de Bézier** pour une application Java de bureau ou côté serveur, Aspose.PSD for Java rend la tâche indolore. Dans ce tutoriel, nous allons parcourir le dessin d’une courbe de Bézier lisse, la personnalisation de la largeur du crayon, et l’enregistrement du résultat sous forme de bitmap. À la fin, vous serez à l’aise avec la méthode `drawBezier()` et prêt à intégrer des graphiques de style vectoriel dans n’importe quel projet Java.

## Quick Answers
- **Quelle bibliothèque est la meilleure pour dessiner des courbes en Java ?** Aspose.PSD for Java fournit une API graphique complète.  
- **Combien de temps faut‑il pour créer une image de courbe de Bézier basique ?** Généralement moins de 10 minutes une fois le SDK installé.  
- **Quels formats d’image sont pris en charge pour l’exportation ?** BMP, PNG, JPEG, TIFF, et plus encore.  
- **Puis‑je modifier la largeur du crayon de la courbe ?** Oui – le constructeur `Pen` vous permet de spécifier n’importe quelle largeur dont vous avez besoin.  
- **Ai‑je besoin d’une licence pour une utilisation en production ?** Une licence commerciale est requise pour les déploiements non‑évaluation.

## Qu’est‑ce que « create bezier curve image » ?
Créer une image de courbe de Bézier signifie générer une image raster contenant une courbe définie mathématiquement. La courbe est définie par un point de départ, deux points de contrôle et un point d’arrivée, vous permettant de produire des formes lisses et évolutives qui restent belles à n’importe quelle taille.

## Pourquoi utiliser Aspose.PSD for Java ?
- **Primitives graphiques riches** – dessinez des lignes, formes et courbes sans manipuler les pixels au bas niveau.  
- **Multiplateforme** – fonctionne sur tout OS supportant Java.  
- **Prise en charge haute résolution** – gérez de grandes toiles sans consommation excessive de mémoire.  
- **Exportation facile** – passez de BMP, PNG, JPEG, TIFF avec une seule ligne de code.

## Prérequis
Avant de commencer, assurez‑vous d’avoir :

1. **Java Development Kit (JDK)** – toute version récente (8 ou supérieure).  
2. **Aspose.PSD for Java JAR** – téléchargez‑le depuis [here](https://releases.aspose.com/psd/java/) et ajoutez‑le au classpath de votre projet.  
3. **IDE** – Eclipse, IntelliJ IDEA, ou tout éditeur de votre choix, configuré avec le JDK.

## Import Packages
Avant de plonger dans l’implémentation, importez les classes Aspose.PSD nécessaires :

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## Step‑by‑Step Guide

### Step 1: Create an Image Instance
Tout d’abord, vous devez créer une instance de la classe `PsdImage`, qui représente une image PSD en mémoire.

```java
String dataDir = "Your Document Directory";
Image image = new PsdImage(100, 100);
```

*Explanation*: `PsdImage` est instanciée avec une largeur et une hauteur de **100 × 100 pixels** – vous pouvez augmenter ces valeurs pour une sortie à plus haute résolution.

### Step 2: Initialize Graphics Context
Ensuite, initialisez une instance de la classe `Graphics` pour effectuer des opérations de dessin sur l’image.

```java
Graphics graphics = new Graphics(image);
```

*Explanation*: L’objet `Graphics` lie les commandes de dessin à l’`image` que nous venons de créer.

### Step 3: Clear the Graphics Surface
Effacez la surface graphique en utilisant une couleur d’arrière‑plan spécifique, ici `Color.getYellow()`.

```java
graphics.clear(Color.getYellow());
```

*Explanation*: Cela définit un arrière‑plan jaune vif afin que la courbe de Bézier noire se détache.

### Step 4: Initialize Pen for Drawing
Configurez un objet `Pen` avec des propriétés telles que la couleur et la largeur pour définir comment la courbe sera dessinée.

```java
Pen blackPen = new Pen(Color.getBlack(), 3);
```

*Explanation*: Le crayon est noir et **3 pixels de large** – vous pouvez ajuster la largeur pour rendre la courbe plus épaisse ou plus fine (`java graphics pen width`).

### Step 5: Define Bezier Curve Parameters
Spécifiez les points de contrôle et les points d’arrivée pour la courbe de Bézier.

```java
float startX = 10, startY = 25;
float controlX1 = 20, controlY1 = 5;
float controlX2 = 55, controlY2 = 10;
float endX = 90, endY = 25;
```

*Explanation*:  
- `startX`, `startY` – point de départ de la courbe.  
- `controlX1`, `controlY1` – premier point de contrôle.  
- `controlX2`, `controlY2` – deuxième point de contrôle.  
- `endX`, `endY` – point d’arrivée.

### Step 6: Draw the Bezier Curve
Utilisez la méthode `drawBezier()` pour tracer la courbe de Bézier sur l’image en utilisant le `Pen` et les points de contrôle définis précédemment.

```java
graphics.drawBezier(blackPen, startX, startY, controlX1, controlY1, controlX2, controlY2, endX, endY);
```

*Explanation*: Cet appel unique rend une ligne **draw bezier curve java** lisse qui suit les points de contrôle fournis.

### Step 7: Save the Image
Enregistrez l’image dessinée au format BMP.

```java
String outpath = dataDir + "Bezier.bmp";
BmpOptions saveOptions = new BmpOptions();
image.save(outpath, saveOptions);
```

*Explanation*: L’objet `BmpOptions` indique à Aspose.PSD d’écrire le fichier au format BMP. Remplacez‑le par `PngOptions`, `JpegOptions`, etc., si vous avez besoin d’un autre format.

## Common Issues & Solutions
- **La courbe apparaît plate** – Vérifiez les coordonnées des points de contrôle ; elles ne doivent pas être colinéaires avec les points de départ/arrivée.  
- **L’image est vide** – Assurez‑vous que `graphics.clear()` est appelé avant le dessin, et que la couleur du `Pen` contraste avec l’arrière‑plan.  
- **OutOfMemoryError sur de grandes toiles** – Augmentez la taille du tas JVM (`-Xmx`) ou travaillez avec des images découpées.

## FAQ's
### Puis‑je dessiner plusieurs courbes de Bézier dans la même image ?
Oui, vous pouvez dessiner plusieurs courbes en répétant le processus dans une boucle, en modifiant les points de contrôle et les points d’arrivée selon vos besoins.

### Comment changer la couleur de la courbe de Bézier ?
Modifiez la propriété couleur de l’objet `Pen` (`Color.getBlack()` dans l’exemple) avant d’appeler `drawBezier()`.

### Aspose.PSD for Java convient‑il aux images haute résolution ?
Oui, Aspose.PSD for Java prend en charge les images haute résolution avec une gestion efficace de la mémoire.

### Puis‑je exporter l’image vers des formats autres que BMP ?
Oui, Aspose.PSD for Java permet d’exporter les images vers divers formats comme PNG, JPEG, TIFF, etc.

### Où trouver plus d’exemples et de documentation ?
Visitez la [documentation Aspose.PSD for Java](https://reference.aspose.com/psd/java/) pour des guides complets et des extraits de code.

## Conclusion
En suivant ce **bezier curve tutorial java**, vous savez maintenant comment **créer une image de courbe de Bézier** avec Aspose.PSD for Java. Expérimentez avec différents points de contrôle, couleurs de crayon et largeurs de ligne pour produire une variété d’effets artistiques dans vos applications Java.

---

**Last Updated:** 2026-01-17  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}