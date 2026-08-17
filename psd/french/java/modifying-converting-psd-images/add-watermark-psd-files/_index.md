---
date: 2026-03-07
description: Apprenez à créer un filigrane d'image dans les fichiers PSD à l'aide
  d'Aspose.PSD pour Java – un guide rapide pour le traitement des images PSD et la
  protection de vos graphiques.
linktitle: How to Create Image Watermark in PSD Files with Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Comment créer un filigrane d'image dans les fichiers PSD avec Aspose.PSD pour
  Java
url: /fr/java/modifying-converting-psd-images/add-watermark-psd-files/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajouter un filigrane aux fichiers PSD avec Aspose.PSD pour Java

## Introduction
Les filigranes sont une façon subtile mais efficace de protéger vos images et d’affirmer la propriété. Dans ce tutoriel, vous apprendrez à **créer un filigrane d’image** dans des fichiers PSD à l’aide d’Aspose.PSD pour Java. Que vous soyez photographe présentant votre portfolio ou designer montrant votre dernier travail, ajouter un filigrane peut être crucial pour maintenir l’identité de votre marque. Alors, prenez une tasse de café, installez‑vous confortablement, et commençons !

## Quick Answers
- **Quel est l’objectif principal ?** Créer un filigrane d’image dans un fichier PSD de façon programmatique.  
- **Quelle bibliothèque est utilisée ?** Aspose.PSD pour Java.  
- **Combien de temps prend l’implémentation ?** Environ 10‑15 minutes pour un filigrane basique.  
- **Quelles sont les principales prérequis ?** Java JDK, bibliothèque Aspose.PSD et un fichier PSD source.  
- **Puis‑je exporter le résultat en PNG ?** Oui – utilisez la méthode `save` avec `PngOptions`.

## Qu’est‑ce que **create image watermark** ?
Créer un filigrane d’image signifie superposer de façon programmatique du texte ou des graphiques semi‑transparents sur un fichier image afin que les informations de propriété soient intégrées directement au contenu visuel.

## Pourquoi utiliser Aspose.PSD pour Java pour le traitement d'images psd ?
Aspose.PSD fournit un ensemble riche d’API pour le **psd image processing**, vous permettant de manipuler les calques, d’appliquer des effets et de rendre l’image finale sans avoir besoin de Photoshop. Il prend en charge le rendu haute fidélité, les opérations par lots et fonctionne sur tous les principaux systèmes d’exploitation.

## Prérequis
Avant de plonger dans le code, assurez‑vous de disposer de ce qui suit :

