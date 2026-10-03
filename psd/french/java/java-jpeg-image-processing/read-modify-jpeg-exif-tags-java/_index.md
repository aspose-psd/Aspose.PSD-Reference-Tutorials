---
date: 2026-10-03
description: Apprenez à lire les métadonnées d'image en Java et à modifier les balises
  EXIF JPEG avec Aspose.PSD for Java grâce à ce guide étape par étape, idéal pour
  les développeurs qui gèrent efficacement les métadonnées d'image.
keywords:
- java read image metadata
- read EXIF tags Java
- modify JPEG metadata Java
- Aspose.PSD Java
lastmod: 2026-10-03
linktitle: Lire et modifier les balises EXIF JPEG en Java
og_description: Apprenez à lire les métadonnées d'image en Java et à modifier les
  balises EXIF JPEG avec Aspose.PSD for Java. Ce guide présente du code étape par
  étape pour extraire et mettre à jour les informations EXIF.
og_image_alt: Guide showing how to java read image metadata and edit JPEG EXIF tags
  using Aspose.PSD for Java
og_title: Comment lire les métadonnées d'image en Java et modifier les balises EXIF
  JPEG
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  headline: How to java read image metadata and modify JPEG EXIF tags
  type: TechArticle
- description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  name: How to java read image metadata and modify JPEG EXIF tags
  steps:
  - name: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
    text: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
  type: HowTo
