---
date: 2026-10-08
description: 'Tutoriel de traitement d''images Java : apprenez à manipuler les fichiers
  PSD et à les enregistrer au format JPEG à l''aide d''Aspose.PSD. Guide étape par
  étape avec des exemples de code pour les débutants et les professionnels.'
keywords:
- java image processing tutorial
- Aspose.PSD
- 2 bit JPEG
- 7 bit JPEG
lastmod: 2026-10-08
linktitle: Prise en charge des JPEG 2 et 7 bits en Java
og_description: 'Tutoriel de traitement d''images Java : apprenez à manipuler les
  fichiers PSD et à les enregistrer au format JPEG à l''aide d''Aspose.PSD. Étapes
  détaillées, réponses rapides et dépannage pour les développeurs.'
og_image_alt: Guide to processing 2‑ and 7‑bit JPEG images in Java with Aspose.PSD
og_title: 'Tutoriel de traitement d''images Java : prise en charge des JPEG 2 bits
  et 7 bits'
schemas:
- author: Aspose
  dateModified: '2026-10-08'
  description: 'Java image processing tutorial: learn how to manipulate PSD files
    and save them as JPEGs using Aspose.PSD. Step‑by‑step guide with code examples
    for beginners and pros.'
  headline: 'Java image processing tutorial: support 2‑ and 7‑bit JPEGs'
  type: TechArticle
