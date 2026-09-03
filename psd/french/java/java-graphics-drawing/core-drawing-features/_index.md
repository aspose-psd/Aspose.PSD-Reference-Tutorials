---
date: 2026-09-03
description: Apprenez à convertir PSD en BMP avec Java en utilisant Aspose.PSD, et
  découvrez les fonctionnalités de base du dessin telles que l'application de dégradés
  et la création de rectangles.
keywords:
- convert PSD to BMP
- how to draw PSD
- apply gradient PSD
- create rectangle PSD
lastmod: 2026-09-03
linktitle: Comment convertir PSD en BMP et dessiner avec Java
og_description: Convertissez PSD en BMP avec Java grâce à Aspose.PSD. Ce guide montre
  étape par étape comment charger des fichiers PSD, manipuler les pixels, appliquer
  des dégradés, créer des rectangles et enregistrer en BMP efficacement.
og_image_alt: 'Tutorial: converting PSD to BMP and drawing shapes in Java using Aspose.PSD'
og_title: Convertir PSD en BMP avec Java – Guide de dessin de base
schemas:
- author: Aspose
  dateModified: '2026-09-03'
  description: Learn how to convert PSD to BMP in Java using Aspose.PSD, and discover
    core drawing features like applying gradients and creating rectangles.
  headline: How to convert PSD to BMP and draw with Java
  type: TechArticle
