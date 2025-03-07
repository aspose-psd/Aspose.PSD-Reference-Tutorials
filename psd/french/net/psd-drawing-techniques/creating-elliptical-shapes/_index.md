---
title: Création de formes elliptiques avec Aspose.PSD pour .NET
linktitle: Création de formes elliptiques avec Aspose.PSD pour .NET
second_title: API Aspose.PSD.NET
description: Apprenez à dessiner des formes elliptiques dans .NET à l'aide d'Aspose.PSD. Guide étape par étape avec des exemples de code. Créez des graphismes époustouflants sans effort.
weight: 13
url: /fr/net/psd-drawing-techniques/creating-elliptical-shapes/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Création de formes elliptiques avec Aspose.PSD pour .NET

## Introduction

Bienvenue dans notre guide complet sur la création de formes elliptiques à l'aide d'Aspose.PSD pour .NET. Aspose.PSD est une puissante bibliothèque .NET qui permet aux développeurs de manipuler et de convertir des fichiers Photoshop sans avoir recours à Adobe Photoshop. Dans ce didacticiel, nous vous guiderons tout au long du processus de dessin de formes elliptiques à l'aide de la bibliothèque.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

- Aspose.PSD pour la bibliothèque .NET : assurez-vous que la bibliothèque Aspose.PSD est installée dans votre projet .NET. Vous pouvez le télécharger depuis le[Aspose.PSD pour la documentation .NET](https://reference.aspose.com/psd/net/).

- Environnement .NET : ce didacticiel suppose que vous possédez une connaissance pratique du framework .NET.

## Importer des espaces de noms

Pour commencer, importez les espaces de noms nécessaires dans votre projet. Cela garantit que vous avez accès aux classes et méthodes requises pour dessiner des formes elliptiques. Voici un exemple :

```csharp
using Aspose.PSD.Brushes;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;
```

Maintenant, décomposons le processus de création de formes elliptiques en plusieurs étapes :

## Étape 1 : configurer le répertoire de documents

```csharp
// Le chemin d'accès au répertoire des documents.
string dataDir = "Your Document Directory";
```

## Étape 2 : Créer une instance de BmpOptions

```csharp
// Créez une instance de BmpOptions et définissez ses différentes propriétés
string outpath = dataDir + "Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.BitsPerPixel = 32;
```

## Étape 3 : Créer une instance d'image

```csharp
// Créer une instance d'Image
using (Image image = new PsdImage(100, 100))
{
    // Créer et initialiser une instance de la classe Graphics et de la surface Clear Graphics
    Graphics graphic = new Graphics(image);
    graphic.Clear(Color.Yellow);
```

## Étape 4 : dessiner une forme d'ellipse en pointillé

```csharp
    // Dessinez une forme d'ellipse en pointillés en spécifiant l'objet Stylo de couleur rouge et un rectangle environnant.
    graphic.DrawEllipse(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
```

## Étape 5 : dessiner une forme d'ellipse continue

```csharp
    //Dessinez une forme d'ellipse continue en spécifiant l'objet Stylo ayant un pinceau solide de couleur bleue et un rectangle environnant.
    graphic.DrawEllipse(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    // Exportez l'image au format de fichier bmp.
    image.Save(outpath, saveOptions);
}
```

## Conclusion

Félicitations! Vous avez réussi à créer des formes elliptiques à l’aide d’Aspose.PSD pour .NET. Ce didacticiel a couvert les étapes essentielles, de la configuration de l'environnement au dessin de formes d'ellipse en pointillés et continues.

## FAQ

### Q1 : Où puis-je trouver la documentation d’Aspose.PSD pour .NET ?

 A1 : La documentation est disponible[ici](https://reference.aspose.com/psd/net/).

### Q2 : Comment télécharger Aspose.PSD pour .NET ?

 A2 : Vous pouvez le télécharger depuis la page de version[ici](https://releases.aspose.com/psd/net/).

### Q3 : Existe-t-il un essai gratuit disponible ?

 A3 : Oui, vous pouvez accéder à l'essai gratuit[ici](https://releases.aspose.com/).

### Q4 : Comment puis-je obtenir une assistance pour Aspose.PSD pour .NET ?

 A4 : Visitez le forum d'assistance[ici](https://forum.aspose.com/c/psd/34).

### Q5 : Ai-je besoin d’une licence temporaire pour tester ?

 A5 : Oui, vous pouvez obtenir une licence temporaire[ici](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
