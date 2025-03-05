---
title: Ajuster la luminosité d'une image avec Aspose.PSD pour Java
linktitle: Ajuster la luminosité d'une image
second_title: API Java Aspose.PSD
description: Améliorez la luminosité de l'image en Java avec Aspose.PSD. Guide étape par étape pour ajuster la luminosité de l’image par programmation.
type: docs
weight: 21
url: /fr/java/advanced-techniques/adjust-brightness/
---
## Introduction

L'amélioration des images est une exigence courante dans la conception graphique et la photographie numérique. Aspose.PSD pour Java fournit une solution puissante pour ajuster la luminosité de l'image par programme. Dans ce didacticiel, nous explorerons comment utiliser la bibliothèque Aspose.PSD pour Java pour ajuster la luminosité d'une image, étape par étape.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous d'avoir les prérequis suivants :

-  Aspose.PSD pour la bibliothèque Java : téléchargez et installez la bibliothèque à partir du[Documentation Aspose.PSD pour Java](https://reference.aspose.com/psd/java/).

## Importer des packages

Pour commencer, importez les packages nécessaires dans votre projet Java. Dans cet exemple, nous utiliserons ce qui suit :

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Maintenant, décomposons le processus de réglage de la luminosité d'une image en étapes simples :

## Étape 1 : Charger l'image

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Charger une image existante dans une instance de la classe RasterImage
Image image = Image.load(sourceFile);
// Convertir l'objet de l'image en RasterImage
RasterImage rasterImage = (RasterImage) image;

// Vérifiez si RasterImage est mis en cache et mettez en cache RasterImage pour de meilleures performances
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Dans cette étape, nous chargeons l'image cible et la diffusons vers un`RasterImage` pour un traitement ultérieur.

## Étape 2 : Ajuster la luminosité

```java
// Ajuster la luminosité
rasterImage.adjustBrightness(-50);
```

 Ici, nous utilisons le`adjustBrightness`méthode pour modifier la luminosité de l’image. Dans cet exemple, nous réduisons la luminosité de 50 unités, mais vous pouvez personnaliser cette valeur en fonction de vos besoins.

## Étape 3 : définir les options Tiff

```java
int[] ushort = {8, 8, 8};
// Créer une instance de TiffOptions pour l'image résultante
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

 Configurez le`TiffOptions` pour enregistrer l’image ajustée. Ajustez le`bitsPerSample` et`photometric` propriétés en fonction de vos besoins spécifiques.

## Étape 4 : Enregistrez l'image résultante

```java
// Enregistrez l'image résultante
rasterImage.save(destName, tiffOptions);
```

 Enfin, enregistrez l'image modifiée en utilisant le spécifié`TiffOptions`.

## Conclusion

Le réglage de la luminosité d'une image par programmation est facilité avec Aspose.PSD pour Java. Ce didacticiel a fourni un guide complet sur la mise en œuvre de cette fonctionnalité dans vos applications Java.

## FAQ

### Q1 : Puis-je régler la luminosité dans d’autres formats d’image que PSD ?

A1 : Oui, Aspose.PSD pour Java prend en charge divers formats d'image tels que JPEG, PNG et TIFF.

### Q2 : Comment puis-je gérer les erreurs pendant le processus de réglage de l'image ?

A2 : Vous pouvez implémenter la gestion des erreurs à l'aide de blocs try-catch pour gérer les exceptions qui peuvent survenir.

### Q3 : Y a-t-il une limite à la plage de réglage de la luminosité ?

A3 : La plage de réglage dépend du contenu et du format de l'image, mais Aspose.PSD offre une flexibilité de personnalisation.

### Q4 : Puis-je utiliser Aspose.PSD pour Java dans des projets commerciaux ?

 A4 : Oui, Aspose.PSD pour Java est une bibliothèque commerciale et vous pouvez obtenir une licence auprès de[ici](https://purchase.aspose.com/buy).

### Q5 : Existe-t-il un essai gratuit disponible pour Aspose.PSD pour Java ?

 A5 : Oui, vous pouvez explorer la bibliothèque avec un essai gratuit à partir de[ici](https://releases.aspose.com/).