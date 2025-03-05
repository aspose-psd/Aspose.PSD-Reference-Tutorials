---
title: Implémentation du réglage de la luminosité dans Aspose.PSD pour .NET
linktitle: Implémentation du réglage de la luminosité
second_title: API Aspose.PSD.NET
description: Découvrez la puissance d'Aspose.PSD pour .NET pour ajuster la luminosité de l'image. Suivez notre guide étape par étape pour une mise en œuvre transparente.
type: docs
weight: 10
url: /fr/net/image-adjustment/brightness-adjustment/
---
## Introduction

L'amélioration et l'ajustement des attributs d'image sont une exigence courante dans diverses applications, et Aspose.PSD pour .NET fournit une solution puissante pour manipuler les fichiers PSD de manière transparente. L'une de ces manipulations est le réglage de la luminosité, qui vous permet de modifier la luminosité d'une image sans effort.

Dans ce didacticiel, nous passerons en revue le processus de mise en œuvre du réglage de la luminosité à l'aide d'Aspose.PSD pour .NET. Suivez les étapes ci-dessous pour bien comprendre comment intégrer les réglages de luminosité dans vos fichiers PSD.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

-  Bibliothèque Aspose.PSD pour .NET : téléchargez et installez la bibliothèque Aspose.PSD pour .NET à partir du[lien de téléchargement](https://releases.aspose.com/psd/net/).

-  Répertoire de documents : configurez un répertoire pour stocker vos fichiers PSD et mettez à jour le`dataDir` variable dans l'extrait de code fourni avec le chemin d'accès à votre répertoire de documents.

## Importer des espaces de noms

Dans votre projet .NET, incluez les espaces de noms nécessaires pour accéder à la fonctionnalité Aspose.PSD. Ajoutez les espaces de noms suivants à votre code :

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

Maintenant, décomposons l'exemple en plusieurs étapes :

## Étape 1 : Chargez le fichier PSD

```csharp
// Le chemin d'accès au répertoire des documents.
string dataDir = "Your Document Directory";
string sourceFile = dataDir + @"sample.psd";

// Chargez le fichier PSD à l'aide d'Aspose.PSD
using (var image = (PsdImage)Image.Load(sourceFile))
{
    // Votre code pour les étapes suivantes va ici
}
```

## Étape 2 : obtenir une image raster

```csharp
// Obtenez l'image raster à partir du fichier PSD chargé
RasterCachedImage rasterImage = image;
```

## Étape 3 : Ajuster la luminosité

```csharp
// Réglez la valeur de luminosité. Les valeurs de luminosité acceptées sont comprises dans la plage [-255, 255].
rasterImage.AdjustBrightness(-50);
```

## Étape 4 : Enregistrez l'image modifiée

```csharp
// Enregistrez l'image modifiée avec la luminosité ajustée
string destName = dataDir + @"AdjustBrightness_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
rasterImage.Save(destName, tiffOptions);
```

Maintenant que nous avons divisé l'exemple en étapes gérables, vous pouvez intégrer de manière transparente le réglage de la luminosité dans votre projet .NET à l'aide d'Aspose.PSD.

## Conclusion

Aspose.PSD pour .NET simplifie le processus de mise en œuvre des ajustements de luminosité dans les fichiers PSD. En suivant le guide étape par étape fourni ci-dessus, vous pouvez sans effort améliorer l'attrait visuel de vos images. Expérimentez avec différentes valeurs de luminosité pour obtenir les résultats souhaités.

## FAQ

### Q1 : Où puis-je trouver la documentation d’Aspose.PSD pour .NET ?

 A1 : La documentation est disponible[ici](https://reference.aspose.com/psd/net/).

### Q2 : Comment puis-je télécharger la bibliothèque Aspose.PSD pour .NET ?

 A2 : Vous pouvez télécharger la bibliothèque à partir du[page de sortie](https://releases.aspose.com/psd/net/).

### Q3 : Existe-t-il un essai gratuit disponible pour Aspose.PSD pour .NET ?

 A3 : Oui, vous pouvez accéder à l'essai gratuit[ici](https://releases.aspose.com/).

### Q4 : Où puis-je obtenir de l'assistance pour Aspose.PSD pour .NET ?

 A4 : Pour obtenir de l'aide, visitez le[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q5 : Comment puis-je obtenir une licence temporaire pour Aspose.PSD pour .NET ?

 A5 : Vous pouvez acquérir une licence temporaire[ici](https://purchase.aspose.com/temporary-license/).