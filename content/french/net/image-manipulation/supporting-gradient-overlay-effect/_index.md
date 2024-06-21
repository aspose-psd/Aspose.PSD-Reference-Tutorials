---
title: Prise en charge de l'effet de superposition de dégradé dans Aspose.PSD pour .NET
linktitle: Prise en charge de l'effet de superposition de dégradé
second_title: API Aspose.PSD.NET
description: Améliorez les graphiques dans .NET avec Aspose.PSD. Ce didacticiel vous guide dans la prise en charge des effets de superposition de dégradé.
type: docs
weight: 18
url: /fr/net/image-manipulation/supporting-gradient-overlay-effect/
---
## Introduction

Bienvenue dans ce didacticiel complet sur la prise en charge de l'effet de superposition de dégradé dans Aspose.PSD pour .NET ! Si vous souhaitez améliorer les capacités graphiques de votre application .NET, ce guide étape par étape est là pour vous aider. Nous approfondirons les subtilités de la création et de la modification de l'effet de superposition de dégradé dans un calque à l'aide d'Aspose.PSD, une bibliothèque puissante qui simplifie le traitement des images.

## Conditions préalables

Avant de vous lancer dans ce voyage, assurez-vous d'avoir les éléments suivants :

- Une compréhension de base de la programmation C# et .NET.
-  Aspose.PSD pour .NET installé. Vous pouvez le télécharger[ici](https://releases.aspose.com/psd/net/).
- Un environnement de développement configuré avec votre IDE préféré.

## Importer des espaces de noms

Pour commencer, importons les espaces de noms nécessaires dans votre code C# :

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
```

Maintenant que nous avons couvert les bases, décomposons chaque étape en détail :

## Étape 1 : Charger l'image PSD

```csharp
// Le chemin d'accès au répertoire des documents.
string SourceDir = "Your Document Directory";
string OutputDir = "Your Output Directory";

string sourceFilePath = Path.Combine(SourceDir, "psdnet256.psd");
string outputFilePath = Path.Combine(OutputDir, "psdnet256.psd_output.psd");

using (var psdImage = (PsdImage)Image.Load(sourceFilePath, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    // Le code pour les étapes suivantes va ici...
}
```

## Étape 2 : accéder aux options de fusion des calques

```csharp
BlendingOptions layerBlendOptions = psdImage.Layers[1].BlendingOptions;
```

## Étape 3 : Rechercher ou créer un effet de superposition de dégradé

```csharp
GradientOverlayEffect gradientOverlayEffect = null;

foreach (ILayerEffect effect in layerBlendOptions.Effects)
{
    gradientOverlayEffect = effect as GradientOverlayEffect;
    if (gradientOverlayEffect != null)
    {
        break;
    }
}

if (gradientOverlayEffect == null)
{
    gradientOverlayEffect = layerBlendOptions.AddGradientOverlay();
}
```

## Étape 4 : configurer l'effet de superposition de dégradé

```csharp
gradientOverlayEffect.Opacity = 200;
gradientOverlayEffect.BlendMode = BlendMode.Hue;

GradientFillSettings settings = gradientOverlayEffect.Settings;

settings.ColorPoints = new IGradientColorPoint[]
{
    new GradientColorPoint(Color.GreenYellow, 0, 50),
    new GradientColorPoint(Color.BlueViolet, 4096, 50),
};

settings.Angle = 80;
settings.Scale = 150;
settings.GradientType = GradientType.Linear;

settings.TransparencyPoints[0].Opacity = 100;
settings.TransparencyPoints[1].Opacity = 100;
```

## Étape 5 : Enregistrez l'image modifiée

```csharp
psdImage.Save(outputFilePath);
```

C'est ça! Vous avez ajouté avec succès un effet de superposition de dégradé à un calque à l'aide d'Aspose.PSD pour .NET.

## Conclusion

Dans ce didacticiel, nous avons exploré le processus de prise en charge de l'effet de superposition de dégradé dans Aspose.PSD pour .NET. En suivant le guide étape par étape, vous pouvez intégrer de manière transparente cette fonctionnalité dans vos applications .NET, améliorant ainsi l'attrait visuel de vos images.

## FAQ

### Q1 : Aspose.PSD est-il compatible avec toutes les versions de .NET ?

A1 : Aspose.PSD pour .NET est compatible avec .NET Framework et .NET Core.

### Q2 : Puis-je appliquer plusieurs effets à un seul calque ?

A2 : Oui, vous pouvez appliquer divers effets, notamment la superposition de dégradé, à un seul calque.

### Q3 : Où puis-je trouver plus d’exemples et de documentation ?

 A3 : Visitez le[Documentation](https://reference.aspose.com/psd/net/) pour des exemples détaillés et des lignes directrices.

### Q4 : Existe-t-il un essai gratuit ?

 A4 : Oui, vous pouvez accéder à un essai gratuit.[ici](https://releases.aspose.com/).

### Q5 : Comment puis-je obtenir de l'aide pour Aspose.PSD ?

 A5 : Visitez le[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour le soutien de la communauté.