---
title: Implémentation de l'ajustement gamma dans Aspose.PSD pour .NET
linktitle: Implémentation de l'ajustement gamma
second_title: API Aspose.PSD.NET
description: Explorez la puissance d'Aspose.PSD pour .NET avec notre guide étape par étape sur la mise en œuvre de l'ajustement gamma. Ajustez facilement la luminosité et le contraste de l’image.
weight: 12
url: /fr/net/image-adjustment/gamma-adjustment/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Implémentation de l'ajustement gamma dans Aspose.PSD pour .NET

## Introduction

Bienvenue dans ce guide complet sur la mise en œuvre de l'ajustement gamma dans Aspose.PSD pour .NET ! Le réglage gamma est une technique de traitement d'image cruciale qui vous permet d'affiner la luminosité et le contraste d'une image. Dans ce didacticiel, nous vous guiderons tout au long du processus en utilisant la puissante bibliothèque Aspose.PSD pour .NET.

## Conditions préalables

Avant de vous lancer dans la mise en œuvre, assurez-vous d’avoir les conditions préalables suivantes en place :

-  Bibliothèque Aspose.PSD pour .NET : assurez-vous que la bibliothèque Aspose.PSD pour .NET est installée. Vous pouvez le télécharger[ici](https://releases.aspose.com/psd/net/).

- .NET Framework : ce didacticiel suppose que vous possédez une compréhension de base du développement .NET et que .NET Framework est installé.

- Environnement de développement intégré (IDE) : choisissez votre IDE préféré pour le développement .NET, tel que Visual Studio.

## Importer des espaces de noms

Dans votre projet .NET, commencez par importer les espaces de noms nécessaires pour travailler avec Aspose.PSD :

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## Étape 1 : Configurez votre projet

Créez un nouveau projet .NET dans l'EDI de votre choix. Assurez-vous d'ajouter des références à la bibliothèque Aspose.PSD.

## Étape 2 : définir le répertoire des documents

```csharp
string dataDir = "Your Document Directory";
```

## Étape 3 : Charger l'image

```csharp
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    // Des étapes supplémentaires seront effectuées à l’intérieur de ce bloc using.
}
```

## Étape 4 : Caster vers RasterImage et mettre en cache les données

```csharp
RasterImage rasterImage = (RasterImage)image;
if (!rasterImage.IsCached)
{
    rasterImage.CacheData();
}
```

## Étape 5 : Ajuster le gamma

```csharp
rasterImage.AdjustGamma(2.2f, 2.2f, 2.2f);
```

## Étape 6 : Créez des TiffOptions et enregistrez

```csharp
string destName = dataDir + @"AdjustGamma_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
```

## Conclusion

Félicitations! Vous avez implémenté avec succès l'ajustement gamma à l'aide d'Aspose.PSD pour .NET. Cette puissante bibliothèque offre des fonctionnalités robustes pour le traitement des images, ce qui en fait un outil précieux pour les développeurs .NET.

## FAQ

### Q1 : Où puis-je trouver la documentation Aspose.PSD ?

 A1 : Vous pouvez vous référer à la documentation[ici](https://reference.aspose.com/psd/net/).

### Q2 : Comment télécharger Aspose.PSD pour .NET ?

 A2 : Vous pouvez télécharger la bibliothèque[ici](https://releases.aspose.com/psd/net/).

### Q3 : Existe-t-il un essai gratuit disponible ?

 A3 : Oui, vous pouvez bénéficier d'un essai gratuit[ici](https://releases.aspose.com/).

### Q4 : Où puis-je obtenir de l'aide pour Aspose.PSD ?

 A4 : Vous pouvez visiter le forum d'assistance[ici](https://forum.aspose.com/c/psd/34).

### Q5 : Ai-je besoin d’une licence temporaire ?

 A5 : Si nécessaire, vous pouvez obtenir un permis temporaire[ici](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
