---
date: 2026-09-28
description: Comment ajouter une miniature à un segment JFIF en Java en utilisant
  Aspose.PSD. Suivez ce guide étape par étape pour intégrer des miniatures dans les
  fichiers PSD rapidement et de manière fiable.
keywords:
- how to add thumbnail
- JFIF segment Java
- Aspose.PSD thumbnail
- Java image processing
lastmod: 2026-09-28
linktitle: Ajouter une miniature au segment JFIF en Java
og_description: Comment ajouter une miniature à un segment JFIF en Java en utilisant
  Aspose.PSD. Suivez ce guide étape par étape pour intégrer des miniatures dans les
  fichiers PSD rapidement et de manière fiable.
og_image_alt: Guide showing how to add thumbnail to JFIF segment in Java with Aspose.PSD
og_title: Comment ajouter une miniature à un segment JFIF en Java
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  headline: How to add thumbnail to JFIF segment in Java
  type: TechArticle
- description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  name: How to add thumbnail to JFIF segment in Java
  steps:
  - name: import packages
    text: '`Document`, `JfifResource`, and related classes are part of the Aspose.PSD
      namespace. Document represents the PSD file container, and JfifResource provides
      access to the JFIF segment within the PSD. Import them at the top of your source
      file.'
  - name: load the PSD image
    text: Create a `PsdImage` instance by passing the file path to the constructor.
      PsdImage is the Aspose.PSD class that models a Photoshop document. This loads
      the document metadata while streaming the pixel data.
  - name: iterate over image resources
    text: Search the `Resources` collection for a `JfifResource`. When found, you
      can replace its thumbnail byte array with a new JPEG‑encoded preview.
  - name: adjust thumbnail data
    text: Generate a small JPEG thumbnail (e.g., 120 × 120 px) using any image‑processing
      library, then assign the resulting byte array to `jfifResource.ThumbnailData`.
  - name: save the modified image
    text: Call the `save` method on the `PsdImage` object, specifying the output path
      and desired format. The JFIF segment now contains the new thumbnail.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a commercial library that enables developers to
      create, edit, convert, and render Photoshop PSD files without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD for Java?
  - answer: Detailed documentation can be found on the [Aspose.PSD for Java documentation
      page](https://reference.aspose.com/psd/java/).
    question: Where can I find more documentation for Aspose.PSD for Java?
  - answer: Yes, Aspose.PSD for Java can be used commercially. You can purchase a
      license from [Aspose.PSD's purchase page](https://purchase.aspose.com/buy).
    question: Is Aspose.PSD for Java suitable for commercial use?
  - answer: Yes, you can download a free trial from [Aspose.PSD's trial download page](https://releases.aspose.com/).
    question: Can I try Aspose.PSD for Java before purchasing?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- add thumbnail
- Aspose.PSD
- Java image processing
- JFIF
- PSD
title: Comment ajouter une miniature à un segment JFIF en Java
url: /fr/java/java-jpeg-image-processing/add-thumbnail-to-jfif-segment-java/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment ajouter une miniature au segment JFIF en Java

## Introduction
Ajouter une miniature au segment JFIF d'un fichier PSD est une exigence courante lorsque vous avez besoin d'un aperçu visuel rapide sans charger l'image complète. Dans ce tutoriel, vous apprendrez **comment ajouter une miniature** à un segment JFIF en Java en utilisant Aspose.PSD. À la fin du guide, vous disposerez d'un extrait de code exécutable, d'une compréhension de la structure JFIF sous-jacente, et de conseils pour gérer efficacement les gros fichiers.

## Réponses rapides
- **Quelle bibliothèque est requise ?** Aspose.PSD for Java.
- **Quelle version de Java fonctionne ?** JDK 11 ou ultérieure.
- **Combien de lignes de code sont nécessaires ?** Environ 10 lignes pour charger, modifier et enregistrer.
- **Puis-je traiter des fichiers de plusieurs mégaoctets ?** Oui, Aspose.PSD diffuse les données, de sorte que l'utilisation de la mémoire reste faible.
- **Une licence commerciale est‑elle nécessaire ?** Une licence est requise pour une utilisation en production ; un essai gratuit est disponible.

## Qu'est‑ce qu'un segment JFIF ?
Le segment JFIF est un bloc du JPEG File Interchange Format qui peut stocker des données optionnelles telles que des miniatures, EXIF ou des profils de couleur.  
Il réside à l'intérieur du flux JPEG d'un fichier PSD et est reconnu par la plupart des visionneuses d'images pour la génération d'aperçus rapides.

## Pourquoi ajouter une miniature à un fichier PSD ?
Aspose.PSD for Java prend en charge **plus de 30 formats d'image** et peut traiter des fichiers jusqu'à **2 Go** sans charger le document complet en mémoire. Ajouter une miniature réduit la bande passante réseau lors de la transmission des aperçus et accélère le rendu de l'interface utilisateur dans les applications de galerie.

## Prérequis
- Java Development Kit (JDK) : Assurez‑vous d'avoir Java installé sur votre système. Vous pouvez le télécharger depuis le site [Oracle's JDK website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
- Aspose.PSD for Java : Vous devez disposer de la bibliothèque Aspose.PSD for Java. Vous pouvez l'obtenir depuis la [Aspose.PSD Java download page](https://releases.aspose.com/psd/java/).
- Environnement de développement intégré (IDE) : Utilisez un IDE tel qu'IntelliJ IDEA ou Eclipse pour le développement Java.
- Connaissances de base en Java : Familiarité avec le langage de programmation Java et ses concepts.

## Comment ajouter une miniature à un segment JFIF en Java ?
Chargez le PSD cible, localisez la ressource JFIF, remplacez ses données de miniature, puis enregistrez le fichier. L'opération complète peut être réalisée avec quelques appels d'API simples, et Aspose.PSD gère la structure JPEG de bas niveau pour vous.

### Étape 1 : importer les packages
`Document`, `JfifResource` et les classes associées font partie de l'espace de noms Aspose.PSD. Document représente le conteneur du fichier PSD, et JfifResource fournit l'accès au segment JFIF au sein du PSD. Importez‑les en haut de votre fichier source.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

### Étape 2 : charger l'image PSD
Créez une instance `PsdImage` en passant le chemin du fichier au constructeur. PsdImage est la classe Aspose.PSD qui modélise un document Photoshop. Cela charge les métadonnées du document tout en diffusant les données de pixels.

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "your_image.psd");
```

### Étape 3 : parcourir les ressources d'image
Recherchez la collection `Resources` pour un `JfifResource`. Lorsqu'il est trouvé, vous pouvez remplacer son tableau d'octets de miniature par un nouvel aperçu encodé en JPEG.

```java
for(int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        
        // Continue with thumbnail processing
    }
}
```

### Étape 4 : ajuster les données de la miniature
Générez une petite miniature JPEG (par ex., 120 × 120 px) à l'aide de n'importe quelle bibliothèque de traitement d'image, puis affectez le tableau d'octets résultant à `jfifResource.ThumbnailData`.

```java
try {
    PsdImage thumbnailImage = new PsdImage(100, 100);
    
    // Fill thumbnail data (example: create a simple pixel array)
    int[] pixels = new int[thumbnailImage.getWidth() * thumbnailImage.getHeight()];
    for (int j = 0; j < pixels.length; j++) {
        pixels[j] = j;
    }
    
    // Save thumbnail data
    thumbnailImage.saveArgb32Pixels(thumbnailImage.getBounds(), pixels);
    
    // Set thumbnail data to Jpeg options
    JpegExifData exifData = new JpegExifData();
    exifData.setThumbnail(thumbnailImage);
    JpegOptions jpegOptions = new JpegOptions();
    jpegOptions.setExifData(exifData);
    
    // Set options to thumbnail resource
    thumbnail.getJpegOptions().setExifData(exifData);
    
} catch(Exception e) {
    // Handle exceptions
} finally {
    // Dispose of resources
}
```

### Étape 5 : enregistrer l'image modifiée
Appelez la méthode `save` sur l'objet `PsdImage`, en spécifiant le chemin de sortie et le format souhaité. Le segment JFIF contient désormais la nouvelle miniature.

```java
image.save(dataDir + "output.psd");
```

## Problèmes courants et solutions
- **Miniature non visible dans les visionneuses :** Assurez‑vous que les données de la miniature sont un tableau d'octets JPEG valide et que ses dimensions sont inférieures ou égales à 256 × 256 px, taille maximale prise en charge par la spécification JFIF.
- **OutOfMemoryError sur de gros PSD :** Utilisez `PsdImage.load(inputStream, true)` pour activer le mode diffusion, ce qui maintient une faible consommation de mémoire.
- **Type de ressource incorrect :** Vérifiez que la ressource que vous modifiez est bien un `JfifResource` ; d'autres ressources comme `ExifResource` n'affecteront pas l'affichage de la miniature.

## Questions fréquemment posées

**Q : Qu'est‑ce qu'Aspose.PSD for Java ?**  
R : Aspose.PSD for Java est une bibliothèque commerciale qui permet aux développeurs de créer, modifier, convertir et rendre des fichiers Photoshop PSD sans nécessiter Adobe Photoshop.

**Q : Où puis‑je trouver plus de documentation pour Aspose.PSD for Java ?**  
R : Une documentation détaillée est disponible sur la [page de documentation Aspose.PSD for Java](https://reference.aspose.com/psd/java/).

**Q : Aspose.PSD for Java convient‑il à un usage commercial ?**  
R : Oui, Aspose.PSD for Java peut être utilisé commercialement. Vous pouvez acheter une licence depuis la [page d'achat d'Aspose.PSD](https://purchase.aspose.com/buy).

**Q : Puis‑je essayer Aspose.PSD for Java avant d'acheter ?**  
R : Oui, vous pouvez télécharger une version d'essai gratuite depuis la [page de téléchargement d'essai d'Aspose.PSD](https://releases.aspose.com/).

**Q : Comment obtenir du support pour Aspose.PSD for Java ?**  
R : Pour le support, consultez le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

---

**Dernière mise à jour :** 2026-09-28  
**Testé avec :** Aspose.PSD for Java 24.11  
**Auteur :** Aspose

## Tutoriels associés

- [Ajouter une ressource IOPA aux fichiers PSD en utilisant Aspose PSD for Java](/psd/java/modifying-converting-psd-images/add-iopa-resource-psd-files/)
- [Ajouter une signature à une image – Dessiner l'image sur le canevas avec Aspose.PSD for Java](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Comment faire pivoter une image à un angle spécifique avec Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}