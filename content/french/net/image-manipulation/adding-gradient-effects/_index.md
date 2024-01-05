---
title: Ajout d'effets de dégradé aux images dans Aspose.PSD pour .NET
linktitle: Ajout d'effets de dégradé aux images
second_title: API Aspose.PSD.NET
description: Améliorez vos images avec des effets de dégradé captivants à l'aide d'Aspose.PSD pour .NET. Suivez notre tutoriel étape par étape pour des transformations visuelles créatives.
type: docs
weight: 11
url: /fr/net/image-manipulation/adding-gradient-effects/
---
## Introduction

L'amélioration des images avec des effets de dégradé peut ajouter une dimension captivante à votre contenu visuel. Aspose.PSD pour .NET fournit une plate-forme puissante pour incorporer des superpositions de dégradés dans vos images. Dans ce didacticiel, nous vous guiderons tout au long du processus d'ajout d'effets de dégradé à l'aide d'Aspose.PSD pour .NET.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

-  Aspose.PSD pour la bibliothèque .NET : téléchargez et installez la bibliothèque à partir de[Aspose.PSD pour la documentation .NET](https://reference.aspose.com/psd/net/).
- Environnement .NET : assurez-vous de disposer d'un environnement .NET fonctionnel configuré sur votre ordinateur.

## Importer des espaces de noms

Commencez par importer les espaces de noms nécessaires dans votre projet :

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
using System.IO;
```

## Étape 1 : charger l'image et définir les chemins

```csharp
// Le chemin d'accès au répertoire des documents.
string SourceDir = "Your Document Directory";
string OutputDir = "Your Output Directory";

string sourceFileName = Path.Combine(SourceDir, "GradientOverlay.psd");
string exportPath = Path.Combine(OutputDir, "GradientOverlayChanged.psd");

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};
```

## Étape 2 : affirmer les paramètres initiaux

Assurez-vous que les paramètres initiaux de la superposition de dégradé sont comme prévu :

```csharp
using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    var gradientOverlay = (GradientOverlayEffect)im.Layers[1].BlendingOptions.Effects[0];

    // Vérification des assertions pour les paramètres initiaux
    // ...

    // Points de couleur
    // ...

    //Points de transparence
    // ...
}
```

## Étape 3 : Modifier les paramètres de superposition de dégradé

Ajustez les paramètres de superposition de dégradé selon vos préférences :

```csharp
// Édition des tests
settings.Color = Color.Green;

gradientOverlay.Opacity = 193;
gradientOverlay.BlendMode = BlendMode.Lighten;

settings.AlignWithLayer = false;
settings.GradientType = GradientType.Radial;
settings.Angle = 45;
settings.Dither = true;
settings.HorizontalOffset = 15;
settings.VerticalOffset = 11;
settings.Reverse = true;

// Ajouter un nouveau point de couleur
// ...

// Changer l'emplacement du point précédent
// ...

// Ajouter un nouveau point de transparence
// ...

// Changer l'emplacement du point de transparence précédent
// ...

im.Save(exportPath);
```

## Étape 4 : Valider le fichier modifié

Vérifiez si les modifications ont été appliquées avec succès :

```csharp
// Tester le fichier après modification
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    var gradientOverlay = (GradientOverlayEffect)im.Layers[1].BlendingOptions.Effects[0];
    try
    {
        // Vérification des assertions pour les paramètres modifiés
        // ...
    }
    catch (Exception e)
    {
        string ex = e.StackTrace;
    }
}
```

## Conclusion

L'ajout d'effets de dégradé aux images à l'aide d'Aspose.PSD pour .NET ouvre un monde de possibilités créatives. Expérimentez avec différents paramètres pour obtenir l’impact visuel souhaité dans vos images.

## FAQ

### Q1 : Puis-je appliquer des effets de dégradé à plusieurs calques simultanément ?

A1 : Oui, vous pouvez appliquer des effets de dégradé à plusieurs calques en parcourant chaque calque et en appliquant les paramètres souhaités.

### Q2 : Quels formats de fichiers Aspose.PSD pour .NET prend-il en charge ?

A2 : Aspose.PSD pour .NET prend en charge divers formats de fichiers image, notamment PSD, PNG, JPEG, BMP et GIF.

### Q3 : Existe-t-il une version d’essai disponible pour Aspose.PSD pour .NET ?

 A3 : Oui, vous pouvez explorer les capacités d'Aspose.PSD pour .NET en téléchargeant la version d'essai gratuite à partir de[ici](https://releases.aspose.com/).

### Q4 : Comment puis-je obtenir une assistance pour Aspose.PSD pour .NET ?

 A4 : Pour toute assistance ou question, visitez le[Aspose.PSD pour le forum de support .NET](https://forum.aspose.com/c/psd/34).

### Q5 : Où puis-je acheter Aspose.PSD pour .NET ?

 A5 : Vous pouvez acheter la bibliothèque auprès du[Page d'achat Aspose.PSD pour .NET](https://purchase.aspose.com/buy).