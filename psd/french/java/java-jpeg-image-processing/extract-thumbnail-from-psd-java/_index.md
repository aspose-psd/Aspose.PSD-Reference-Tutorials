---
date: 2026-10-03
description: Apprenez comment extraire la miniature d'un PSD en Java à l'aide d'Aspose.PSD.
  Ce guide étape par étape couvre la configuration, les extraits de code et l'enregistrement
  de la miniature au format JPEG.
keywords:
- extract thumbnail from psd
- java aspose psd
- psd thumbnail extraction
lastmod: 2026-10-03
linktitle: Extraire la miniature d'un PSD en Java
og_description: Apprenez comment extraire la miniature d'un PSD en Java avec Aspose.PSD.
  Ce guide vous accompagne à travers la configuration, le chargement du fichier, l'extraction
  de la miniature et son enregistrement au format JPEG.
og_image_alt: Screenshot showing Java code extracting a thumbnail from a PSD file
  using Aspose.PSD
og_title: Extraire la miniature d'un PSD en Java à l'aide d'Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to extract thumbnail from PSD in Java using Aspose.PSD. This
    step‑by‑step guide covers setup, code snippets, and saving the thumbnail as a
    JPEG image.
  headline: Extract thumbnail from PSD in Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD is a Java library that enables programmatic creation, manipulation,
      and conversion of PSD and other raster image formats without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD?
  - answer: You can refer to the [documentation](https://reference.aspose.com/psd/java/)
      for detailed API references and examples.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: Yes, you can download a [free trial](https://releases.aspose.com/) to
      evaluate the library’s capabilities.
    question: Can I try Aspose.PSD for free before purchasing?
  - answer: Temporary licenses are available from the [temporary license](https://purchase.aspose.com/temporary-license/)
      page.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Yes, Aspose.PSD can be used in both personal and commercial projects under
      its licensing terms.
    question: Is Aspose.PSD suitable for commercial use?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose.psd
- thumbnail extraction
title: Extraire la miniature d'un PSD en Java
url: /fr/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Extraire une vignette d'un PSD en Java

## Introduction
Extraire une vignette d'un fichier PSD vous permet de générer des aperçus rapides sans charger l'image en pleine résolution. En Java, Aspose.PSD rend ce processus simple et performant. Dans ce tutoriel, vous apprendrez comment configurer la bibliothèque, localiser la ressource de vignette et l'enregistrer en tant que fichier JPEG — le tout en quelques lignes de code.

## Réponses rapides
- **Quelle bibliothèque gère les vignettes PSD ?** Aspose.PSD for Java.
- **Combien de lignes de code sont nécessaires ?** Environ cinq lignes pour charger, extraire et enregistrer.
- **Puis-je extraire des vignettes de gros fichiers PSD ?** Oui, Aspose.PSD traite des fichiers jusqu'à 500 MB sans chargement complet en mémoire.
- **Ai-je besoin d'une licence pour le développement ?** Un essai gratuit fonctionne pour l'évaluation ; une licence est requise pour la production.
- **Quels formats de sortie sont pris en charge ?** La vignette extraite peut être enregistrée en JPEG, PNG ou BMP.

## Qu'est-ce que l'extraction d'une vignette d'un PSD ?
L'extraction d'une vignette d'un PSD est le processus de lecture de la petite image d'aperçu intégrée dans un document Photoshop (PSD). Cet aperçu est stocké comme une ressource et peut être enregistré indépendamment pour la cataloguer ou l'afficher. La vignette est généralement une représentation basse résolution utilisée par les applications pour afficher un résumé visuel rapide sans charger l'image en pleine taille.

## Pourquoi utiliser Aspose.PSD pour cette tâche ?
Aspose.PSD prend en charge **plus de 30 formats d'image** et peut gérer des fichiers PSD jusqu'à **500 Mo** tout en maintenant une faible utilisation de la mémoire car il lit les ressources à la demande. L'API offre également une gestion robuste des erreurs, vous permettant d'extraire de manière fiable des vignettes même à partir de fichiers corrompus.

## Prérequis
Avant de commencer, assurez-vous d'avoir :
- Java Development Kit (JDK) installé.
- Bibliothèque Aspose.PSD for Java téléchargée depuis [Aspose.PSD for Java download](https://releases.aspose.com/psd/java/).
- Familiarité de base avec la syntaxe Java et la configuration du projet.

## Comment extraire une vignette d'un fichier PSD en Java ?
Chargez le fichier PSD avec `PsdImage`, localisez le `ThumbnailResource` et enregistrez ses données d'image en JPEG. Aspose.PSD abstrait l'analyse de bas niveau, vous n'avez donc qu'à appeler `getResources()` puis `save()` sur l'image extraite. Cette approche fonctionne pour tout PSD contenant une vignette, quelle que soit la taille du fichier.

## Importer les packages
`Image` est la classe de base pour charger des images. `PsdImage` représente un document PSD. `ThumbnailResource` et `Thumbnail4Resource` représentent les ressources de vignette. `JpegOptions` spécifie les options d'enregistrement JPEG.

```text
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
```

## Étape 1 : charger le fichier PSD
Tout d'abord, créez une instance `PsdImage` pointant vers votre fichier PSD. Le constructeur ne lit que l'en-tête et les ressources requises, maintenant ainsi une utilisation minimale de la mémoire.

```text
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
```

Remplacez `"Your_Document_Directory/"` par le chemin du répertoire où se trouve votre fichier PSD, et `"your_file.psd"` par le nom de votre fichier PSD.

## Étape 2 : parcourir les ressources de l'image
Aspose.PSD stocke les vignettes sous forme d'objets `ThumbnailResource` dans la collection de ressources de l'image. Parcourez la collection, vérifiez le type de ressource et capturez la première vignette rencontrée.

```text
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extract thumbnail data
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Create a new image with the extracted thumbnail data
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Save the extracted thumbnail as a separate JPEG file
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Output success message
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Exit the loop once thumbnail is found and processed
    }
}
```
```

## Étape 3 : enregistrer la vignette extraite
Une fois que vous avez l'image de la vignette, appelez sa méthode `save` pour l'écrire sur le disque. Vous pouvez choisir JPEG, PNG ou BMP ; JPEG est le plus courant pour les aperçus web.

## Étape 4 : gestion des différents types de vignettes
Si un PSD contient plusieurs variantes de vignette, comme `Thumbnail4Resource`, étendez la logique d'itération pour vérifier chaque type. L'API fournit des classes séparées pour chaque ressource, vous permettant de sélectionner la résolution dont vous avez besoin.

## Problèmes courants et solutions
- **Aucune vignette trouvée :** Tous les fichiers PSD n'intègrent pas d'aperçu. Vérifiez le fichier source dans le panneau “File → File Info” de Photoshop.
- **Erreur de format non pris en charge :** Assurez-vous d'utiliser la dernière version d'Aspose.PSD ; les versions antérieures peuvent ne pas prendre en charge les nouveaux types de ressources de vignette.
- **Mémoire insuffisante sur les gros fichiers :** Utilisez `PsdImage.load(..., LoadOptions)` avec `LoadOptions.setLoadResourcesOnly(true)` pour éviter de charger les données complètes de l'image lorsque vous n'avez besoin que de la vignette.

## Questions fréquemment posées

**Q : Qu'est-ce qu'Aspose.PSD ?**  
R : Aspose.PSD est une bibliothèque Java qui permet la création, la manipulation et la conversion programmatique de fichiers PSD et d'autres formats d'images raster sans nécessiter Adobe Photoshop.

**Q : Où puis‑je trouver plus de documentation sur Aspose.PSD pour Java ?**  
R : Vous pouvez consulter la [documentation](https://reference.aspose.com/psd/java/) pour des références API détaillées et des exemples.

**Q : Puis‑je essayer Aspose.PSD gratuitement avant d'acheter ?**  
R : Oui, vous pouvez télécharger un [essai gratuit](https://releases.aspose.com/) pour évaluer les capacités de la bibliothèque.

**Q : Comment obtenir une licence temporaire pour Aspose.PSD ?**  
R : Des licences temporaires sont disponibles sur la page [licence temporaire](https://purchase.aspose.com/temporary-license/).

**Q : Aspose.PSD convient‑il à un usage commercial ?**  
R : Oui, Aspose.PSD peut être utilisé dans des projets personnels et commerciaux selon ses conditions de licence.

---

**Dernière mise à jour :** 2026-10-03  
**Testé avec :** Aspose.PSD for Java 24.12  
**Auteur :** Aspose

## Tutoriels associés

- [Comment convertir un PSD en formats d'image raster avec Aspose.PSD pour Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [Enregistrer un PSD en JPEG et prendre en charge la couleur RVB avec Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)
- [Redimensionner une image avec Aspose.PSD pour Java – Dessiner des formes et opérations d'image de base](/psd/java/basic-image-operations/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}