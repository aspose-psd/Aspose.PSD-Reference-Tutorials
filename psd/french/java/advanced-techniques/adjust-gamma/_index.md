---
title: Ajuster le gamma d'une image avec Aspose.PSD pour Java
linktitle: Ajuster le gamma d'une image
second_title: API Java Aspose.PSD
description: Apprenez à ajuster le gamma de l'image sans effort à l'aide d'Aspose.PSD pour Java. Suivez notre guide étape par étape pour des résultats optimaux.
type: docs
weight: 23
url: /fr/java/advanced-techniques/adjust-gamma/
---
## Introduction

Dans le domaine du traitement d’images, l’ajustement du gamma d’une image est une étape cruciale pour améliorer son attrait visuel. Aspose.PSD pour Java offre une solution puissante aux développeurs Java pour manipuler sans effort le gamma des images. Dans ce didacticiel, nous explorerons comment ajuster le gamma à l'aide d'Aspose.PSD, en décomposant chaque étape pour garantir une mise en œuvre transparente.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous d'avoir configuré les conditions préalables suivantes :

1. Environnement de développement Java : assurez-vous qu'un environnement de développement Java est installé sur votre système.
2.  Bibliothèque Aspose.PSD : téléchargez et intégrez la bibliothèque Aspose.PSD dans votre projet Java. Vous pouvez trouver les ressources nécessaires dans le[documentation](https://reference.aspose.com/psd/java/).
3. Exemple d'image : préparez un exemple d'image PSD que vous utiliserez pour appliquer l'ajustement gamma.

## Importer des packages

Pour lancer le processus, importez les packages requis dans votre projet Java. Cela ouvre la voie à une utilisation transparente des fonctionnalités d’Aspose.PSD.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Étape 1 : Charger l'image

 Commencez par charger l’exemple d’image PSD dans une instance du`RasterImage` classe. C’est la base des ajustements gamma ultérieurs.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Charger une image existante dans une instance de la classe RasterImage
Image image = Image.load(sourceFile);

// Convertir l'objet de l'image en RasterImage
RasterImage rasterImage = (RasterImage)image;

// Vérifiez si RasterImage est mis en cache pour de meilleures performances
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## Étape 2 : Ajuster le gamma

 Maintenant, ajustez le gamma de l'image chargée à l'aide du`adjustGamma` méthode. Ajustez les valeurs gamma en fonction de vos besoins.

```java
// Ajuster le gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## Étape 3 : Créer des TiffOptions

 Créer une instance de`TiffOptions` pour l'image résultante. Définissez diverses propriétés, telles que les bits par échantillon et les options photométriques, pour adapter la sortie à vos spécifications.

```java
// Créer une instance de TiffOptions pour l'image résultante
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## Étape 4 : Enregistrez l'image résultante

 Enregistrez l'image manipulée au format TIFF en utilisant le format précédemment défini`TiffOptions`.

```java
// Enregistrez l'image résultante au format TIFF
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Conclusion

Félicitations! Vous avez réussi à ajuster le gamma d'une image à l'aide d'Aspose.PSD pour Java. Ce processus permet aux développeurs d'améliorer la qualité de l'image sans effort, contribuant ainsi à une expérience utilisateur visuellement attrayante.

## FAQ

### Q1 : Où puis-je trouver la documentation Aspose.PSD ?

 A1 : Vous pouvez accéder à la documentation à l'adresse[https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### Q2 : Comment télécharger Aspose.PSD pour Java ?

 A2 : Téléchargez la bibliothèque depuis[https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### Q3 : Où puis-je acheter Aspose.PSD ?

 A3 : Visite[https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) pour acheter Aspose.PSD.

### Q4 : Existe-t-il un essai gratuit ?

 A4 : Oui, vous pouvez explorer un essai gratuit sur[https://releases.aspose.com/](https://releases.aspose.com/).

### Q5 : Où puis-je demander de l'aide pour Aspose.PSD ?

 A5 : Pour obtenir de l'aide, visitez le forum Aspose.PSD à l'adresse[https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).