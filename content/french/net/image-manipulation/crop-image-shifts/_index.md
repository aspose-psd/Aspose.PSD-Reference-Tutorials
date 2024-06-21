---
title: Recadrage d'images par décalages dans Aspose.PSD pour .NET
linktitle: Recadrage des images par décalages
second_title: API Aspose.PSD.NET
description: Apprenez à recadrer des images sans effort à l'aide d'Aspose.PSD pour .NET. Suivez notre guide étape par étape pour des réglages précis de l’image.
type: docs
weight: 12
url: /fr/net/image-manipulation/crop-image-shifts/
---
## Introduction

Dans le domaine du développement .NET, Aspose.PSD se distingue comme une puissante boîte à outils pour les tâches de traitement d'images. Une de ses caractéristiques notables est la possibilité de recadrer les images avec précision, grâce à la fonctionnalité « Recadrage par Shifts ». Dans ce guide étape par étape, nous vous guiderons tout au long du processus de recadrage d'images de manière transparente à l'aide d'Aspose.PSD pour .NET.

## Conditions préalables

Avant de vous lancer dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

-  Aspose.PSD pour la bibliothèque .NET : assurez-vous que la bibliothèque est installée. Sinon, vous pouvez le télécharger depuis le[page de sortie](https://releases.aspose.com/psd/net/).

- Environnement .NET : assurez-vous d'avoir un environnement de développement .NET configuré sur votre ordinateur.

- Exemple d'image : préparez un exemple d'image au format PSD avec lequel vous souhaitez travailler.

## Importer des espaces de noms

Commencez par importer les espaces de noms nécessaires dans votre projet .NET. Ces espaces de noms donnent accès aux classes et méthodes Aspose.PSD requises pour le recadrage d’images.

```csharp
using Aspose.PSD.ImageOptions;
```

## Étape 1 : définissez votre répertoire de documents

Définissez le chemin d'accès à votre répertoire de documents où se trouveront les fichiers source et de destination.

```csharp
string dataDir = "Your Document Directory";
```

## Étape 2 : Charger l'image source

Chargez l'image PSD que vous souhaitez recadrer. Assurez-vous de remplacer "sample.psd" par le nom de votre fichier source.

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"CroppingByShifts_out.jpg";
```

## Étape 3 : mettre en cache les données d'image pour de meilleures performances

Avant le recadrage, il est conseillé de mettre en cache les données de l'image pour améliorer les performances.

```csharp
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
```

## Étape 4 : Définir les valeurs de décalage pour le recadrage

Spécifiez les valeurs de décalage pour les côtés gauche, droit, supérieur et inférieur de l'image. Ajustez ces valeurs en fonction de vos besoins de recadrage.

```csharp
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

## Étape 5 : appliquer le recadrage et enregistrer les résultats

 Utiliser le`Crop` méthode pour appliquer les décalages spécifiés et enregistrer l’image recadrée dans le fichier de destination.

```csharp
rasterImage.Crop(leftShift, rightShift, topShift, bottomShift);
rasterImage.Save(destName, new JpegOptions());
}
```

## Conclusion

Toutes nos félicitations! Vous avez appris avec succès comment recadrer des images par décalage à l'aide d'Aspose.PSD pour .NET. Cette fonctionnalité puissante vous offre la précision et le contrôle nécessaires à diverses tâches de traitement d’image.

## FAQ

### Q1 : Puis-je recadrer des images de différents formats, pas seulement PSD ?

A1 : Oui, Aspose.PSD prend en charge différents formats d'image, vous permettant de recadrer des images dans des formats tels que JPEG, PNG, etc.

### Q2 : Existe-t-il une version d'essai disponible avant d'acheter Aspose.PSD pour .NET ?

 A2 : Certainement ! Vous pouvez explorer la boîte à outils avec un essai gratuit disponible[ici](https://releases.aspose.com/).

### Q3 : Comment puis-je obtenir une licence temporaire pour Aspose.PSD pour .NET ?

 A3 : Vous pouvez acquérir une licence temporaire à des fins de test.[ici](https://purchase.aspose.com/temporary-license/).

### Q4 : Où puis-je trouver une assistance supplémentaire et des discussions liées à Aspose.PSD ?

 A4 : Visitez le[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour du soutien et des discussions engageantes.

### Q5 : Puis-je acheter Aspose.PSD pour .NET directement depuis le site Web ?

 A5 : Oui, vous pouvez acheter la bibliothèque en toute sécurité sur le[page d'achat](https://purchase.aspose.com/buy).
