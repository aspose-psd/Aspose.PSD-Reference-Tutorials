---
title: Ajout d'un calque de trait avec une couleur unie dans Aspose.PSD pour .NET
linktitle: Ajout d'un calque de trait avec une couleur unie
second_title: API Aspose.PSD.NET
description: Améliorez vos compétences en manipulation d'images .NET avec Aspose.PSD. Apprenez à ajouter des calques de traits avec des couleurs unies, étape par étape.
weight: 11
url: /fr/net/layer-effects/adding-stroke-layer-solid-color/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajout d'un calque de trait avec une couleur unie dans Aspose.PSD pour .NET

## Introduction

Dans le domaine du développement .NET, la création d’images visuellement attrayantes est une exigence courante. Aspose.PSD pour .NET fournit un ensemble d'outils puissants pour manipuler et améliorer les images de manière transparente. L'une des fonctionnalités essentielles consiste à ajouter un calque de trait avec une couleur unie, qui apporte du dynamisme et de la profondeur à vos images. Dans ce didacticiel, nous vous guiderons étape par étape tout au long du processus en utilisant Aspose.PSD pour .NET.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous d'avoir les prérequis suivants :

- Connaissance de base du développement .NET.
- Visual Studio installé sur votre ordinateur.
- Aspose.PSD pour la bibliothèque .NET. Vous pouvez le télécharger depuis le[site web](https://releases.aspose.com/psd/net/).

## Importer des espaces de noms

Commencez par importer les espaces de noms nécessaires pour exploiter les fonctionnalités d'Aspose.PSD pour .NET :

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
```

## Étape 1 : Chargez le fichier PSD

Commencez par charger le fichier PSD que vous souhaitez améliorer avec un calque de trait. Assurez-vous d'avoir le chemin de fichier correct :

```csharp
string dataDir = "Your Document Directory";
string sourceFileName = dataDir + "Stroke.psd";

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    // Le code pour les étapes suivantes sera ajouté ici
}
```

## Étape 2 : accéder aux propriétés de l'effet de trait

Récupérez les propriétés de l'effet de trait à partir du fichier PSD :

```csharp
var colorStroke = (StrokeEffect)im.Layers[1].BlendingOptions.Effects[0];

if ((colorStroke.BlendMode != BlendMode.Normal) ||
    (colorStroke.Opacity != 255) ||
    (colorStroke.IsVisible != true))
{
    throw new Exception("Color stroke effect was read wrong");
}
```

## Étape 3 : Ajuster les paramètres de trait

Modifiez les paramètres de trait selon vos préférences. Dans cet exemple, nous changeons la couleur en jaune, définissons l'opacité sur 127 et utilisons le mode de fusion des couleurs :

```csharp
var fillSettings = (ColorFillSettings)colorStroke.FillSettings;

if ((fillSettings.Color != Color.Black) || (fillSettings.FillType != FillType.Color))
{
    throw new Exception("Color stroke effect settings were read wrong");
}

fillSettings.Color = Color.Yellow;
colorStroke.Opacity = 127;
colorStroke.BlendMode = BlendMode.Color;
```

## Étape 4 : Enregistrez l'image modifiée

Enregistrez l'image après avoir appliqué les modifications du calque de trait :

```csharp
string exportPath = dataDir + "StrokeGradientChanged.psd";
im.Save(exportPath);
```

## Étape 5 : Vérifiez les modifications

Assurez-vous que les modifications sont correctement appliquées en chargeant et en inspectant l'image modifiée :

```csharp
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    // Le code pour vérifier les modifications sera ajouté ici
}
```

Répétez ces étapes pour des ajustements supplémentaires ou expérimentez différents effets de trait pour obtenir l'impact visuel souhaité.

## Conclusion

Félicitations! Vous avez appris avec succès comment ajouter un calque de trait avec une couleur unie à l'aide d'Aspose.PSD pour .NET. Cette fonctionnalité puissante ouvre un monde de possibilités pour améliorer vos images dans l'environnement .NET.

## FAQ

### Q1 : Aspose.PSD pour .NET est-il compatible avec les dernières versions du framework .NET ?

A1 : Oui, Aspose.PSD pour .NET est régulièrement mis à jour pour garantir la compatibilité avec les dernières versions du framework .NET.

### Q2 : Puis-je utiliser Aspose.PSD pour .NET pour des projets commerciaux ?

A2 : Absolument ! Aspose.PSD pour .NET est un produit commercial et vous pouvez l'utiliser dans vos projets en achetant une licence.

### Q3 : Où puis-je trouver plus d’exemples et de documentation pour Aspose.PSD pour .NET ?

 A3 : Explorez le[documentation](https://reference.aspose.com/psd/net/) pour des exemples et des conseils complets.

### Q4 : Existe-t-il un essai gratuit disponible pour Aspose.PSD pour .NET ?

 A4 : Oui, vous pouvez bénéficier d'un essai gratuit auprès du[page des versions](https://releases.aspose.com/).

### Q5 : Comment puis-je obtenir une assistance pour Aspose.PSD pour .NET ?

 A5 : Visitez le[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour demander de l'aide et entrer en contact avec la communauté.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
