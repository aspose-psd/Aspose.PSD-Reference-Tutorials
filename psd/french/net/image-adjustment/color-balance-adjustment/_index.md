---
title: Application du réglage de la balance des couleurs dans Aspose.PSD pour .NET
linktitle: Application du réglage de la balance des couleurs
second_title: API Aspose.PSD.NET
description: Améliorez les couleurs des images PSD sans effort avec la fonction de réglage de la balance des couleurs d'Aspose.PSD pour .NET. Suivez notre guide étape par étape pour des résultats époustouflants.
type: docs
weight: 14
url: /fr/net/image-adjustment/color-balance-adjustment/
---
## Introduction

Bienvenue dans ce guide complet sur l'application de l'ajustement de la balance des couleurs dans Aspose.PSD pour .NET ! Aspose.PSD est une puissante bibliothèque .NET qui permet aux développeurs de travailler efficacement avec les fichiers PSD. Dans ce didacticiel, nous nous concentrerons sur la fonction de réglage de la balance des couleurs, vous permettant d'améliorer facilement la balance des couleurs de vos images PSD.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

-  Aspose.PSD pour la bibliothèque .NET : téléchargez et installez la bibliothèque à partir du[Site Web Aspose.PSD](https://releases.aspose.com/psd/net/).
- Environnement de développement : assurez-vous que vous disposez d'un environnement de développement .NET fonctionnel configuré sur votre ordinateur.
- Fichier PSD : préparez un fichier PSD auquel vous souhaitez appliquer le réglage de la balance des couleurs.

## Importer des espaces de noms

Dans votre projet .NET, incluez les espaces de noms nécessaires pour utiliser les fonctionnalités Aspose.PSD. Ajoutez les lignes suivantes à votre code :

```csharp
using Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers;
```

Maintenant, décomposons le processus d'ajustement de la balance des couleurs en plusieurs étapes :

## Étape 1 : Chargez le fichier PSD

```csharp
string dataDir = "Your Document Directory";
var filePath = dataDir + "ColorBalance.psd";
var outputPath = dataDir + "ColorBalance_out.psd";

using (var im = (FileFormats.Psd.PsdImage)Image.Load(filePath))
{
    // Le code pour le réglage de la balance des couleurs sera ajouté dans les étapes suivantes.
}
```

## Étape 2 : accéder et ajuster la balance des couleurs

```csharp
foreach (var layer in im.Layers)
{
    var cbLayer = layer as ColorBalanceAdjustmentLayer;
    if (cbLayer != null)
    {
        cbLayer.ShadowsCyanRedBalance = 30;
        cbLayer.ShadowsMagentaGreenBalance = -15;
        cbLayer.ShadowsYellowBlueBalance = 40;
        cbLayer.MidtonesCyanRedBalance = -90;
        cbLayer.MidtonesMagentaGreenBalance = -25;
        cbLayer.MidtonesYellowBlueBalance = 20;
        cbLayer.HighlightsCyanRedBalance = -30;
        cbLayer.HighlightsMagentaGreenBalance = 67;
        cbLayer.HighlightsYellowBlueBalance = -95;
        cbLayer.PreserveLuminosity = true;
    }
}
```

## Étape 3 : Enregistrez l'image ajustée

```csharp
im.Save(outputPath);
```

Vous avez maintenant appliqué avec succès l’ajustement de la balance des couleurs à votre fichier PSD à l’aide d’Aspose.PSD pour .NET !

## Conclusion

Félicitations! Vous avez appris à améliorer la balance des couleurs de vos images PSD avec Aspose.PSD pour .NET. Expérimentez avec différentes valeurs d'équilibre pour obtenir les effets visuels souhaités.

## FAQ

### Q1 : Puis-je appliquer le réglage de la balance des couleurs à plusieurs calques ?

A1 : Oui, vous pouvez parcourir tous les calques de votre fichier PSD et ajuster la balance des couleurs selon vos besoins.

### Q2 : Aspose.PSD pour .NET est-il adapté au traitement par lots de fichiers PSD ?

A2 : Absolument ! Aspose.PSD offre des capacités efficaces de traitement par lots pour les fichiers PSD.

### Q3 : Comment puis-je obtenir une licence temporaire pour Aspose.PSD pour .NET ?

 A3 : Visite[Aspose.PSD Licence temporaire](https://purchase.aspose.com/temporary-license/) pour un permis temporaire.

### Q4 : Où puis-je trouver plus d’exemples et de documentation ?

 A4 : Explorez le[Documentation Aspose.PSD](https://reference.aspose.com/psd/net/) pour des exemples détaillés et des guides.

### Q5 : Quelles options de support sont disponibles pour Aspose.PSD pour .NET ?

 A5 : Visitez le[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour le soutien et les discussions de la communauté.