- questions:
  - answer: Yes, the library fully supports layered PSD files, including transparency,
      blending modes, and layer effects.
    question: Can Aspose.PSD for Java handle layers and transparency in PSD files?
  - answer: Absolutely. You can automate batch jobs by iterating over a folder, loading
      each PSD, applying the same drawing logic, and saving as BMP or any other supported
      format.
    question: Is Aspose.PSD for Java suitable for batch processing of PSD files?
  - answer: Besides PSD, the API handles BMP, PNG, JPEG, TIFF, GIF, and over 20 additional
      raster formats for both input and output.
    question: Does Aspose.PSD for Java support multiple image formats other than PSD?
  - answer: Visit the [Aspose.PSD temporary license](https://purchase.aspose.com/temporary-license/)
      page for obtaining a temporary license.
    question: How can I obtain a temporary license for Aspose.PSD for Java?
  - answer: Explore the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for
      community support, tips, and additional resources.
    question: Where can I find more help and resources for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert PSD
- Aspose.PSD
- Java image processing
title: Comment convertir PSD en BMP et dessiner avec Java
url: /fr/java/java-graphics-drawing/core-drawing-features/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment convertir un PSD en BMP et dessiner avec Java

## Introduction
Aspose.PSD for Java est une bibliothèque Java qui permet la création, la modification et la conversion programmatiques de fichiers Adobe Photoshop PSD. Dans ce tutoriel, vous apprendrez à **convertir un PSD en BMP** et à explorer les fonctionnalités de dessin essentielles qui vous permettent de **dessiner des calques PSD, d’appliquer des dégradés et de créer des rectangles** directement depuis du code Java. Maîtriser ces capacités vous permet d’automatiser des pipelines de traitement d’image complexes sans avoir besoin de Photoshop installé.

## Réponses rapides
- **Puis‑je convertir un PSD en BMP avec une seule ligne de code ?** Oui – chargez le PSD avec `PsdImage` et appelez `save("output.bmp", SaveFormat.Bmp)`.  
- **Quelle version d’Aspose.PSD est requise ?** La dernière version 24.x prend en charge toutes les API de dessin de base.  
- **Ai‑je besoin d’une licence pour le développement ?** Une licence temporaire gratuite suffit pour les tests ; une licence complète est requise en production.  
- **Quelles versions de Java sont supportées ?** Java 8 à Java 21 sont pleinement compatibles.  
- **Puis‑je traiter en lot de nombreux fichiers PSD ?** Absolument – parcourez un répertoire et réutilisez la même logique de conversion.

## Comment convertir un PSD en BMP avec Java ?
Chargez le PSD source, modifiez éventuellement ses pixels ou ses calques de dessin, puis enregistrez‑le au format BMP. La conversion se fait en mémoire, ce qui évite les fichiers intermédiaires et permet de traiter des milliers d’images efficacement. Aspose.PSD diffuse les données, ce qui signifie que même les fichiers de plusieurs centaines de pages sont gérés sans épuiser la mémoire du tas.

### Quelles sont les fonctionnalités de dessin principales d’Aspose.PSD pour Java ?
La bibliothèque fournit un ensemble complet de primitives de dessin qui vous permettent de **dessiner des formes PSD**, **appliquer des remplissages en dégradé** et **créer des calques de rectangles** de façon programmatique. Ces API fonctionnent sur le même moteur pixel‑par‑pixel que Photoshop, garantissant une fidélité visuelle entre les formats.

## Prérequis
Avant de commencer, assurez‑vous que les éléments suivants sont prêts :

### Environnement de développement Java
Installez le Java Development Kit (JDK) depuis le [site d’Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html). Le tutoriel a été testé avec le JDK 11, mais tout JDK 8+ fonctionnera.

### Installation d’Aspose.PSD for Java
1. **Téléchargez Aspose.PSD for Java** – rendez‑vous sur la [page de téléchargement](https://releases.aspose.com/psd/java/) et récupérez la dernière archive ZIP.  
2. **Ajoutez les JARs à votre projet** – copiez `aspose-psd.jar` et ses dépendances dans votre classpath, ou référencez‑les via Maven/Gradle comme indiqué dans la documentation du produit.

Vous avez maintenant tout ce qu’il faut pour commencer à coder.

## Importer les packages
Pour travailler avec Aspose.PSD, vous devez importer les espaces de noms principaux. Ces imports vous donnent accès au chargement d’images, à la manipulation de pixels et aux utilitaires de dessin.  
```java
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## Étape 1 : charger une image PSD
La première étape consiste à créer une instance `PsdImage` qui représente le fichier source en mémoire. Cet objet vous donne un accès en lecture/écriture aux calques, canaux et pixels individuels.  
```java
String dataDir = "Your Document Directory";
String loadpath = dataDir + "sample.psd";
// Load the PSD image
PsdImage image = new PsdImage(loadpath);
```

## Étape 2 : manipuler les pixels
Une fois le PSD chargé, vous pouvez modifier ses données de pixels, dessiner de nouvelles formes ou appliquer des remplissages en dégradé. L’API de dessin reflète les outils de Photoshop, vous permettant de **dessiner des rectangles PSD** ou **d’appliquer des effets de dégradé PSD** en quelques appels de méthode.  
```java
// Load pixels of a specific region (e.g., a 100x10 rectangle starting from top-left corner)
int[] pixels = image.loadArgb32Pixels(new Rectangle(0, 0, 100, 10));
// Modify the pixels (e.g., apply a gradient effect)
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = i;  // Apply your desired manipulation logic here
}
```

## Étape 3 : enregistrer l’image modifiée
Après vos modifications, appelez la méthode `save` en spécifiant `SaveFormat.Bmp`. La bibliothèque écrit un fichier BMP qui préserve les changements visuels effectués, complétant le flux de travail **convertir PSD en BMP**.  
```java
String outpath = dataDir + "CoreDrawingFeatures.bmp";
// Save modified pixels back to the image
image.saveArgb32Pixels(new Rectangle(0, 0, 100, 10), pixels);
// Save the image to BMP format
image.save(outpath, new BmpOptions());
```

## Problèmes courants et dépannage
- **Erreurs de mémoire insuffisante** – Aspose.PSD diffuse les données ; toutefois, les PSD très volumineux (> 2 Go) peuvent nécessiter une allocation supplémentaire du tas JVM (`-Xmx4g`).  
- **Incohérences de profil couleur** – Si le BMP de sortie apparaît délavé, assurez‑vous que le profil ICC du PSD source est conservé en appelant `psdImage.getColorProfile()` avant l’enregistrement.  
- **Calques manquants après conversion** – Vérifiez que les calques masqués ne sont pas supprimés en testant `layer.isVisible()` avant d’enregistrer.

## Questions fréquemment posées

**Q : Aspose.PSD for Java peut‑il gérer les calques et la transparence dans les fichiers PSD ?**  
R : Oui, la bibliothèque prend en charge les fichiers PSD à calques, y compris la transparence, les modes de fusion et les effets de calque.

**Q : Aspose.PSD for Java est‑il adapté au traitement par lots de fichiers PSD ?**  
R : Absolument. Vous pouvez automatiser des travaux par lots en parcourant un dossier, en chargeant chaque PSD, en appliquant la même logique de dessin et en enregistrant au format BMP ou tout autre format supporté.

**Q : Aspose.PSD for Java supporte‑t‑il plusieurs formats d’image autres que le PSD ?**  
R : En plus du PSD, l’API gère BMP, PNG, JPEG, TIFF, GIF et plus de 20 formats raster supplémentaires en entrée comme en sortie.

**Q : Comment obtenir une licence temporaire pour Aspose.PSD for Java ?**  
R : Consultez la page de la [licence temporaire Aspose.PSD](https://purchase.aspose.com/temporary-license/) pour obtenir une licence temporaire.

**Q : Où puis‑je trouver davantage d’aide et de ressources pour Aspose.PSD for Java ?**  
R : Explorez le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour le support communautaire, des astuces et des ressources supplémentaires.

---

**Dernière mise à jour :** 2026-09-03  
**Testé avec :** Aspose.PSD 24.12 pour Java  
**Auteur :** Aspose

## Tutoriels associés

- [Comment créer des effets de dégradé radial dans Aspose.PSD for Java](/psd/java/advanced-image-effects/add-gradient-effects/)
- [Dessiner et enregistrer un rectangle dans un PSD avec Aspose.PSD for Java](/psd/java/basic-image-operations/simple-drawing/)
- [Comment convertir un PSD en formats d’image raster avec Aspose.PSD for Java](/psd/java/advanced-techniques/convert-psd-to-raster-forms/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}