---
title: Recadrage de fichiers PSD lors de la conversion en PNG dans Aspose.PSD pour .NET
linktitle: Recadrage des fichiers PSD lors de la conversion en PNG
second_title: API Aspose.PSD.NET
description: Apprenez à recadrer des fichiers PSD sans effort à l'aide d'Aspose.PSD pour .NET. Suivez notre guide étape par étape pour une conversion transparente en PNG.
type: docs
weight: 18
url: /fr/net/psd-file-manipulation/crop-psd-conversion-png/
---
## Introduction
Dans le domaine du développement .NET, la manipulation et la conversion d'images sont une tâche courante. Aspose.PSD pour .NET fournit un ensemble d'outils puissants pour rationaliser ce processus. Une exigence fréquente consiste à recadrer les fichiers PSD avant de les convertir en PNG. Dans ce didacticiel étape par étape, nous approfondirons le processus d'utilisation d'Aspose.PSD pour .NET.
## Conditions préalables
Avant de vous lancer dans ce voyage, assurez-vous d'avoir les éléments suivants :
-  Aspose.PSD pour la bibliothèque .NET : téléchargez et installez la bibliothèque à partir du[Aspose.PSD pour la documentation .NET](https://reference.aspose.com/psd/net/).
- Exemple de fichier PSD : préparez un fichier PSD pour l’expérimentation. Si vous n'en avez pas, vous pouvez utiliser l'exemple fourni dans le didacticiel.
- Environnement .NET : assurez-vous d'avoir configuré un environnement de développement .NET fonctionnel.
- Répertoire de documents : spécifiez le chemin d'accès à votre répertoire de documents dans le code.
## Importer des espaces de noms
Dans votre projet .NET, incluez les espaces de noms nécessaires pour Aspose.PSD pour .NET :
```csharp
using Aspose.PSD.ImageOptions;
```
## Étape 1 : Charger l'image PSD
```csharp
// Le chemin d'accès au répertoire des documents.
string dataDir = "Your Document Directory";
string srcPath = dataDir + @"sample.psd";
// Charger une image PSD existante
using (RasterImage image = (RasterImage)Image.Load(srcPath))
{
    // Votre code pour les étapes ultérieures sera ici
}
```
## Étape 2 : définir le rectangle de recadrage
```csharp
// Créez une instance de la classe Rectangle en passant x, y, largeur et hauteur
Rectangle cropRectangle = new Rectangle(0, 0, 350, 450);
```
## Étape 3 : Recadrer l'image
```csharp
//Appelez la méthode crop de la classe Image et transmettez l'instance de la classe rectangle
image.Crop(cropRectangle);
```
## Étape 4 : Spécifier les options PNG
```csharp
// Créer une instance de la classe PngOptions
PngOptions pngOptions = new PngOptions();
```
## Étape 5 : Enregistrez l’image recadrée au format PNG
```csharp
// Appelez la méthode save, fournissez le chemin de sortie et PngOptions pour convertir le fichier PSD en PNG et enregistrer la sortie
string destName = dataDir + @"export.png";
image.Save(destName, pngOptions);
```
## Conclusion

Toutes nos félicitations! Vous avez appris avec succès comment recadrer des fichiers PSD lors de leur conversion en PNG à l'aide d'Aspose.PSD pour .NET. Cette capacité peut s’avérer inestimable dans divers scénarios de traitement d’images.

## FAQ

### Q1 : Puis-je utiliser cette bibliothèque dans un projet commercial ?

 A1 : Oui, Aspose.PSD pour .NET est disponible pour un usage commercial. Faire référence à[Licence Aspose.PSD](https://purchase.aspose.com/buy) pour plus de détails.

### Q2 : Existe-t-il un essai gratuit ?

 A2 : Absolument ! Vous pouvez explorer une version d'essai gratuite[ici](https://releases.aspose.com/).

### Q3 : Où puis-je trouver de l'assistance pour Aspose.PSD pour .NET ?

 A3 : Visitez le[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour toute aide ou question.

### Q4 : Comment puis-je obtenir une licence temporaire ?

 A4 : Si vous avez besoin d'un permis temporaire, vous pouvez en obtenir un[ici](https://purchase.aspose.com/temporary-license/).

### Q5 : Y a-t-il des exemples ou des didacticiels disponibles dans la documentation ?

 A5 : Oui, vous pouvez trouver une documentation complète et des exemples[ici](https://reference.aspose.com/psd/net/).