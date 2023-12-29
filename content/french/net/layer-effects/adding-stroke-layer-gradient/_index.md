---
title: Ajout d'un calque de trait avec dégradé dans Aspose.PSD pour .NET
linktitle: Ajout d'un calque de trait avec dégradé
second_title: API Aspose.PSD.NET
description: Découvrez comment ajouter un calque de trait de dégradé dans Aspose.PSD pour .NET. Élevez vos compétences en manipulation d’images avec ce didacticiel complet.
type: docs
weight: 12
url: /fr/net/layer-effects/adding-stroke-layer-gradient/
---
## Introduction

Si vous cherchez à améliorer vos applications .NET avec des effets graphiques époustouflants, Aspose.PSD pour .NET est votre solution incontournable. Dans ce didacticiel, nous aborderons le processus d'ajout d'un calque de trait avec un dégradé à l'aide d'Aspose.PSD pour .NET. Ce guide étape par étape vous permettra d'améliorer l'attrait visuel de vos images sans effort.

## Conditions préalables

Avant de nous lancer dans cette aventure, assurez-vous d’avoir les conditions préalables suivantes en place :

- Une connaissance pratique du développement C# et .NET.
-  Aspose.PSD pour la bibliothèque .NET installée. Vous pouvez le télécharger[ici](https://releases.aspose.com/psd/net/).
- Un éditeur de code, tel que Visual Studio, pour implémenter les exemples fournis.

## Importer des espaces de noms

Pour commencer, importons les espaces de noms nécessaires dans notre projet. Ces espaces de noms sont cruciaux pour exploiter les fonctionnalités d’Aspose.PSD pour .NET.

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
```

## Étape 1 : configurer le répertoire de documents

Commencez par définir le chemin d’accès à votre répertoire de documents dans le code. Cela garantit que les fichiers nécessaires sont chargés et enregistrés à partir du bon emplacement.

```csharp
string dataDir = "Your Document Directory";
```

## Étape 2 : Chargez le fichier PSD

Chargez le fichier PSD source à l’aide d’Aspose.PSD pour .NET. Assurez-vous que la ressource d’effets est chargée pour manipuler efficacement les calques.

```csharp
string sourceFileName = dataDir + "Stroke.psd";
string exportPath = dataDir + "StrokeGradientChanged.psd";

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    // Le code pour gérer le fichier PSD vient ici
}
```

## Étape 3 : Vérifier les paramètres du trait de dégradé

Assurez-vous que le calque de trait avec un dégradé est correctement configuré en vérifiant divers paramètres tels que le mode de fusion, l'opacité et la visibilité.

```csharp
var gradientStroke = (StrokeEffect)im.Layers[2].BlendingOptions.Effects[0];

// Vérifications d'assertion pour les paramètres de trait de dégradé
AssertIsTrue(gradientStroke.BlendMode == BlendMode.Normal);
AssertIsTrue(gradientStroke.Opacity == 255);
AssertIsTrue(gradientStroke.IsVisible);

// Plus de vérifications d'assertions pour les paramètres de remplissage
// ...
```

Continuez à mettre en œuvre des vérifications d'assertion pour d'autres paramètres de remplissage, notamment les points de couleur et les points de transparence.

## Étape 4 : Modifier les paramètres du trait de dégradé

Maintenant, apportons quelques modifications aux paramètres du trait de dégradé. Modifiez les paramètres tels que la couleur, l'opacité, le mode de fusion et le type de dégradé pour obtenir l'effet visuel souhaité.

```csharp
// Code de modification des paramètres de trait de dégradé
// ...
```

## Étape 5 : Enregistrez le fichier PSD modifié

Enregistrez le fichier PSD modifié dans le chemin d'exportation spécifié.

```csharp
im.Save(exportPath);
```

## Conclusion

Toutes nos félicitations! Vous avez ajouté avec succès un calque de trait avec un dégradé à l'aide d'Aspose.PSD pour .NET. Ce didacticiel vous a doté des connaissances nécessaires pour améliorer vos images par programmation.

## FAQ

### Q1 : Puis-je utiliser Aspose.PSD pour .NET avec d’autres frameworks .NET ?

A1 : Oui, Aspose.PSD pour .NET est compatible avec divers frameworks .NET.

### Q2 : Existe-t-il un essai gratuit disponible pour Aspose.PSD pour .NET ?

 A2 : Oui, vous pouvez accéder à l'essai gratuit[ici](https://releases.aspose.com/).

### Q3 : Comment puis-je obtenir une assistance pour Aspose.PSD pour .NET ?

 A3 : Visitez le[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour le soutien de la communauté.

### Q4 : Où puis-je trouver une documentation complète pour Aspose.PSD pour .NET ?

 A4 : Reportez-vous au[Documentation](https://reference.aspose.com/psd/net/) pour des informations détaillées.

### Q5 : Comment puis-je acheter une licence pour Aspose.PSD pour .NET ?

 A5 : Vous pouvez acheter une licence[ici](https://purchase.aspose.com/buy).