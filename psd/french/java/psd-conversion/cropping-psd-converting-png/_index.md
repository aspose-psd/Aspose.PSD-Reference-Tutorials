---
date: 2026-03-21
description: Apprenez à convertir les fichiers PSD en PNG et à recadrer les fichiers
  PSD à l’aide d’Aspose.PSD pour Java. Ce guide montre le traitement d’image étape
  par étape dans les applications Java.
linktitle: Cropping PSD when Converting to PNG
second_title: Aspose.PSD Java API
title: Comment convertir un PSD en PNG tout en le recadrant avec Aspose.PSD pour Java
url: /fr/java/psd-conversion/cropping-psd-converting-png/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment convertir un PSD en PNG tout en recadrant avec Aspose.PSD pour Java

## Introduction
Dans le monde dynamique du développement Java, maîtriser le traitement d'images efficace est crucial. Dans ce tutoriel, vous apprendrez **comment convertir un PSD en PNG** et recadrer l'image en un seul flux de travail à l'aide de la puissante bibliothèque Aspose.PSD pour Java. À la fin de ce guide étape par étape, vous serez capable d'ajouter un recadrage précis à vos exportations PNG et de permettre à vos applications Java de gérer les actifs PSD en toute confiance.

## Réponses rapides
- **Que fait le code ?** Charge un PSD, recadre un rectangle et l'enregistre en PNG.  
- **Quelle bibliothèque est requise ?** Aspose.PSD for Java (dernière version).  
- **Ai‑je besoin d'une licence ?** Oui, une licence commerciale est requise pour une utilisation en production.  
- **Puis‑je définir n'importe quelle région de recadrage ?** Absolument – vous définissez les valeurs X, Y, largeur et hauteur dont vous avez besoin.  
- **Cette approche est‑elle rapide pour les gros fichiers ?** Oui, Aspose.PSD est optimisé pour un traitement haute performance.

## Qu'est‑ce que la conversion PSD en PNG ?
Convertir un PSD en PNG signifie prendre un document Photoshop à calques et le aplatir en une image PNG sans perte. Ce format est idéal pour la diffusion sur le web, les vignettes ou tout scénario où vous avez besoin d'une image raster sans les calques d'origine.

## Pourquoi recadrer le PSD avant de le convertir en PNG ?
Le recadrage vous permet d'extraire uniquement la partie du design dont vous avez besoin, réduisant la taille du fichier et se concentrant sur le contenu visuel pertinent. C'est particulièrement utile pour générer des vignettes, des ressources d'interface utilisateur ou préparer des images pour des mises en page réactives.

## Prérequis
Avant de plonger dans le tutoriel, assurez‑vous d'avoir les prérequis suivants en place :
- Connaissances de base en programmation Java.  
- Java Development Kit (JDK) installé sur votre système.  
- Bibliothèque Aspose.PSD for Java téléchargée et ajoutée à votre projet.  
- Un fichier PSD d'exemple pour l'expérimentation.

## Importer les packages
Dans votre projet Java, assurez‑vous d'importer les packages nécessaires pour utiliser les fonctionnalités d'Aspose.PSD :
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;
import com.aspose.psd.imageoptions.PngOptions;
```

## Étape 1 : Configurer votre projet
Commencez par créer un projet Java et ajouter la bibliothèque Aspose.PSD pour Java au classpath de votre projet. Cela vous donne accès à toutes les classes de traitement d'images dont vous aurez besoin.

## Étape 2 : Charger l'image PSD
```java
String dataDir = "Your Document Directory";
String srcPath = dataDir + "sample.psd";
// Load an existing PSD image
RasterImage image = (RasterImage)Image.load(srcPath);
```
*Ici nous chargeons le fichier PSD source dans un objet `RasterImage`, qui fournit des opérations basées sur le raster telles que le recadrage.*

## Étape 3 : Définir la région de recadrage
```java
// Create an instance of Rectangle class by passing x, y, width, and height
Rectangle cropRegion = new Rectangle(0, 0, 350, 450);
```
*Le `Rectangle` définit la zone que vous souhaitez conserver. Ajustez les valeurs `x`, `y`, `width` et `height` selon votre design. Cette étape répond directement au mot‑clé « définir la région de recadrage ». *

## Étape 4 : Recadrer l'image PSD
```java
// Call the crop method of Image class and pass the Rectangle instance
image.crop(cropRegion);
```
*Appeler `crop` modifie l'image en mémoire, en éliminant tout ce qui se trouve en dehors du rectangle spécifié.*

## Étape 5 : Définir les options d'exportation PNG
```java
// Create an instance of PngOptions class
PngOptions pngOptions = new PngOptions();
```
*`PngOptions` vous permet de contrôler les paramètres spécifiques au PNG tels que le niveau de compression, le type de couleur, etc.*

## Étape 6 : Enregistrer l'image recadrée en PNG
```java
// Provide output path and PngOptions to convert the PSD file to PNG and save the output
String destName = dataDir + "export.png";
image.save(destName, pngOptions);
```
*La méthode `save` effectue l'opération **convertir un PSD en PNG** tout en préservant le recadrage que vous avez défini.*

## Pièges courants et conseils
- **Dimensions du rectangle incorrectes :** Assurez‑vous que la largeur et la hauteur ne dépassent pas la taille de l'image originale, sinon une exception sera levée.  
- **Utilisation de la mémoire avec de gros PSD :** Libérez l'objet `RasterImage` (`image.dispose()`) après l'enregistrement pour libérer les ressources natives.  
- **Licence non définie :** Si vous exécutez le code sans licence valide, un filigrane apparaîtra sur le PNG de sortie.

## Questions fréquentes
### Puis‑je recadrer des fichiers PSD avec des formes irrégulières en utilisant Aspose.PSD pour Java ?
Oui, Aspose.PSD pour Java vous permet de définir une région de recadrage personnalisée, vous permettant de recadrer les images sous diverses formes.

### Aspose.PSD pour Java convient‑il aux tâches de traitement d'images à grande échelle ?
Absolument ! Aspose.PSD est conçu pour gérer efficacement les grandes images, ce qui le rend idéal pour les projets avec des exigences importantes en traitement d'images.

### Ai‑je besoin d'une licence pour Aspose.PSD pour Java ?
Oui, une licence valide est requise pour une utilisation commerciale. Vous pouvez l'obtenir sur [Aspose Purchase](https://purchase.aspose.com/buy).

### Comment puis‑je obtenir de l'aide ou signaler des problèmes avec Aspose.PSD pour Java ?
Visitez le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour demander de l'aide, partager vos expériences et signaler tout problème que vous rencontrez.

### Puis‑je essayer Aspose.PSD pour Java avant d'acheter ?
Bien sûr ! Explorez les fonctionnalités de la bibliothèque avec un essai gratuit disponible [ici](https://releases.aspose.com/).

---

**Dernière mise à jour :** 2026-03-21  
**Testé avec :** Aspose.PSD pour Java 24.12 (dernière version au moment de la rédaction)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}