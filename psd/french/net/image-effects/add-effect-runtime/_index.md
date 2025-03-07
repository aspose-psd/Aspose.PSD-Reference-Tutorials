---
title: Ajout d'effets au moment de l'exécution dans Aspose.PSD pour .NET
linktitle: Ajout d'effets au moment de l'exécution
second_title: API Aspose.PSD.NET
description: Explorez les améliorations d'images dynamiques à l'aide d'Aspose.PSD pour .NET. Ajoutez facilement des effets au moment de l’exécution.
weight: 10
url: /fr/net/image-effects/add-effect-runtime/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajout d'effets au moment de l'exécution dans Aspose.PSD pour .NET

## Introduction

Améliorer l’attrait visuel des images est une exigence courante dans les applications de conception graphique et de traitement d’images. Dans ce didacticiel, nous verrons comment ajouter des effets au moment de l'exécution à l'aide d'Aspose.PSD pour .NET. Aspose.PSD est une API puissante qui permet aux développeurs de travailler de manière transparente avec les fichiers Adobe Photoshop. 

## Conditions préalables

Avant de plonger dans le guide étape par étape, assurez-vous d'avoir les éléments suivants :

- Connaissance de base de C# et du framework .NET.
-  Aspose.PSD pour .NET installé. Vous pouvez le télécharger depuis[ici](https://releases.aspose.com/psd/net/).

## Importer des espaces de noms

Pour commencer, assurez-vous d'inclure les espaces de noms nécessaires dans votre projet C#. Ces espaces de noms sont essentiels pour utiliser les fonctionnalités fournies par Aspose.PSD.

```csharp
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageLoadOptions;
```

## Étape 1 : Configurez votre répertoire de documents

```csharp
string dataDir = "Your Document Directory";
```

Remplacez « Votre répertoire de documents » par le chemin réel où se trouvent vos fichiers PSD.

## Étape 2 : Charger l'image PSD avec la ressource d'effets

```csharp
string sourceFileName = dataDir + "ThreeRegularLayers.psd";
string exportPath = dataDir + "ThreeRegularLayersChanged.psd";

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
```

Cette étape charge l'image PSD, permettant le chargement des ressources d'effets.

## Étape 3 : ajouter un effet de calque de superposition de couleurs

```csharp
var effect = im.Layers[1].BlendingOptions.AddColorOverlay();
effect.Color = Color.Green;
effect.Opacity = 128;
effect.BlendMode = BlendMode.Normal;
```

Ici, nous ajoutons un effet de superposition de couleurs au deuxième calque de l'image PSD. Vous pouvez personnaliser la couleur, l'opacité et le mode de fusion selon vos préférences.

## Étape 4 : Enregistrez l'image modifiée

```csharp
im.Save(exportPath);
```

Enfin, enregistrez l'image avec l'effet appliqué dans le chemin d'exportation spécifié.

## Conclusion

L'ajout d'effets au moment de l'exécution dans Aspose.PSD pour .NET est un processus simple. Avec seulement quelques lignes de code, vous pouvez améliorer dynamiquement l’attrait visuel de vos images. Expérimentez avec différents effets et paramètres pour obtenir les résultats souhaités.

## FAQ

### Q1 : Aspose.PSD est-il compatible avec le dernier framework .NET ?

A1 : Oui, Aspose.PSD est régulièrement mis à jour pour garantir la compatibilité avec les dernières versions du framework .NET.

### Q2 : Puis-je appliquer plusieurs effets à un seul calque ?

A2 : Absolument ! Vous pouvez enchaîner plusieurs effets sur un calque pour créer des améliorations visuelles complexes.

### Q3 : Y a-t-il des limites aux types d'effets que je peux ajouter ?

A3 : Aspose.PSD offre une large gamme d'effets, mais il est conseillé de consulter la documentation pour des détails spécifiques sur les effets pris en charge.

### Q4 : Comment puis-je obtenir une licence temporaire à des fins de test ?

 A4 : Vous pouvez obtenir une licence temporaire[ici](https://purchase.aspose.com/temporary-license/) pour les tests et l'évaluation.

### Q5 : Où puis-je trouver du soutien supplémentaire et des discussions communautaires ?

 A5 : Visitez le[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour du soutien et des discussions.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
