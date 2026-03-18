---
date: 2026-03-18
description: Apprenez à convertir un PSD en PNG tout en modifiant la profondeur de
  bits du PNG avec Aspose.PSD pour Java – guide étape par étape avec des exemples
  de code.
linktitle: Specify PNG Bit Depth in Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Comment convertir un PSD en PNG avec une profondeur de bits spécifiée en utilisant
  Aspose.PSD pour Java
url: /fr/java/optimizing-png-files/specify-png-bit-depth/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir PSD en PNG avec profondeur de bits spécifiée à l'aide d'Aspose.PSD pour Java

## Introduction
Si vous devez **convert psd to png** et contrôler la profondeur de bits exacte du PNG, vous êtes au bon endroit. Dans ce tutoriel, nous verrons comment modifier la profondeur de bits du PNG tout en enregistrant un fichier PSD au format PNG avec Aspose.PSD pour Java. Que vous construisiez un outil de traitement par lots, un service web ou une utilité de bureau, pouvoir **save png with options** comme le type de couleur en niveaux de gris et une profondeur de bits personnalisée vous donne un contrôle fin sur la qualité de l'image et la taille du fichier.

## Quick Answers
- **Can I change the PNG bit depth?** Yes – use `PngOptions.setBitDepth()` to specify 1, 2, 4, 8, or 16 bits.  
- **Which color types are supported?** Grayscale, TrueColor, Indexed, and others via `PngColorType`.  
- **Do I need a license for Aspose.PSD?** A free trial works for development; a commercial license is required for production.  
- **What Java version is required?** Java 8+ (the library is compatible with newer JDKs).  
- **Is the code runnable as‑is?** Yes – just replace the placeholder path with your own folder.

## What is “convert psd to png” with custom bit depth?
Convertir un fichier Photoshop PSD en image PNG est une tâche courante lorsque vous avez besoin d’un format adapté au web. Ajouter la possibilité d’**adjust png quality** en définissant la profondeur de bits vous permet d’équilibrer la fidélité visuelle et la taille du fichier, ce qui est particulièrement utile pour les miniatures, les icônes ou lorsque la bande passante est limitée.

## Why use Aspose.PSD for Java?
Aspose.PSD pour Java fournit une API de haut niveau qui abstrait la complexité du format PSD. Elle vous permet de **create grayscale png**, **save png with options**, et de gérer les profils colorimétriques sans manipuler les octets de bas niveau. La bibliothèque est entièrement gérée, multiplateforme et reçoit des mises à jour régulières.

## Prerequisites
Avant de plonger dans le code, assurez‑vous de disposer de ce qui suit :

