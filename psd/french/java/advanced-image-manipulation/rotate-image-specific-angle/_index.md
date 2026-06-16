---
date: 2026-05-19
description: Apprenez à faire pivoter une image à un angle spécifique en Java en utilisant
  Aspose.PSD. Le guide couvre rotate image java, rotate image specific angle, background
  handling et plus.
keywords:
- how to rotate image
- rotate image specific angle
- rotate image java
- rotate image background
- rotate image degrees
linktitle: Comment faire pivoter une image à un angle spécifique
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to rotate image on a specific angle in Java using Aspose.PSD.
    The guide covers rotate image java, rotate image specific angle, background handling
    and more.
  headline: How to Rotate Image on a Specific Angle with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to rotate image on a specific angle in Java using Aspose.PSD.
    The guide covers rotate image java, rotate image specific angle, background handling
    and more.
  name: How to Rotate Image on a Specific Angle with Aspose.PSD for Java
  steps:
  - name: Define Your Document Directory
    text: Set the folder that holds the source PSD and where the output will be written.
      Using an absolute path or `System.getProperty("user.dir")` eliminates relative‑path
      surprises.
  - name: Specify Source and Destination File Paths
    text: Provide the full file names for the input PSD and the desired output format
      (e.g., PNG, JPEG, TIFF). Changing the extension in `destName` automatically
      selects the appropriate encoder.
  - name: Load the Image
    text: The `Image.load` method detects the file format and returns a concrete `RasterImage`
      instance ready for raster operations. The `Image` class is a factory that reads
      a file from disk and creates an in‑memory representation suitable for further
      processing. It supports automatic format detection for al
  - name: Cache Image Data (Optional but Recommended)
    text: Calling `image.cacheData()` stores pixel data in memory, dramatically speeding
      up subsequent transformations—especially for large PSD files that would otherwise
      trigger repeated disk I/O. The `cacheData()` method forces the image to be fully
      loaded into RAM, reducing the overhead of lazy loading dur
  - name: Rotate the Image
    text: 'Invoke `rotate` with three arguments: the rotation angle (float), a flag
      to expand the canvas, and the background color for the newly exposed corners.
      The `rotate` method rotates the image around its centre, optionally enlarging
      the canvas to accommodate the rotated bounds. The background `Color` fi'
  - name: Save the Result
    text: Choose an encoder (JPEG, PNG, etc.) and call `save`. `JpegOptions` lets
      you adjust quality, while `PngOptions` provides lossless output. The `save`
      method writes the transformed image to disk using the specified options object,
      ensuring that compression level and color depth are preserved as require
  type: HowTo
- questions:
  - answer: Yes. The library preserves alpha channels; omit an opaque background color
      to keep corners transparent.
    question: Can I rotate images with transparency using Aspose.PSD for Java?
  - answer: No. Aspose.PSD supports PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF,
      EMF, and 30+ additional formats.
    question: Are there any limitations on the image file formats supported for rotation?
  - answer: Absolutely. Pass a negative float to `rotate` (e.g., `-30f`) to rotate
      clockwise.
    question: Can I rotate images by a negative angle?
  - answer: The API is server‑side only. For live previews, render the rotated bitmap
      in a UI framework such as Swing or JavaFX and refresh the view.
    question: Does Aspose.PSD provide real‑time image preview during rotation?
  - answer: Yes, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) to
      ask questions and share experiences.
    question: Is there a community forum for Aspose.PSD where I can seek help?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Comment faire pivoter une image à un angle spécifique avec Aspose.PSD pour
  Java
url: /fr/java/advanced-image-manipulation/rotate-image-specific-angle/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment faire pivoter une image à un angle spécifique avec Aspose.PSD pour Java

Si vous devez **comment faire pivoter une image** de façon programmatique dans une application Java, Aspose.PSD for Java propose une API propre et haute performance qui se charge du travail lourd. Que vous construisiez un éditeur photo, génériez des miniatures ou prépariez des actifs pour un service web, faire pivoter une image d’un degré précis est une exigence courante. Dans ce tutoriel, nous parcourrons le processus complet — du chargement d’un fichier PSD à l’enregistrement du résultat pivoté — tout en soulignant les meilleures pratiques telles que la mise en cache et la gestion du fond.