1. **Java Development Kit (JDK)** – toute version récente (8 ou supérieure).  
2. **Aspose.PSD pour Java Library** – téléchargez‑la depuis le [site Aspose](https://releases.aspose.com/psd/java/).  
3. **IDE** – Eclipse, IntelliJ IDEA ou tout éditeur de votre choix.  
4. **Fichier PSD** – un fichier d’exemple nommé `layers.psd` placé dans votre répertoire de travail.  
5. **Connaissances de base en Java** – familiarité avec les classes, les objets et les entrées/sorties de fichiers.

## Import Packages
Maintenant que tout est configuré, importons les packages nécessaires. Les imports en Java vous permettent d’inclure des classes et fonctions provenant de diverses bibliothèques, rendant votre code plus efficace. Voici ce dont vous aurez besoin :

```java
import com.aspose.psd.Color;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringAlignment;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## Comment **create image watermark** – Guide étape par étape

### Étape 1 : Configurer votre répertoire
Tout d’abord, nous devons définir le chemin où se trouve votre fichier PSD. C’est crucial car Java doit savoir où chercher vos fichiers.

```java
String dataDir = "Your Document Directory";
```

Remplacez `Your Document Directory` par le dossier réel contenant `layers.psd`.

### Étape 2 : Charger le fichier PSD
Ensuite, nous chargerons le fichier PSD et le convertirons en un `PsdImage`. Cette étape transforme le fichier en un format que nous pouvons manipuler.

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Considérez cela comme l’ouverture d’un livre afin de pouvoir écrire sur ses pages.

### Étape 3 : Créer un objet Graphics
Avec le fichier PSD maintenant chargé, nous devons créer un objet `Graphics`. Cela nous permet d’effectuer des opérations de dessin – essentiellement comme prendre un pinceau pour votre toile.

```java
Graphics graphics = new Graphics(psdImage);
```

### Étape 4 : Définir la police pour votre filigrane
Il est temps de choisir l’apparence de votre filigrane. Nous utiliserons Arial avec une taille de police de 20. N’hésitez pas à changer le nom de la police ou la taille pour correspondre à votre style de marque.

```java
Font font = new Font("Arial", 20.0f);
```

### Étape 5 : Créer un pinceau solide pour le filigrane
Un pinceau solide donne à votre filigrane sa couleur et son opacité. Nous fixerons l’alpha à 50 (sur 255) pour un gris semi‑transparent.

```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```

Ici, `Color.fromArgb(50, 128, 128, 128)` crée une couleur grise avec une opacité de 50 % – parfait pour une signature discrète.

### Étape 6 : Définir l’alignement du texte pour votre filigrane
Pour que le filigrane apparaisse exactement au centre de l’image, nous configurerons les options d’alignement du texte.

```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
sf.setLineAlignment(StringAlignment.Center);
```

### Étape 7 : Dessiner le filigrane avec **java graphics drawstring**
Passons maintenant à la partie excitante. Avec le contexte graphique prêt, nous dessinerons le texte du filigrane sur l’image en utilisant `java graphics drawstring`.

```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, 0, psdImage.getWidth(), psdImage.getHeight()), sf);
```

Remplacez `"Some watermark text"` par le texte réel que vous souhaitez voir apparaître sur votre PSD.

### Étape 8 : **Save PSD as PNG** – **export psd png**
Le filigrane étant en place, nous allons **save psd png** (c’est‑à‑dire exporter le PSD en PNG) afin que le résultat puisse être visualisé dans n’importe quel navigateur ou visualiseur d’images.

```java
psdImage.save(dataDir + "AddWatermark_output.png", new PngOptions());
```

L’exécution de cette ligne crée un nouveau fichier PNG contenant votre filigrane.

## Problèmes courants et solutions
- **Filigrane invisible ?** Vérifiez la valeur alpha dans `Color.fromArgb()` ; une valeur plus basse rend le filigrane plus transparent.  
- **Dimensions incorrectes ?** Assurez‑vous d’utiliser `psdImage.getWidth()` et `psdImage.getHeight()` pour le rectangle afin que le texte s’ajuste à la taille de l’image.  
- **Exceptions de licence ?** Une licence d’évaluation temporaire fonctionne pour les tests, mais une licence complète est requise en production.

## Foire aux questions

**Q : Puis‑je personnaliser le texte du filigrane ?**  
R : Absolument ! Remplacez simplement la chaîne dans la méthode `drawString` par le texte souhaité.

**Q : Et si je veux une police différente ?**  
R : Changez l’instanciation du `Font` par n’importe quelle police installée, par ex. `new Font("Times New Roman", 24.0f)`.

**Q : Existe‑t‑il un moyen d’ajuster l’opacité ?**  
R : Oui—modifiez le premier paramètre de `Color.fromArgb(alpha, r, g, b)`. Des valeurs `alpha` plus faibles augmentent la transparence.

**Q : Puis‑je utiliser d’autres formats d’image que le PNG ?**  
R : Bien sûr. Remplacez `new PngOptions()` par `new JpegOptions()` ou `new BmpOptions()` pour **save psd png** dans un format différent.

**Q : Où puis‑je trouver plus d’aide ?**  
R : Pour des questions détaillées, visitez les [forums Aspose](https://forum.aspose.com/c/psd/34) ou consultez leur [documentation](https://reference.aspose.com/psd/java/).

## Conclusion
Vous avez maintenant appris à **create image watermark** dans un fichier PSD à l’aide d’Aspose.PSD pour Java. Cette technique sécurise non seulement votre contenu mais renforce également la présence de votre marque sur tous vos actifs visuels. Expérimentez avec différentes polices, couleurs et niveaux d’opacité pour correspondre à votre style, et rappelez‑vous que vous pouvez **save psd png** ou **export psd png** dans n’importe quel format dont vous avez besoin.

---

**Dernière mise à jour :** 2026-03-07  
**Testé avec :** Aspose.PSD pour Java 24.11  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}