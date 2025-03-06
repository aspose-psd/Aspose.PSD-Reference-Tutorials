---
title: Ajout d'effets de trait aux calques dans Aspose.PSD pour .NET
linktitle: Ajout d'effets de trait aux calques
second_title: API Aspose.PSD.NET
description: Améliorez l’esthétique de l’image avec Aspose.PSD pour .NET. Apprenez à ajouter des effets de trait étape par étape. Téléchargez, achetez ou essayez l'essai gratuit maintenant.
weight: 10
url: /fr/net/layer-effects/adding-stroke-effects/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajout d'effets de trait aux calques dans Aspose.PSD pour .NET

## Introduction

Bienvenue dans ce didacticiel étape par étape sur l'ajout d'effets de trait aux calques dans Aspose.PSD pour .NET. Améliorer l'attrait visuel de vos images est un jeu d'enfant grâce à l'effet de trait, et Aspose.PSD le rend transparent pour les développeurs .NET. Dans ce guide, nous vous guiderons tout au long du processus, en fournissant des étapes claires et des exemples pour vous aider à maîtriser cette fonctionnalité puissante.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

- Aspose.PSD pour .NET : téléchargez et installez la bibliothèque Aspose.PSD à partir du[site web](https://releases.aspose.com/psd/net/).

- Répertoire du document : préparez un répertoire contenant le document PSD auquel vous souhaitez appliquer des effets de trait.

- Répertoire de sortie : disposez d'un répertoire séparé pour stocker les images de sortie avec des effets de trait.

- Visual Studio : assurez-vous que Visual Studio ou tout autre environnement de développement .NET préféré est configuré.

## Importer des espaces de noms

Dans votre projet .NET, incluez les espaces de noms nécessaires pour exploiter la fonctionnalité Aspose.PSD :

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using Aspose.PSD.ImageOptions;
```

## Étape 1 : Charger le document PSD

```csharp
string srcFile = Path.Combine(SourceDir, "AddStrokeEffect.psd");
string outputFilePng = Path.Combine(OutputDir, "AddStrokeEffect.png");

using (var psdImage = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    // Votre code pour charger le document PSD va ici
}
```

## Étape 2 : ajouter un effet de trait de couleur

```csharp
// Ajoute un remplissage de couleur, à la position À l'intérieur
strokeEffect = psdImage.Layers[1].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Inside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## Étape 3 : Position extérieure

```csharp
// Ajoute un remplissage de couleur, à la position À l'extérieur
strokeEffect = psdImage.Layers[2].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Outside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## Étape 4 : Position centrale

```csharp
// Ajoute un remplissage de couleur, à la position Centre
strokeEffect = psdImage.Layers[3].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Center;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

Répétez des étapes similaires pour les remplissages Dégradé et Motif, en ajustant les paramètres en conséquence.

## Conclusion

Félicitations! Vous avez appris avec succès comment ajouter des effets de trait aux calques à l'aide d'Aspose.PSD pour .NET. Expérimentez avec différents paramètres pour obtenir l’impact visuel souhaité dans vos images.

## FAQ

### Q1 : Puis-je appliquer des effets de trait uniquement à des calques spécifiques ?

A1 : Oui, vous pouvez cibler des couches spécifiques en ajustant l'index des couches dans le code.

### Q2 : Aspose.PSD est-il compatible avec le dernier framework .NET ?

A2 : Absolument ! Aspose.PSD est conçu pour s'intégrer de manière transparente aux derniers frameworks .NET.

### Q3 : Comment puis-je personnaliser la couleur du trait ?

 A3 : Modifiez simplement le`Color` propriété dans le code pour obtenir la couleur de trait souhaitée.

### Q4 : Aspose.PSD prend-il en charge le traitement par lots pour plusieurs fichiers PSD ?

A4 : Oui, vous pouvez parcourir plusieurs fichiers PSD et appliquer l'effet de trait en utilisant une approche similaire.

### Q5 : Puis-je utiliser la version d'essai avant d'acheter Aspose.PSD ?

 A5 : Certainement ! Prenez le[essai gratuit](https://releases.aspose.com/) pour explorer les capacités d'Aspose.PSD avant de faire un achat.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
