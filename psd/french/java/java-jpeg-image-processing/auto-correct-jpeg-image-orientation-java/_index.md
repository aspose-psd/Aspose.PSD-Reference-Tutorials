---
title: Correction automatique de l'orientation de l'image JPEG en Java
linktitle: Correction automatique de l'orientation de l'image JPEG en Java
second_title: API Java Aspose.PSD
description: Apprenez à corriger automatiquement l'orientation de l'image JPEG en Java à l'aide d'Aspose.PSD. Améliorez vos compétences en traitement d’image sans effort.
type: docs
weight: 12
url: /fr/java/java-jpeg-image-processing/auto-correct-jpeg-image-orientation-java/
---
## Introduction
À l'ère numérique d'aujourd'hui, la manipulation et l'optimisation des images par programmation sont devenues une tâche cruciale pour les développeurs de divers domaines. Aspose.PSD pour Java offre aux développeurs des outils robustes pour gérer efficacement les formats PSD, JPEG et autres formats d'image. Ce didacticiel se penche sur une tâche spécifique : corriger automatiquement l'orientation de l'image JPEG à l'aide d'Aspose.PSD pour Java. Que vous créiez une application de retouche photo, gériez des ressources d'images dans un système de gestion de contenu ou automatisiez des flux de travail de traitement d'images, ce guide vous fournira les connaissances nécessaires pour intégrer de manière transparente cette fonctionnalité dans vos applications Java.
## Conditions préalables
Avant de plonger dans ce didacticiel, assurez-vous d'avoir configuré les conditions préalables suivantes :
- Environnement de développement Java : assurez-vous que le kit de développement Java (JDK) est installé sur votre système.
-  Aspose.PSD pour Java JAR : téléchargez la bibliothèque Aspose.PSD pour Java à partir de[ici](https://releases.aspose.com/psd/java/).
- Environnement de développement intégré (IDE) : utilisez IntelliJ IDEA, Eclipse ou tout autre IDE de votre choix pour le développement Java.
- Compréhension de base de Java et du traitement d'images : Une connaissance de la programmation Java et des concepts de base du traitement d'images sera bénéfique.

## Importer des packages
Avant de commencer avec l'exemple, assurez-vous d'importer les packages nécessaires depuis Aspose.PSD pour Java :
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## Étape 1 : Charger l'image PSD
Tout d'abord, chargez l'image PSD contenant la vignette JPEG dont l'orientation doit être corrigée :
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```
 Remplacer`"Your Document Directory"` avec le chemin du répertoire réel où se trouve votre fichier PSD.
## Étape 2 : Itérer sur les ressources d’images
Ensuite, parcourez les ressources d'image pour trouver la ressource de vignettes JPEG :
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // Rechercher une ressource miniature. Ils sont généralement au format de fichier Jpeg.
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Ajustez les données des vignettes.
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
        if (exifData != null && exifData.getThumbnail() != null) {
            // Si une vignette est stockée, faites-la pivoter automatiquement.
            PsdImage jpegImage = (PsdImage) exifData.getThumbnail();
            if (jpegImage != null) {
                jpegImage.autoRotate();
            }
        }
    }
}
```
## Étape 3 : Enregistrez l'image
Enfin, enregistrez l'image corrigée après avoir appliqué l'auto-rotation :
```java
image.save();
```
Cette étape garantit que les modifications apportées à l'image sont conservées.

## Conclusion
En conclusion, l'utilisation d'Aspose.PSD pour Java fournit une solution puissante pour corriger automatiquement les orientations des images JPEG dans les fichiers PSD. En suivant les étapes décrites dans ce didacticiel, les développeurs peuvent améliorer leurs flux de travail de traitement d'images, en garantissant que les images sont correctement affichées sur diverses plates-formes et appareils.
## FAQ
### Qu’est-ce qu’Aspose.PSD pour Java ?
Aspose.PSD pour Java est une bibliothèque puissante qui permet aux développeurs Java de travailler avec PSD, JPEG et d'autres formats d'image par programme.
### Comment puis-je télécharger Aspose.PSD pour Java ?
 Vous pouvez télécharger la bibliothèque depuis[ici](https://releases.aspose.com/psd/java/).
### Aspose.PSD pour Java prend-il en charge la manipulation d’images ?
Oui, il prend en charge diverses tâches de manipulation d'images telles que le redimensionnement, le recadrage et l'ajustement de l'orientation.
### Où puis-je trouver de la documentation pour Aspose.PSD pour Java ?
 Une documentation complète est disponible[ici](https://reference.aspose.com/psd/java/).
### Puis-je essayer Aspose.PSD pour Java gratuitement ?
 Oui, vous pouvez bénéficier d'un essai gratuit auprès de[ici](https://releases.aspose.com/).