- questions:
  - answer: EXIF (Exchangeable Image File Format) metadata stores camera settings,
      timestamps, GPS coordinates, and other information embedded in JPEG and other
      image files.
    question: What is EXIF data?
  - answer: You can get a free trial from the [Aspose releases page](https://releases.aspose.com/).
    question: Can I use Aspose.PSD for Java for free?
  - answer: Aspose.PSD for Java supports Java SE 7 and above.
    question: Is Aspose.PSD for Java compatible with all versions of Java?
  - answer: Check out the [documentation](https://reference.aspose.com/psd/java/)
      for more details.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: You can get support from the [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/).
    question: How do I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- exif tags
- aspose psd
- jpeg metadata
- java tutorial
title: Comment lire les métadonnées d'image en Java et modifier les balises EXIF JPEG
url: /fr/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lire et modifier les balises EXIF JPEG en Java

## Introduction
Si vous devez **java read image metadata** à partir de fichiers JPEG et les modifier programmatiquement, vous êtes au bon endroit. Dans ce tutoriel, nous parcourrons l'extraction et la mise à jour des balises EXIF à l'aide d'Aspose.PSD pour Java. À la fin, vous pourrez récupérer les détails de l'appareil photo, l'orientation et les champs personnalisés, puis les réécrire dans le fichier — le tout sans éditeur graphique.

## Réponses rapides
- **Quelle bibliothèque gère les EXIF JPEG en Java ?** Aspose.PSD for Java.  
- **Combien de lignes de code pour lire les EXIF ?** Environ trois lignes après le chargement de l'image.  
- **Pouvez‑vous modifier les balises EXIF ?** Oui, vous pouvez changer n'importe quelle balise standard ou personnalisée et enregistrer le résultat.  
- **Formats d'image pris en charge ?** Plus de 150 formats, dont PSD, JPEG, PNG, TIFF et BMP.  
- **Version minimale de Java ?** Java 7 ou supérieure.

## Pourquoi utiliser Aspose.PSD pour Java ?
Aspose.PSD prend en charge **plus de 150 formats d'image** et peut traiter des fichiers jusqu'à **2 Go** sans charger le document complet en mémoire, vous offrant des opérations de métadonnées rapides et à faible consommation de mémoire sur de grandes collections de photos. Il fournit également une API simple pour lire et écrire les données EXIF, IPTC et XMP, rendant le traitement par lots de milliers d'images efficace et fiable.

## Prérequis
1. **Java Development Kit (JDK)** – assurez‑vous d'avoir JDK 11 ou plus récent. Vous pouvez le télécharger depuis le [site Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java library** – obtenez le dernier JAR depuis la [page des releases Aspose](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse ou tout autre éditeur de votre choix.  
4. **Connaissances de base en Java** – vous devez être à l'aise avec la création de projets et l'ajout de JAR externes.

## Qu'est‑ce que Java read image metadata ?
Java read image metadata désigne le processus d'accès programmatique aux informations intégrées telles que EXIF, IPTC et XMP stockées à l'intérieur des fichiers image à l'aide de code Java. Ces métadonnées peuvent inclure les réglages de l'appareil, les horodatages, les coordonnées GPS, les mentions de droits d'auteur et les commentaires utilisateur, permettant aux applications d'organiser, de rechercher et de manipuler les images en fonction de leurs données descriptives.

## Importer les packages
Tout d'abord, ajoutez le JAR Aspose.PSD au classpath de votre projet et importez les classes requises.

Le package `com.aspose.psd` fournit l'API principale pour charger les images et accéder à leurs ressources.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Comment lire les métadonnées d'image à partir de fichiers JPEG en Java ?
Chargez le JPEG avec `PsdImage.load("image.jpg")`, localisez la ressource de vignette qui contient les données EXIF, puis appelez `ExifData.read()` pour obtenir un objet `ExifData` rempli. Cette approche en une seule étape vous donne un accès complet à tous les champs EXIF standard et à toute balise personnalisée que vous auriez ajoutée.

## Étape 1 : Charger l'image PSD
PsdImage est la classe Aspose.PSD représentant un fichier PSD et fournit des méthodes pour accéder à ses ressources et métadonnées.  
Dans cette étape, nous chargerons l'image PSD à partir de laquelle nous voulons lire les données EXIF. Assurez‑vous que votre image se trouve dans le bon répertoire.

```java
String dataDir = "Your Document Directory";
PsdImage image = null;
try {
    image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Étape 2 : Parcourir les ressources de l'image
ThumbnailResource représente une image miniature stockée dans un fichier PSD, contenant souvent les données EXIF intégrées.  
Une fois l'image chargée, l'étape suivante consiste à parcourir ses ressources pour trouver la ressource de vignette, qui contient généralement les données EXIF.

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // Proceed to next step
    }
}
```

## Étape 3 : Extraire les données EXIF
JpegExifData est la classe qui contient les informations EXIF extraites d'une image JPEG, vous permettant de lire et de modifier les balises individuelles.  
Maintenant que nous disposons de la ressource de vignette, nous pouvons extraire les données EXIF de celle‑ci. Les données EXIF comprennent des informations précieuses comme le nom du propriétaire de l'appareil, la valeur d'ouverture, l'orientation, etc.

```java
JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
if (exifData != null) {
    System.out.println("Camera Owner Name: " + exifData.getCameraOwnerName());
    System.out.println("Aperture Value: " + exifData.getApertureValue());
    System.out.println("Orientation: " + exifData.getOrientation());
    System.out.println("Focal Length: " + exifData.getFocalLength());
    System.out.println("Compression: " + exifData.getCompression());
}
```

## Étape 4 : Modifier les données EXIF
Après avoir lu les données EXIF, vous souhaiterez peut‑être modifier certains de leurs champs. Voici comment procéder :

```java
if (exifData != null) {
    exifData.setCameraOwnerName("New Camera Owner");
    exifData.setApertureValue(3.5);
    exifData.setOrientation(1);
    exifData.setFocalLength(35.0);
    exifData.setCompression(6);
    thumbnail.getJpegOptions().setExifData(exifData);
}
```

## Étape 5 : Enregistrer les modifications
Enfin, après avoir modifié les données EXIF, enregistrez les changements dans un nouveau fichier PSD.

```java
try {
    image.save(dataDir + "Modified_Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Problèmes courants et solutions
- **Ressource de vignette manquante** – Certains JPEG stockent les EXIF directement dans l'en‑tête principal de l'image. Si la ressource de vignette est absente, utilisez `image.getExifData()` à la place.  
- **Les gros fichiers provoquent OutOfMemoryError** – Assurez‑vous d'exécuter la JVM avec suffisamment de heap (`-Xmx2g`) ou traitez l'image en mode flux avec `PsdImage.load(inputStream, loadOptions)`.  
- **Types de balises non pris en charge** – Aspose.PSD prend en charge toutes les balises EXIF standard ; les balises personnalisées peuvent nécessiter une gestion manuelle au niveau des octets.

## Questions fréquentes

**Q : Qu'est‑ce que les données EXIF ?**  
R : Les métadonnées EXIF (Exchangeable Image File Format) stockent les réglages de l'appareil, les horodatages, les coordonnées GPS et d'autres informations intégrées dans les fichiers JPEG et autres images.

**Q : Puis‑je utiliser Aspose.PSD pour Java gratuitement ?**  
R : Vous pouvez obtenir un essai gratuit depuis la [page des releases Aspose](https://releases.aspose.com/).

**Q : Aspose.PSD pour Java est‑il compatible avec toutes les versions de Java ?**  
R : Aspose.PSD pour Java prend en charge Java SE 7 et supérieur.

**Q : Où puis‑je trouver plus de documentation sur Aspose.PSD pour Java ?**  
R : Consultez la [documentation](https://reference.aspose.com/psd/java/) pour plus de détails.

**Q : Comment obtenir du support pour Aspose.PSD pour Java ?**  
R : Vous pouvez obtenir du support via le [forum de support Aspose PSD](https://forum.aspose.com/c/psd/34/).

## Conclusion
En suivant ces étapes, vous pouvez **java read image metadata** depuis n'importe quel JPEG, ajuster les champs EXIF nécessaires et réécrire les données mises à jour dans le fichier — le tout avec quelques lignes de code Java propre. L'API riche d'Aspose.PSD rend la gestion des métadonnées fiable et performante, vous permettant de l'intégrer dans des pipelines de traitement par lots, des outils de gestion de photos ou toute application nécessitant de travailler avec les informations d'image.

---

**Last Updated:** 2026-10-03  
**Tested With:** Aspose.PSD for Java 24.5  
**Author:** Aspose

## Tutoriels associés

- [Lire les informations de balises EXIF spécifiques en Java avec Aspose (asp)](/psd/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/)
- [Créer des métadonnées XMP dans les fichiers PSD avec Aspose.PSD pour Java](/psd/java/image-editing/create-xmp-metadata/)
- [Redimensionner une image avec Aspose.PSD pour Java – Dessiner des formes et opérations d'image de base](/psd/java/basic-image-operations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}