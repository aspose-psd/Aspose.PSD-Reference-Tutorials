---
title: Rotation d'une image selon un angle spécifique dans Aspose.PSD pour .NET
linktitle: Rotation d'une image selon un angle spécifique
second_title: API Aspose.PSD.NET
description: Explorez la puissance d'Aspose.PSD pour .NET. Faites pivoter les images sans effort selon des angles spécifiques. Téléchargez la bibliothèque et commencez à manipuler les images de manière transparente.
type: docs
weight: 16
url: /fr/net/image-manipulation/rotate-image-specific-angle/
---
Si vous plongez dans le monde de la manipulation d'images avec .NET, Aspose.PSD fournit une solution puissante. Dans ce didacticiel, nous vous guiderons tout au long du processus de rotation d'une image selon un angle spécifique à l'aide d'Aspose.PSD. Avant de plonger dans les étapes, préparons le terrain avec une introduction.

## Introduction

Aspose.PSD pour .NET est une bibliothèque polyvalente qui permet aux développeurs de travailler de manière transparente avec les formats d'images PSD et raster. L'une de ses principales caractéristiques est la possibilité de faire pivoter les images selon des angles précis, offrant ainsi une flexibilité dans la manipulation des images. Ce didacticiel vous guidera à travers les étapes pour faire pivoter une image selon un angle spécifique à l'aide d'Aspose.PSD pour .NET.

## Conditions préalables

Avant de nous lancer dans cette aventure, assurez-vous d’avoir les conditions préalables suivantes en place :

-  Aspose.PSD pour la bibliothèque .NET : téléchargez et installez la bibliothèque à partir du[page de téléchargement](https://releases.aspose.com/psd/net/).
- Répertoire de documents : configurez un répertoire pour stocker vos fichiers source et de sortie.

## Importer des espaces de noms

Pour commencer, importez les espaces de noms nécessaires dans votre projet .NET :

```csharp
using Aspose.PSD.ImageOptions;
```

Maintenant, décomposons l'exemple en plusieurs étapes dans un format de guide étape par étape.

## Étape 1 : définissez votre répertoire de documents

```csharp
string dataDir = "Your Document Directory";
```

 Remplacer`"Your Document Directory"` avec le chemin d'accès au répertoire dans lequel vous stockez vos fichiers source et de sortie.

## Étape 2 : Charger l'image

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"RotatingImageOnSpecificAngle_out.jpg";

using (RasterImage image = (RasterImage)Image.Load(sourceFile))
{
    // Des étapes supplémentaires seront insérées ici
}
```

 Chargez l'image que vous souhaitez faire pivoter dans une instance de`RasterImage`.

## Étape 3 : mettre en cache les données d'image

```csharp
if (!image.IsCached)
{
    image.CacheData();
}
```

Mettez en cache les données d’image pour de meilleures performances lors de la rotation.

## Étape 4 : faire pivoter l'image

```csharp
image.Rotate(20f, true, Color.Red);
```

Faites pivoter l'image de 20 degrés, en conservant une taille proportionnelle et en utilisant un arrière-plan rouge.

## Étape 5 : Enregistrez le résultat

```csharp
image.Save(destName, new JpegOptions());
```

Enregistrez l'image pivotée avec les options spécifiées (dans ce cas, au format JPEG).

## Conclusion

 Toutes nos félicitations! Vous avez réussi à faire pivoter une image selon un angle spécifique à l'aide d'Aspose.PSD pour .NET. Cette bibliothèque fournit un ensemble robuste d'outils pour la manipulation d'images, et ce didacticiel n'est que la pointe de l'iceberg. Explore le[Documentation](https://reference.aspose.com/psd/net/) pour plus de fonctionnalités et d’options.

## FAQ

### Q1 : Puis-je faire pivoter les images selon des angles autres que 20 degrés ?

 A1 : Oui, vous pouvez personnaliser le paramètre d'angle dans le`image.Rotate` méthode à n’importe quelle valeur souhaitée.

### Q2 : Aspose.PSD prend-il en charge d'autres formats d'image que JPEG ?

A2 : Absolument ! Aspose.PSD prend en charge un large éventail de formats, notamment PNG, GIF, BMP et TIFF.

### Q3 : La mise en cache des données d’image est-elle nécessaire avant la rotation ?

A3 : Bien que cela ne soit pas obligatoire, la mise en cache des données peut améliorer considérablement les performances, en particulier pour les images plus grandes.

### Q4 : Où puis-je obtenir de l'aide pour les requêtes liées à Aspose.PSD ?

 A4 : Visitez le[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour le soutien et les discussions de la communauté.

### Q5 : Puis-je essayer Aspose.PSD avant d’acheter ?

 A5 : Certainement ! Prenez votre[essai gratuit](https://releases.aspose.com/) pour explorer les capacités de la bibliothèque.