- description: 'Java image processing tutorial: learn how to manipulate PSD files
    and save them as JPEGs using Aspose.PSD. Step‑by‑step guide with code examples
    for beginners and pros.'
  name: 'Java image processing tutorial: support 2‑ and 7‑bit JPEGs'
  steps:
  - name: '**Java Development Kit (JDK)** – version 8 or higher.'
    text: '**Java Development Kit (JDK)** – version 8 or higher.'
  - name: '**Aspose.PSD for Java library** – you can [download it here](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – you can [download it here](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
  - name: '**Sample PSD file** – any PSD you wish to convert.'
    text: '**Sample PSD file** – any PSD you wish to convert.'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a commercial library that enables creation, manipulation,
      and conversion of Photoshop PSD files directly from Java applications.
    question: What is Aspose.PSD for Java?
  - answer: You can download the library from the [website](https://releases.aspose.com/psd/java/)
      and add the JAR to your project’s build path or Maven/Gradle dependencies.
    question: How do I install Aspose.PSD for Java?
  - answer: Yes, you can load custom RGB or CMYK ICC profiles and assign them to the
      `JpegOptions` before saving.
    question: Can I use custom color profiles with Aspose.PSD for Java?
  - answer: It supports PSD, JPEG, PNG, BMP, TIFF, GIF, and over 20 additional raster
      formats.
    question: What image formats does Aspose.PSD for Java support?
  - answer: Yes, you can download a [free trial](https://releases.aspose.com/) to
      evaluate the library before purchasing a license.
    question: Is there a free trial available for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- Aspose.PSD
- JPEG conversion
title: 'Tutoriel de traitement d''images Java : prise en charge des JPEG 2 bits et
  7 bits'
url: /fr/java/java-jpeg-image-processing/support-2-7-bits-jpeg-java/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tutoriel de traitement d'images Java : prise en charge des JPEG 2‑bits et 7‑bits

## Introduction
Dans ce **tutoriel de traitement d'images Java**, vous découvrirez comment utiliser la bibliothèque Aspose.PSD for Java pour charger un fichier PSD et l'exporter en JPEG 2‑bits ou 7‑bits. Que vous construisiez un service de conversion par lots ou que vous ayez besoin d'un contrôle fin de la qualité d'image, les étapes ci‑dessous vous guident de la configuration de l'environnement jusqu'à l'enregistrement du JPEG final. Commençons !

## Réponses rapides
- **Quelle bibliothèque gère les JPEG 2‑bits et 7‑bits ?** Aspose.PSD for Java.  
- **Version minimale de Java ?** JDK 8 ou ultérieure.  
- **Ai‑je besoin d'une licence pour le développement ?** Un essai gratuit suffit pour l'évaluation ; une licence commerciale est requise pour la production.  
- **Puis‑je changer le mode couleur ?** Oui – CMYK, YCCK et d’autres modes sont pris en charge via `JpegCompressionColorMode`.  
- **Quelle réduction de taille de fichier puis‑je attendre ?** Utiliser 2 bits par canal peut réduire le JPEG jusqu'à 80 % par rapport à une sortie 8 bits.

## Qu'est‑ce qu'un tutoriel de traitement d'images Java ?
Un tutoriel de traitement d'images Java est un guide pas à pas qui enseigne aux développeurs comment manipuler programmétiquement des données d'image en Java. Il couvre le chargement de divers formats, l'application de transformations, le réglage des paramètres de couleur et de compression, et l'enregistrement des résultats, vous permettant de créer des flux de travail personnalisés de gestion d'images.

## Pourquoi utiliser Aspose.PSD for Java ?
Aspose.PSD for Java fournit une API complète pour travailler avec les fichiers Photoshop sans nécessiter Photoshop lui‑même. Elle prend en charge plus de 30 formats d'image, gère des fichiers jusqu'à 2 Go en diffusant les données, et offre un contrôle fin sur les calques, les canaux et les profils couleur, ce qui la rend idéale pour le traitement côté serveur haute performance.

## Prérequis
Avant de commencer, assurez‑vous que vous disposez de ce qui suit :

1. **Java Development Kit (JDK)** – version 8 ou supérieure.  
2. **Bibliothèque Aspose.PSD for Java** – vous pouvez [la télécharger ici](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse ou NetBeans.  
4. **Fichier PSD d'exemple** – tout PSD que vous souhaitez convertir.  
5. **Connaissances de base en Java** – familiarité avec les classes, les objets et la gestion des exceptions.

## Importer les packages
Tout d'abord, ajoutez le JAR Aspose.PSD au classpath de votre projet. Ensuite, importez les espaces de noms requis :

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.jpeg.JpegCompressionColorMode;
import com.aspose.psd.fileformats.jpeg.JpegCompressionMode;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.JpegOptions;
```

## Comment charger une image PSD en Java ?
Pour charger un fichier PSD, appelez la méthode statique `load` de la classe `Image` et convertissez le résultat en `PsdImage`. Cela crée une représentation en mémoire du document Photoshop, vous donnant accès à ses calques, canaux, masques et métadonnées, que vous pouvez ensuite manipuler ou exporter vers d'autres formats.

`PsdImage` est la classe principale d'Aspose.PSD qui représente un document Photoshop en mémoire, permettant des opérations de lecture/écriture sur son contenu.

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "PsdImage.psd");
```

## Comment configurer les options JPEG pour une sortie 2‑bits ou 7‑bits ?
Créez une nouvelle instance de `JpegOptions` et définissez ses propriétés pour correspondre à la sortie souhaitée. Utilisez `setColorType` pour choisir le `JpegCompressionColorMode` approprié (par ex., CMYK ou YCCK), et `setCompressionType` pour sélectionner l'algorithme de compression. Enfin, attribuez la valeur `bitsPerChannel` (2 ou 7) pour contrôler la profondeur de bits de chaque canal couleur.

```java
JpegOptions options = new JpegOptions();
options.setColorType(JpegCompressionColorMode.Cmyk);
options.setCompressionType(JpegCompressionMode.JpegLs);
```

## Comment définir les bits par canal pour les JPEG à faible profondeur de bits ?
`bitsPerChannel` spécifie le nombre de bits utilisés pour chaque canal couleur dans le JPEG de sortie. Définir cette propriété à 2 réduit chaque canal à deux bits, produisant une image fortement compressée avec un banding visible, tandis qu'une valeur de 7 conserve plus de détails et donne une taille de fichier intermédiaire entre les sorties à très faible profondeur de bits et les sorties standard 8 bits. Choisissez la valeur qui équilibre qualité et taille pour votre cas d'utilisation.

```java
byte bpp = 2;
options.setBitsPerChannel(bpp);
```

## Comment appliquer des profils couleur (facultatif) ?
`ICCProfile` représente un profil International Color Consortium qui décrit les caractéristiques colorimétriques d'un dispositif ou d'un espace de travail. Si vous avez un fichier ICC personnalisé, chargez‑le avec `ICCProfile.getInstance(path)` et affectez‑le à la propriété `iccProfile` de l'objet `jpegOptions`. Laisser la propriété à null fait qu'Aspose.PSD utilise le profil système par défaut, ce qui fonctionne dans la plupart des scénarios.

```java
options.setRgbColorProfile(null);
options.setCmykColorProfile(null);
```

## Comment enregistrer l'image traitée en JPEG ?
La méthode `save` écrit l'image dans un fichier en utilisant les options fournies. Appelez‑la sur l'instance `PsdImage`, en passant le nom de fichier cible (avec l'extension .jpg) et les `JpegOptions` configurés. La bibliothèque gère l'encodage, l'application des bits‑par‑canal et du profil couleur sélectionnés, et produit un JPEG qui correspond à vos spécifications.

```java
image.save(dataDir + "2_7BitsJPEG_output.jpg", options);
```

## Problèmes courants et solutions
- **Erreur fichier trop volumineux** – Assurez‑vous d'utiliser la dernière version d'Aspose.PSD, qui diffuse les données et évite de charger le fichier entier en RAM.  
- **Couleurs inattendues** – Vérifiez que le `JpegCompressionColorMode` sélectionné correspond à l'espace couleur de votre image source.  
- **Profil ICC manquant** – Si vous avez besoin d'un profil spécifique, chargez‑le avec `ICCProfile.getInstance(path)` et affectez‑le aux `JpegOptions`.

## Questions fréquemment posées

**Q : Qu'est‑ce qu'Aspose.PSD for Java ?**  
A : Aspose.PSD for Java est une bibliothèque commerciale qui permet la création, la manipulation et la conversion de fichiers Photoshop PSD directement depuis des applications Java.

**Q : Comment installer Aspose.PSD for Java ?**  
A : Vous pouvez télécharger la bibliothèque depuis le [site web](https://releases.aspose.com/psd/java/) et ajouter le JAR au chemin de construction de votre projet ou aux dépendances Maven/Gradle.

**Q : Puis‑je utiliser des profils couleur personnalisés avec Aspose.PSD for Java ?**  
A : Oui, vous pouvez charger des profils ICC RGB ou CMYK personnalisés et les affecter aux `JpegOptions` avant l'enregistrement.

**Q : Quels formats d'image Aspose.PSD for Java prend‑il en charge ?**  
A : Il prend en charge PSD, JPEG, PNG, BMP, TIFF, GIF et plus de 20 formats raster supplémentaires.

**Q : Une version d'essai gratuite est‑elle disponible pour Aspose.PSD for Java ?**  
A : Oui, vous pouvez télécharger un [essai gratuit](https://releases.aspose.com/) pour évaluer la bibliothèque avant d'acheter une licence.

---

**Dernière mise à jour :** 2026-10-08  
**Testé avec :** Aspose.PSD 24.12 for Java  
**Auteur :** Aspose

## Tutoriels associés

- [Traitement d'images Java – Prise en charge du JPEG-LS avec CMYK](/psd/java/java-jpeg-image-processing/support-jpeg-ls-cmyk-java/)
- [Enregistrer PSD en JPEG et prise en charge de la couleur RVB avec Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)
- [Comment convertir PSD en formats d'image raster avec Aspose.PSD for Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}