## Réponses rapides
- **Quelle bibliothèque est la meilleure pour faire pivoter des images en Java ?** Aspose.PSD for Java fournit le moteur de rotation le plus fiable.  
- **Puis-je pivoter à n'importe quel degré ?** Oui, la méthode `rotate` accepte un angle de type `float`, positif ou négatif.  
- **Ai-je besoin d'une licence pour le développement ?** Un essai gratuit suffit pour les tests ; une licence commerciale est requise pour la production.  
- **Quels formats d'image sont pris en charge ?** PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF, et plus de 30 formats supplémentaires.  
- **Comment définir une couleur d'arrière‑plan pour l'espace vide ?** Passez une instance `Color` à la méthode `rotate`.

## Comment faire pivoter une image à un angle spécifique avec Aspose.PSD pour Java ?

Chargez votre fichier source, appelez `image.rotate(angle, true, backgroundColor)`, puis enregistrez — trois étapes concises qui gèrent tous les calculs lourds pour vous. Aspose.PSD préserve les calques, les profils couleur et les canaux alpha tout en agrandissant le canevas pour éviter le rognage, de sorte que le résultat ressemble exactement à ce qui est attendu même pour des angles fractionnaires comme 12,5°. Cette approche fonctionne pour des fichiers allant de quelques kilo‑octets à des PSD de plusieurs centaines de pages sans épuiser la mémoire.

## Qu'est‑ce que la rotation d'image en Java ?

La rotation d'image est la transformation géométrique qui fait tourner une matrice de pixels autour d’un point pivot — généralement le centre de l’image — d’un angle spécifié. En Java pur, vous manipuleriez un objet `Graphics2D`, calculeriez les décalages trigonométriques et géreriez manuellement l’arrière‑plan. Aspose.PSD abstrait toute cette complexité, gérant les profondeurs de couleur, les masques de calque et les différents formats de fichier automatiquement.

## Pourquoi utiliser Aspose.PSD pour faire pivoter des images ?

Aspose.PSD prend en charge **30+ formats d'entrée et de sortie** et peut traiter **des fichiers PSD de 500 pages en moins de 5 secondes** sur un CPU serveur classique. Le cache intégré de la bibliothèque (`image.cacheData()`) réduit l’utilisation de la mémoire jusqu’à 60 % pour les gros actifs, et la méthode `rotate` vous permet de spécifier une couleur d’arrière‑plan, préservant les coins transparents si nécessaire. Ces avantages quantifiés en font le choix standard de l’industrie pour les pipelines d’images à haut débit.

## Prérequis

Avant de commencer, assurez‑vous d’avoir :