1. **Java Development Kit (JDK)** – téléchargez‑le depuis [le site d’Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java** – obtenez le JAR le plus récent via [ce lien](https://releases.aspose.com/psd/java/).  
3. **Basic Java knowledge** – vous devez être à l’aise avec les classes, les méthodes et la gestion des exceptions.  
4. **An IDE** such as IntelliJ IDEA or Eclipse (optional but recommended).  
5. **A sample PSD file** – placez‑le dans un dossier que vous référencerez dans le code.

Tout est‑t‑il prêt ? Super – importons les packages nécessaires.

## Import Packages
Maintenant que nous avons couvert les prérequis, il est temps de configurer notre environnement en important les packages pertinents dans notre application Java. Ouvrez votre environnement de développement et ajoutez les instructions d’importation suivantes en haut de votre fichier Java :

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Ces déclarations importent les classes que nous utiliserons tout au long du tutoriel, nous permettant de charger des fichiers PSD et de les enregistrer en images PNG avec la profondeur de bits spécifiée.

## Step 1: Set Up Your Document Directory
Avant de commencer le traitement d’image, définissons un répertoire où nos images seront stockées. C’est l’équivalent de créer un dossier pour vos fournitures d’art avant de commencer un projet de bricolage.

```java
String dataDir = "Your Document Directory";
```

## Step 2: Load the PSD Image
Ensuite, nous devons charger le fichier d’image PSD que vous souhaitez convertir. Pensez à cela comme ouvrir une toile sur laquelle vous effectuerez tout votre travail.

```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "sample.psd");
```

Ici, nous utilisons la méthode `Image.load()` pour lire notre fichier PSD d’exemple et le convertir en `PsdImage` afin d’accéder aux propriétés spécifiques au PSD.

## Step 3: Create PNG Options
Une fois notre toile ouverte, nous avons besoin d’un ensemble d’options pour la façon dont nous voulons enregistrer notre image. C’est essentiellement choisir vos couleurs et vos styles de pinceau avant de commencer à peindre.

```java
PngOptions options = new PngOptions();
```

Dans cette étape, nous initialisons une instance de `PngOptions`, qui nous permet de spécifier les paramètres de notre sortie PNG.

## Step 4: Set the Desired Color Type
Maintenant, nous décidons quel type de couleurs nous voulons dans le PNG final. Optez‑vous pour une palette colorée ou un style monochrome ? Prenons cette décision !

```java
options.setColorType(PngColorType.Grayscale);
```

Dans cet exemple, nous définissons le type de couleur sur niveaux de gris. Vous pourriez également choisir `PngColorType.TrueColor` si vous voulez une image en couleur complète. C’est la partie où nous **create grayscale png**.

## Step 5: Specify the Bit Depth
Passons maintenant à la spécification de la profondeur de bits. C’est similaire à dire à votre imprimante à quel point elle doit imprimer finement votre image – plus il y a de bits, plus il y a de détails !

```java
options.setBitDepth((byte)1);
```

Ici, nous définissons la profondeur de bits à **1 bit**, ce qui convient aux images simples en niveaux de gris. Vous pouvez changer la valeur à 2, 4, 8 ou 16 selon vos exigences de qualité – un exemple classique de **change png bit depth**.

## Step 6: Save the PNG Image
Enfin, il est temps d’enregistrer votre chef‑d’œuvre ! Cette étape conclut notre projet en transférant effectivement notre création du canevas d’édition à un mur de galerie.

```java
psdImage.save(dataDir + "SpecifyBitDepth_out.png", options);
```

En utilisant la méthode `save()` de `PsdImage`, nous enregistrons le fichier converti en appliquant les options que nous avons définies. Voilà ! Notre image est maintenant enregistrée avec la profondeur de bits personnalisée.

## Common Issues and Solutions
- **`NullPointerException` when loading the PSD** – double‑check that `dataDir` points to the correct folder and that `sample.psd` exists.  
- **Unsupported bit depth** – Aspose.PSD supports 1, 2, 4, 8, and 16 bits for PNG. Using any other value will throw an `IllegalArgumentException`.  
- **Color type mismatch** – if you set a bit depth that isn’t compatible with the chosen `PngColorType`, the library will automatically adjust to the nearest supported setting.

## Frequently Asked Questions

**Q: What is Aspose.PSD for Java?**  
A: Aspose.PSD for Java is a library for working with PSD files in Java applications, allowing you to manipulate and convert images.

**Q: How do I specify different bit depths?**  
A: You can set the bit depth by using the `options.setBitDepth((byte)n)` method, replacing `n` with your desired depth.

**Q: Can I use Aspose.PSD for free?**  
A: Yes, you can try out the library with a free trial which you can find [here](https://releases.aspose.com/).

**Q: Where can I get a support license for Aspose?**  
A: For a temporary license, you can apply [here](https://purchase.aspose.com/temporary-license/).

**Q: What type of images can I convert?**  
A: Aspose.PSD primarily deals with PSD files, but it supports conversion to various formats like PNG, JPEG, and TIFF.

## Conclusion
Vous avez maintenant appris comment **convert psd to png** tout en contrôlant la profondeur de bits du PNG à l’aide d’Aspose.PSD pour Java. En ajustant les `PngOptions`, vous pouvez **adjust png quality**, créer **grayscale png**, et affiner la taille du fichier pour n’importe quel scénario. Expérimentez avec différents types de couleur et profondeurs de bits pour trouver le parfait équilibre pour votre application.

---

**Last Updated:** 2026-03-18  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}