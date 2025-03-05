---
title: Ajuster le contraste d'une image avec Aspose.PSD pour Java
linktitle: Ajuster le contraste d'une image
second_title: API Java Aspose.PSD
description: Explorez le monde du réglage du contraste des images en Java avec Aspose.PSD. Suivez notre guide étape par étape pour une manipulation transparente des images.
type: docs
weight: 22
url: /fr/java/advanced-techniques/adjust-contrast/
---
## Introduction

Dans le domaine du traitement d'images avec Java, Aspose.PSD s'impose comme un outil puissant. Parmi sa myriade de fonctionnalités, le réglage du contraste de l’image est une exigence courante. Ce didacticiel vous guidera tout au long du processus de réglage du contraste de l'image à l'aide d'Aspose.PSD pour Java. Que vous soyez un développeur chevronné ou débutant, ce guide vous aidera à maîtriser cet aspect essentiel de la manipulation d'images.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

- Compréhension de base de la programmation Java.
-  Aspose.PSD pour la bibliothèque Java installée. Vous pouvez le télécharger[ici](https://releases.aspose.com/psd/java/).

## Importer des packages

Pour commencer, vous devez importer les packages nécessaires dans votre projet Java. Ajoutez les lignes suivantes à votre code :

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Étape 1 : Charger l'image

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Charger une image existante dans une instance de la classe RasterImage
Image image = Image.load(sourceFile);
```

 Dans cette étape, nous chargeons l'exemple d'image ("sample.psd") à l'aide du`Image.load` méthode.

## Étape 2 : Caster vers RasterImage et mettre en cache les données

```java
// Convertir l'objet de l'image en RasterImage
RasterImage rasterImage = (RasterImage)image;

// Vérifiez si RasterImage est mis en cache et mettez en cache RasterImage pour de meilleures performances
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Ici, nous castons le générique`Image` s'opposer à un`RasterImage` pour un traitement spécifique. La mise en cache des données d'image améliore les performances.

## Étape 3 : Ajuster le contraste

```java
// Ajuster le contraste
rasterImage.adjustContrast(50);
```

 Le`adjustContrast`La méthode est utilisée pour modifier le contraste de l’image. Dans cet exemple, le contraste est augmenté de 50 %.

## Étape 4 : Créez des TiffOptions et enregistrez

```java
// Créer une instance de TiffOptions pour l'image résultante
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Enregistrez l'image résultante au format TIFF
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

 Ici, nous installons`TiffOptions` pour l'image de sortie, en spécifiant le format et d'autres propriétés. L'image finale est ensuite enregistrée dans un fichier TIFF.

## Conclusion

Félicitations! Vous avez réussi à ajuster le contraste d'une image à l'aide d'Aspose.PSD pour Java. Ce tutoriel a couvert les étapes essentielles, de l'importation des packages à la sauvegarde de l'image traitée.

## FAQ

### Q1 : Aspose.PSD est-il compatible avec différents formats d'image ?

A1 : Oui, Aspose.PSD prend en charge différents formats d'image, offrant ainsi de la flexibilité à vos projets.

### Q2 : Comment puis-je obtenir une licence temporaire pour Aspose.PSD ?

 A2 : Vous pouvez obtenir une licence temporaire[ici](https://purchase.aspose.com/temporary-license/).

### Q3 : Où puis-je trouver la documentation Aspose.PSD ?

A3 : La documentation est disponible[ici](https://reference.aspose.com/psd/java/).

### Q4 : Quelles options de support sont disponibles pour Aspose.PSD ?

 A4 : Pour obtenir de l'aide, visitez le[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q5 : Puis-je acheter Aspose.PSD ?

 A5 : Oui, vous pouvez acheter Aspose.PSD[ici](https://purchase.aspose.com/buy).