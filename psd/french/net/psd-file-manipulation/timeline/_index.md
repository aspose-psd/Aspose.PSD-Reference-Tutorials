---
title: Travailler avec Timeline dans Aspose.PSD pour .NET
linktitle: Travailler avec la chronologie
second_title: API Aspose.PSD.NET
description: Améliorez la manipulation des images PSD avec Aspose.PSD pour la classe .NET Timeline. Contrôlez les propriétés des images, les états des calques et libérez les possibilités créatives sans effort.
type: docs
weight: 16
url: /fr/net/psd-file-manipulation/timeline/
---
## Introduction
Dans le monde dynamique de la conception graphique et de la manipulation d’images, la capacité de contrôler et de manipuler la chronologie des images est cruciale. Aspose.PSD pour .NET fournit une solution puissante avec sa classe Timeline. Cette fonctionnalité de haut niveau permet aux utilisateurs d'apporter des modifications à la chronologie de PsdImage, telles que la modification du délai d'image, la modification des états de calque sur des images spécifiques, etc.
## Conditions préalables
Avant de plonger dans les possibilités passionnantes qu'offre le cours Timeline, assurez-vous d'avoir les conditions préalables suivantes en place :
-  Bibliothèque Aspose.PSD pour .NET : assurez-vous que la bibliothèque Aspose.PSD pour .NET est installée. Vous pouvez le télécharger depuis le[Aspose.PSD pour la documentation .NET](https://reference.aspose.com/psd/net/).
-  Répertoires de documents et de sortie : définissez les chemins de vos répertoires de documents et de sortie dans le code. Ajustez le`baseDir` et`outputDir` variables en fonction de la structure de votre projet.
Voyons maintenant comment utiliser la classe Timeline, étape par étape.
## Importer des espaces de noms
Pour commencer à travailler avec la classe Timeline, importez les espaces de noms nécessaires dans votre code :
```csharp
using System;
using System.Collections.Generic;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.Animation;
```
## Étape 1 : Charger l'image PSD
Commencez par charger l'image PSD à partir du fichier source spécifié. Assurez-vous que le chemin du fichier source est correctement défini :
```csharp
string sourceFile = Path.Combine(baseDir, "image1219.psd");
using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    //Votre code pour d'autres opérations va ici
}
```
## Étape 2 : accéder à la chronologie
Une fois l'image PSD chargée, accédez à la Timeline en utilisant le code suivant :
```csharp
Timeline timeline = psdImage.Timeline;
```
## Étape 3 : Modifier la méthode d'élimination
Manipuler la méthode de suppression d’un cadre spécifique. Dans cet exemple, nous modifions la méthode dispose de l'image 1 :
```csharp
timeline.Frames[0].DisposalMethod = FrameDisposalMethod.DoNotDispose;
```
## Étape 4 : Ajuster le délai d'image
Modifier le délai d'une trame particulière. Ici, nous changeons le retard de l'image 2 en 15 :
```csharp
timeline.Frames[1].Delay = 15;
```
## Étape 5 : Modifier l'état du calque
Modifiez l'opacité du "Couche 1" sur un cadre spécifique. Dans ce cas, nous définissons l'opacité à 50 sur l'image 2 :
```csharp
LayerState layerState11 = timeline.Frames[1].LayerStates[1];
layerState11.Opacity = 50;
```
## Étape 6 : Déplacer le calque
Déplacez le « Couche 1 » vers le coin inférieur gauche d'un cadre spécifique (le cadre 3 dans cet exemple) :
```csharp
LayerState layerState21 = timeline.Frames[2].LayerStates[1];
layerState21.PositionOffset = new Point(-50, 230);
```
## Étape 7 : Ajouter un nouveau cadre
Ajoutez une nouvelle image à la timeline :
```csharp
List<Frame> frames = new List<Frame>(timeline.Frames);
frames.Add(new Frame());
timeline.Frames = frames.ToArray();
```
## Étape 8 : Changer le mode de fusion
Modifiez le mode de fusion du « Couche 1 » sur une image spécifique (image 4 dans ce cas) :
```csharp
LayerState layerState31 = timeline.Frames[3].LayerStates[1];
layerState31.BlendMode = BlendMode.Dissolve;
```
## Étape 9 : Enregistrer les modifications
Appliquez les modifications à l'instance PsdImage et enregistrez l'image PSD modifiée :
```csharp
psdImage.Save(outputPsd);
```
## Étape 10 : Nettoyer
Enfin, faites le ménage en supprimant le fichier de sortie temporaire :
```csharp
File.Delete(outputPsd);
```
## Conclusion

En conclusion, la classe Timeline d'Aspose.PSD pour .NET permet aux développeurs d'avoir un contrôle granulaire sur la chronologie des images PSD. Grâce à une série d'étapes simples, vous pouvez manipuler les propriétés des cadres, les états des calques, etc., ouvrant ainsi un champ de possibilités créatives.

## FAQ

### Q1 : Aspose.PSD pour .NET convient-il aux débutants ?

A1 : Absolument ! Aspose.PSD pour .NET fournit une interface conviviale et une documentation complète, le rendant accessible aux développeurs débutants et chevronnés.

### Q2 : Puis-je appliquer des modifications à la chronologie aux images GIF ?

A2 : La classe Timeline est spécifiquement conçue pour les images PSD. Pour la manipulation GIF, reportez-vous à Aspose.GIF pour .NET.

### Q3 : Où puis-je trouver une assistance supplémentaire ou discuter de problèmes ?

 A3 : Visitez le[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour le soutien de la communauté et les discussions sur les problèmes.

### Q4 : Comment puis-je obtenir une licence temporaire pour Aspose.PSD pour .NET ?

 A4 : Acquérir une licence temporaire[ici](https://purchase.aspose.com/temporary-license/).

### Q5 : Quels sont les principaux avantages de l’utilisation d’Aspose.PSD pour .NET ?

A5 : Aspose.PSD pour .NET offre des capacités avancées de traitement d'image, de manipulation de fichiers PSD et de rendu hautes performances.