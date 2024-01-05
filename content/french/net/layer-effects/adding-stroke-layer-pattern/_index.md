---
title: Ajout d'un calque de trait avec motif dans Aspose.PSD pour .NET
linktitle: Ajout d'un calque de trait avec un motif
second_title: API Aspose.PSD.NET
description: Améliorez vos fichiers PSD avec des calques et des motifs de traits à l'aide d'Aspose.PSD pour .NET. Suivez notre guide étape par étape pour une intégration transparente.
type: docs
weight: 13
url: /fr/net/layer-effects/adding-stroke-layer-pattern/
---
## Introduction

L'amélioration de vos fichiers PSD (Photoshop Document) avec des calques et des motifs de traits peut ajouter une touche dynamique à vos conceptions. Dans ce didacticiel, nous verrons comment exploiter Aspose.PSD pour .NET pour ajouter sans effort un calque de trait avec un motif à vos fichiers PSD. Aspose.PSD est une puissante bibliothèque .NET qui fournit une prise en charge complète de la manipulation des fichiers PSD, ce qui en fait un outil inestimable pour les développeurs et les concepteurs.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

- Connaissance de base du langage de programmation C#.
- Visual Studio installé sur votre ordinateur.
-  Bibliothèque Aspose.PSD pour .NET, que vous pouvez télécharger[ici](https://releases.aspose.com/psd/net/).

## Importer des espaces de noms

Assurez-vous d'importer les espaces de noms nécessaires dans votre code C# :

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.FileFormats.Psd.Layers.LayerResources;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
using System.IO;
```

## Étape 1 : Configurez votre environnement

Commencez par définir les répertoires source et de sortie dans votre code C# :

```csharp
string SourceDir = "Your Document Directory";
string OutputDir = "Your Output Directory";
```

## Étape 2 : Chargez le fichier PSD

Chargez le fichier PSD à l'aide de la classe PsdImage d'Aspose.PSD :

```csharp
var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

string sourceFileName = Path.Combine(SourceDir, "Stroke.psd");
using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    // Votre code pour traiter le fichier PSD va ici
}
```

## Étape 3 : préparer de nouvelles données de modèle

Définissez un nouveau modèle et ses limites :

```csharp
var newPattern = new int[]
{
    // Les couleurs de votre motif vont ici
};

var newPatternBounds = new Rectangle(0, 0, 4, 4);
var guid = Guid.NewGuid();
```

## Étape 4 : modifier le calque de trait

Accédez au calque de trait et mettez à jour ses propriétés :

```csharp
var patternStroke = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

// Vérifier et mettre à jour les propriétés du trait
// ...

// Mettre à jour l'opacité et le mode de fusion
patternStroke.Opacity = 127;
patternStroke.BlendMode = BlendMode.Color;
```

## Étape 5 : Mettre à jour les informations sur le modèle

Mettez à jour les informations de modèle dans le fichier PSD :

```csharp
foreach (var globalLayerResource in im.GlobalLayerResources)
{
    if (globalLayerResource is PattResource)
    {
        // Votre code pour mettre à jour les informations sur le modèle va ici
    }
}

// Enregistrez le fichier PSD modifié
im.Save(exportPath);
```

## Étape 6 : Vérifiez les modifications

Chargez le fichier PSD modifié et vérifiez les modifications :

```csharp
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    var patternStroke = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

    // Votre code pour vérifier les modifications va ici
}
```

## Conclusion

Toutes nos félicitations! Vous avez appris avec succès comment ajouter un calque de trait avec un motif dans Aspose.PSD pour .NET. Cette bibliothèque polyvalente permet aux développeurs de créer des conceptions visuellement attrayantes et d'améliorer la flexibilité des fichiers PSD.

## FAQ

### Q1 : Puis-je utiliser Aspose.PSD pour .NET avec n’importe quelle version de Visual Studio ?

A1 : Oui, Aspose.PSD pour .NET est compatible avec différentes versions de Visual Studio.

### Q2 : Comment puis-je obtenir une licence temporaire pour Aspose.PSD ?

 A2 : Visite[ici](https://purchase.aspose.com/temporary-license/) pour obtenir un permis temporaire.

### Q3 : Existe-t-il des exemples de fichiers PSD disponibles pour les tests ?

 A3 : Vous pouvez trouver des exemples de fichiers PSD dans la documentation[ici](https://reference.aspose.com/psd/net/).

### Q4 : Aspose.PSD est-il adapté au traitement par lots de fichiers PSD ?

A4 : Absolument, Aspose.PSD pour .NET offre une prise en charge robuste du traitement par lots.

### Q5 : Où puis-je demander de l'aide ou participer aux discussions communautaires ?

 A5 : Visitez le[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour le soutien et les interactions communautaires.