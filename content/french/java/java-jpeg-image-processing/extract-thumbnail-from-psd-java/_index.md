---
title: Extraire la vignette du PSD en Java
linktitle: Extraire la vignette du PSD en Java
second_title: API Java Aspose.PSD
description: Découvrez comment extraire des vignettes de fichiers PSD à l'aide d'Aspose.PSD pour Java. Ce guide étape par étape couvre tout, de la configuration à l'enregistrement des images extraites.
type: docs
weight: 15
url: /fr/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
---
## Introduction
Dans ce didacticiel, nous verrons comment extraire des vignettes de fichiers PSD à l'aide d'Aspose.PSD pour Java. Les miniatures peuvent être utiles pour des aperçus rapides ou pour créer des versions plus petites d'images intégrées dans des documents PSD. Examinons les étapes nécessaires pour y parvenir à l'aide d'Aspose.PSD.
## Conditions préalables
Avant de commencer, assurez-vous d'avoir la configuration suivante :
- Kit de développement Java (JDK) installé sur votre système.
-  Aspose.PSD pour la bibliothèque Java. Vous pouvez le télécharger depuis[ici](https://releases.aspose.com/psd/java/).
- Connaissance de base de la programmation Java.
## Importer des packages
Pour commencer, incluez le package Aspose.PSD nécessaire dans votre classe Java :
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
## Étape 1 : Chargez le fichier PSD
Tout d’abord, chargez le fichier PSD contenant la vignette que vous souhaitez extraire.
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
 Remplacer`"Your_Document_Directory/"` avec le chemin du répertoire où se trouve votre fichier PSD, et`"your_file.psd"` avec le nom de votre fichier PSD.
## Étape 2 : Itérer sur les ressources d’images
Parcourez les ressources d’image pour trouver la ressource miniature.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extraire les données miniatures
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Créez une nouvelle image avec les données miniatures extraites
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Enregistrez la vignette extraite dans un fichier JPEG distinct
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Message de réussite de sortie
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Quittez la boucle une fois la vignette trouvée et traitée
    }
}
```
## Étape 3 : Enregistrez la vignette extraite
Enregistrez la vignette extraite en tant que fichier image distinct (dans ce cas, en tant que fichier JPEG).
## Étape 4 : Gérer différents types de vignettes
 Si votre fichier PSD peut contenir plusieurs types de vignettes, telles que`Thumbnail4Resource`, vous pouvez étendre la logique pour gérer ces cas de la même manière.

## Conclusion
Dans ce didacticiel, nous avons exploré comment extraire des vignettes de fichiers PSD à l'aide d'Aspose.PSD pour Java. En suivant les étapes décrites ci-dessus, vous pouvez récupérer et enregistrer efficacement les vignettes intégrées dans vos documents PSD.

## FAQ
### Qu’est-ce qu’Aspose.PSD ?
Aspose.PSD est une bibliothèque Java qui permet aux développeurs de travailler avec PSD et d'autres formats de fichiers image par programme.
### Où puis-je trouver plus de documentation sur Aspose.PSD pour Java ?
 Vous pouvez vous référer au[documentation](https://reference.aspose.com/psd/java/) pour des références API détaillées et des exemples.
### Puis-je essayer Aspose.PSD gratuitement avant d’acheter ?
 Oui, vous pouvez télécharger un[essai gratuit](https://releases.aspose.com/) pour évaluer les capacités de la bibliothèque.
### Comment puis-je obtenir des licences temporaires pour Aspose.PSD ?
 Des licences temporaires peuvent être obtenues auprès de[ici](https://purchase.aspose.com/temporary-license/).
### Aspose.PSD est-il adapté à un usage commercial ?
Oui, Aspose.PSD peut être utilisé pour des projets personnels et commerciaux selon ses conditions de licence.