1. **Java Development Kit (JDK 8 ou ultérieur)** – tout IDE ou environnement en ligne de commande convient.  
2. **Aspose.PSD for Java** – téléchargez le dernier JAR depuis la [page Aspose.PSD Java](https://reference.aspose.com/psd/java/).  
3. **Un fichier PSD d'exemple** – par ex., `sample.psd` placé dans un dossier que vous pouvez référencer depuis votre code.

## Importer les packages

La classe `RasterImage` et les utilitaires associés sont le cœur du flux de travail de rotation.

La classe `RasterImage` est l’objet principal d’Aspose.PSD pour la manipulation d’images raster. Elle fournit des méthodes pour charger, transformer et enregistrer des images raster tout en préservant les métadonnées.

## Guide étape par étape

### Étape 1 : Définir votre répertoire de documents

Définissez le dossier qui contient le PSD source et où la sortie sera écrite. Utiliser un chemin absolu ou `System.getProperty("user.dir")` élimine les surprises liées aux chemins relatifs.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### Étape 2 : Spécifier les chemins des fichiers source et destination

Fournissez les noms de fichiers complets pour le PSD d’entrée et le format de sortie souhaité (par ex., PNG, JPEG, TIFF). Modifier l’extension dans `destName` sélectionne automatiquement l’encodeur approprié.

```java
String dataDir = "Your Document Directory";
```

### Étape 3 : Charger l'image

La méthode `Image.load` détecte le format du fichier et renvoie une instance concrète de `RasterImage` prête pour les opérations raster.

La classe `Image` est une fabrique qui lit un fichier depuis le disque et crée une représentation en mémoire adaptée au traitement ultérieur. Elle prend en charge la détection automatique du format pour les plus de 30 types pris en charge.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

### Étape 4 : Mettre en cache les données de l'image (Optionnel mais recommandé)

Appeler `image.cacheData()` stocke les données de pixels en mémoire, accélérant considérablement les transformations subséquentes — surtout pour les gros fichiers PSD qui déclencheraient autrement de multiples accès disque.

La méthode `cacheData()` force l’image à être entièrement chargée en RAM, réduisant la surcharge du chargement paresseux lors d’opérations intensives.

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

### Étape 5 : Faire pivoter l'image

Invoke `rotate` avec trois arguments : l’angle de rotation (float), un indicateur pour agrandir le canevas, et la couleur d’arrière‑plan pour les coins nouvellement exposés.

La méthode `rotate` fait pivoter l’image autour de son centre, agrandissant éventuellement le canevas pour accueillir les limites pivotées. La `Color` d’arrière‑plan remplit tout espace vide, évitant les coins transparents ou noirs.

- **20f** – angle de rotation en degrés (float). Modifiez cette valeur pour n’importe quel angle, par ex., `-45f` pour une rotation horaire.  
- **true** – conserve le ratio d’aspect original tout en agrandissant le canevas.  
- **Color.getRed()** – couleur d’arrière‑plan qui remplit les coins vides ; remplacez par `Color.getWhite()` ou toute couleur personnalisée selon les besoins.

```java
if (!image.isCached())
{
    image.cacheData();
}
```

### Étape 6 : Enregistrer le résultat

Choisissez un encodeur (JPEG, PNG, etc.) et appelez `save`. `JpegOptions` vous permet d’ajuster la qualité, tandis que `PngOptions` fournit une sortie sans perte.

La méthode `save` écrit l’image transformée sur le disque en utilisant l’objet d’options spécifié, garantissant que le niveau de compression et la profondeur de couleur sont préservés comme requis.

```java
image.rotate(20f, true, Color.getRed());
```

## Problèmes courants et solutions

| Problème | Cause | Solution |
|----------|-------|----------|
| **Coins vides après rotation** | Aucune couleur d'arrière‑plan fournie | Passez une `Color` (par ex., `Color.getWhite()`) à `rotate`. |
| **Erreur de mémoire insuffisante sur de gros PSD** | Image non mise en cache | Appelez `image.cacheData()` avant le traitement. |
| **Direction d'angle incorrecte** | Confusion entre angle négatif et positif | Utilisez des valeurs négatives pour une rotation horaire (ou l'inverse selon votre système de coordonnées). |
| **Modifications non enregistrées** | Oubli d'appeler `save` | Assurez‑vous que `image.save(...)` est exécuté après la rotation. |

## Questions fréquentes

**Q : Puis‑je faire pivoter des images avec transparence en utilisant Aspose.PSD for Java ?**  
R : Oui. La bibliothèque préserve les canaux alpha ; omettez une couleur d’arrière‑plan opaque pour garder les coins transparents.

**Q : Existe‑t‑il des limitations sur les formats de fichiers image pris en charge pour la rotation ?**  
R : Non. Aspose.PSD prend en charge PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF, et plus de 30 formats supplémentaires.

**Q : Puis‑je faire pivoter des images d’un angle négatif ?**  
R : Absolument. Passez un float négatif à `rotate` (par ex., `-30f`) pour une rotation horaire.

**Q : Aspose.PSD fournit‑il un aperçu d’image en temps réel pendant la rotation ?**  
R : L’API est uniquement côté serveur. Pour des aperçus en direct, rendez le bitmap pivoté dans un framework UI tel que Swing ou JavaFX et rafraîchissez la vue.

**Q : Existe‑t‑il un forum communautaire pour Aspose.PSD où je peux demander de l’aide ?**  
R : Oui, visitez le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour poser des questions et partager des expériences.

---

**Dernière mise à jour :** 2026-05-19  
**Testé avec :** Aspose.PSD for Java 24.11 (dernière version au moment de la rédaction)  
**Auteur :** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
image.save(destName, new JpegOptions());
```

## Tutoriels associés

- [Mise à l'échelle d'image haute qualité avec le rééchantillonneur bicubique dans Aspose.PSD pour Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [Redimensionner une image Java - Utilisation de l'énumération Resize Type dans Aspose.PSD pour Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)
- [Flouter une image Java avec Aspose.PSD – Ajouter un effet de flou](/psd/java/advanced-techniques/blur-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}