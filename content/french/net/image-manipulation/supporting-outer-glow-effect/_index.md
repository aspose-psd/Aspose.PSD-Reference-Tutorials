---
title: Prise en charge de l'effet de lueur externe dans Aspose.PSD pour .NET
linktitle: Prise en charge de l'effet de lueur externe
second_title: API Aspose.PSD.NET
description: Explorez la puissance de Outer Glow Effect dans Aspose.PSD pour .NET. Améliorez la conception de vos images avec ce didacticiel étape par étape.
type: docs
weight: 16
url: /fr/net/image-manipulation/supporting-outer-glow-effect/
---
## Introduction

Bienvenue dans notre guide étape par étape sur la prise en charge de l'effet Outer Glow dans Aspose.PSD pour .NET. Aspose.PSD est une bibliothèque puissante qui permet une manipulation transparente des fichiers PSD dans les applications .NET. Dans ce didacticiel, nous explorerons la mise en œuvre de l'effet Outer Glow et fournirons une procédure détaillée pour l'intégrer dans vos projets.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

-  Aspose.PSD pour la bibliothèque .NET : téléchargez la bibliothèque à partir du[Documentation Aspose.PSD .NET](https://reference.aspose.com/psd/net/).

- Environnement de développement : configurez votre environnement de développement .NET préféré.

- Répertoires de documents et de sortie : définissez vos répertoires de documents et de sortie dans le code fourni.

## Importer des espaces de noms

Dans cette section, nous importerons les espaces de noms nécessaires pour lancer notre implémentation de Outer Glow Effect. Suivez ces étapes:

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageOptions;
```

Maintenant, décomposons l'exemple fourni en plusieurs étapes pour obtenir l'effet de lueur extérieure.

## Étape 1 : Définir les chemins de document et de sortie

```csharp
string baseDir = "Your Document Directory";
string outputDir = "Your Output Directory";
```

## Étape 2 : Charger l'image PSD

```csharp
string src = Path.Combine(baseDir, "GreenLayer.psd");
using (var image = (PsdImage)Image.Load(src))
{
    // Les étapes de mise en œuvre seront ajoutées ci-dessous.
}
```

## Étape 3 : Ajouter un effet de lueur externe

```csharp
OuterGlowEffect effect = image.Layers[1].BlendingOptions.AddOuterGlow();
```

## Étape 4 : Configurer les paramètres de lueur externe

```csharp
effect.Range = 10;
effect.Spread = 10;
((IColorFillSettings)effect.FillColor).Color = Color.Red;
effect.Opacity = 128;
effect.BlendMode = BlendMode.Normal;
```

## Étape 5 : Enregistrez l'image

```csharp
string outputPng = Path.Combine(outputDir, "output261.png");
image.Save(outputPng, new PngOptions());
```

## Étape 6 : Nettoyer

```csharp
File.Delete(outputPng);
```

## Étape 7 : Afficher le message de réussite

```csharp
Console.WriteLine("SupportOfOuterGlowEffect executed successfully");
```

## Conclusion

Toutes nos félicitations! Vous avez implémenté avec succès l’effet Outer Glow à l’aide d’Aspose.PSD pour .NET. Cette fonctionnalité puissante améliore l’attrait visuel de vos images, apportant une touche unique à vos créations.

## FAQ

### Q1 : Aspose.PSD est-il compatible avec tous les frameworks .NET ?

A1 : Oui, Aspose.PSD prend en charge un large éventail de frameworks .NET, garantissant la compatibilité avec divers environnements de développement.

### Q2 : Où puis-je trouver de la documentation supplémentaire pour Aspose.PSD ?

 A2 : Reportez-vous au[Documentation Aspose.PSD .NET](https://reference.aspose.com/psd/net/) pour des informations complètes et des exemples.

### Q3 : Comment puis-je obtenir une licence temporaire pour Aspose.PSD ?

 A3 : Visite[Aspose.PSD Licence temporaire](https://purchase.aspose.com/temporary-license/) pour les options de licence temporaire.

### Q4 : Quelle assistance est disponible pour les utilisateurs d'Aspose.PSD ?

 A4 : Rejoignez le[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour le soutien et les discussions de la communauté.

### Q5 : Puis-je acheter Aspose.PSD pour .NET ?

 A5 : Oui, explorez les options de licence et effectuez votre achat.[ici](https://purchase.aspose.com/buy).