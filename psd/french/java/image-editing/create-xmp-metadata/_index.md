---
date: 2026-01-01
description: Apprenez à créer des métadonnées XMP, à ajouter XMP aux fichiers PSD
  et à mettre à jour les métadonnées d’image avec Aspose.PSD pour Java. Suivez dès
  maintenant ce guide pas à pas.
linktitle: Create XMP Metadata
second_title: Aspose.PSD Java API
title: Créer des métadonnées XMP avec Aspose.PSD pour Java
url: /fr/java/image-editing/create-xmp-metadata/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Créer des métadonnées XMP avec Aspose.PSD pour Java

## Introduction

La gestion des métadonnées d'image est une exigence courante pour les développeurs Java qui travaillent avec des fichiers Photoshop (PSD). Dans ce tutoriel, vous apprendrez **comment créer des métadonnées XMP** en utilisant la bibliothèque Aspose.PSD, ajouter XMP à une image PSD, et mettre à jour les métadonnées d'image de façon programmatique. Nous parcourrons chaque étape, expliquerons pourquoi chaque élément est important, et vous donnerons des conseils pratiques que vous pourrez appliquer dans de vrais projets.

## Réponses rapides
- **Qu'est-ce que les métadonnées XMP ?** Un format standardisé pour intégrer des informations descriptives (auteur, mots‑clés, etc.) à l'intérieur des fichiers image.  
- **Pourquoi utiliser Aspose.PSD ?** Il fournit une API pure‑Java pour créer, lire et modifier des fichiers PSD sans Photoshop.  
- **Puis‑je ajouter XMP à un PSD existant ?** Oui – vous pouvez mettre à jour les métadonnées d'image à la volée avec `setXmpData`.  
- **Quelles sont les étapes principales ?** Définir la taille de l'image, créer l'en‑tête/la fin, construire les paquets XMP, les attacher, puis enregistrer.  
- **Ai‑je besoin d'une licence ?** Un essai gratuit suffit pour le développement ; une licence commerciale est requise pour la production.

## Qu'est‑ce que « créer des métadonnées XMP » en Java ?

Créer des métadonnées XMP signifie construire un paquet XMP (en‑tête, corps, fin) qui décrit l'image, puis intégrer ce paquet dans un fichier PSD. La bibliothèque Aspose.PSD abstrait les détails de bas niveau, vous permettant de vous concentrer sur le contenu que vous souhaitez stocker.

## Pourquoi ajouter XMP aux fichiers PSD ?

- **Recherchabilité :** Permet des recherches puissantes de gestion d'actifs basées sur l'auteur, le titre ou des balises personnalisées.  
- **Interopérabilité :** XMP est reconnu par les produits Adobe, Lightroom et de nombreux systèmes DAM.  
- **Contrôle de version :** Stocke l'historique de traitement (par ex., ville, mode couleur) directement dans le fichier.

## Prérequis

- **Environnement de développement Java :** JDK 8 ou supérieur installé et une compréhension de base de Java.  
- **Bibliothèque Aspose.PSD :** Téléchargez et configurez la bibliothèque Aspose.PSD pour Java. Vous pouvez trouver la bibliothèque et la documentation détaillée [ici](https://reference.aspose.com/psd/java/).  
- **Votre répertoire de documents :** Décidez où vous lirez/écrirez les fichiers PSD sur votre système.

## Importer les packages

Dans votre projet Java, importez les packages nécessaires pour exploiter les fonctionnalités d'Aspose.PSD :

```java
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.system.io.MemoryStream;
import com.aspose.psd.xmp.XmpHeaderPi;
import com.aspose.psd.xmp.XmpMeta;
import com.aspose.psd.xmp.XmpPacketWrapper;
import com.aspose.psd.xmp.XmpTrailerPi;
import com.aspose.psd.xmp.schemas.dublincore.DublinCorePackage;
import com.aspose.psd.xmp.schemas.photoshop.ColorMode;
import com.aspose.psd.xmp.schemas.photoshop.PhotoshopPackage;
```

## Étape 1 : Spécifier la taille de l'image

Tout d'abord, définissez les dimensions du canevas pour la nouvelle image PSD.

```java
// Specify the size of the image by defining a Rectangle
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## Étape 2 : Créer une nouvelle image

Créez une image PSD vierge que nous enrichirons ensuite avec des métadonnées XMP.

```java
// Create a brand new image for sample purposes
PsdImage image = new PsdImage(rect.getWidth(), rect.getHeight());
```

## Étape 3 : Créer l'en‑tête XMP

L'en‑tête contient l'instruction de traitement XML d'ouverture et un GUID qui identifie le document.

```java
// Create an instance of XMP-Header
XmpHeaderPi xmpHeader = new XmpHeaderPi();
xmpHeader.setGuid("Your Document Directory");
```

## Étape 4 : Créer la fin XMP

La fin marque la fin du paquet XMP. Définir le drapeau `true` écrit l'instruction de traitement de fermeture.

```java
// Create an instance of Xmp-TrailerPi 
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## Étape 5 : Créer les métadonnées XMP

Ajoutez des attributs génériques tels que l'auteur et la description à l'objet de métadonnées XMP de base.

```java
// Create an instance of XMPmeta class to set different attributes
XmpMeta xmpMeta = new XmpMeta();
xmpMeta.addAttribute("Author", "Mr Smith");
xmpMeta.addAttribute("Description", "The fake metadata value");
```

## Étape 6 : Créer l'enveloppe du paquet XMP

Enveloppez l'en‑tête, la fin et les métadonnées de base dans un seul paquet qui peut être attaché à l'image.

```java
// Create an instance of XmpPacketWrapper that contains all metadata
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Étape 7 : Définir les attributs Photoshop

Remplissez les champs spécifiques à Photoshop (ville, pays, mode couleur) que de nombreux outils Adobe attendent.

```java
// Create an instance of Photoshop package and set Photoshop attributes
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.setCity("London");
photoshopPackage.setCountry("England");
photoshopPackage.setColorMode(ColorMode.Rgb);
```

## Étape 8 : Ajouter le paquet Photoshop aux métadonnées XMP

Attachez le paquet Photoshop au paquet XMP.

```java
// Add Photoshop package into XMP metadata
xmpData.addPackage(photoshopPackage);
```

## Étape 9 : Définir les attributs DublinCore

Ajoutez des métadonnées Dublin Core telles que l'auteur, le titre et une balise personnalisée de film.

```java
// Create an instance of DublinCore package and set DublinCore attributes
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.setAuthor("Charles Bukowski");
dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.addValue("dc:movie", "Barfly");
```

## Étape 10 : Ajouter le paquet DublinCore aux métadonnées XMP

Combinez le paquet Dublin Core avec le paquet XMP existant.

```java
// Add DublinCore Package into XMP metadata
xmpData.addPackage(dublinCorePackage);
```

## Étape 11 : Mettre à jour les métadonnées XMP dans l'image

Intégrez maintenant le paquet XMP complet dans l'image PSD.

```java
// Update XMP metadata into the image
image.setXmpData(xmpData);
```

## Étape 12 : Enregistrer l'image

Enfin, écrivez le fichier PSD sur le disque (ou un flux mémoire) afin que les métadonnées soient persistées.

```java
// Save the image on the disk or in a memory stream
image.save("Your Document Directory" + "create_XMP_Metadata.psd");
```

## Problèmes courants et solutions

| Problème | Pourquoi cela se produit | Solution |
|----------|--------------------------|----------|
| **`NullPointerException` on `setXmpData`** | Le paquet XMP n'était pas entièrement construit (en‑tête/fin manquants). | Assurez‑vous de créer `XmpHeaderPi`, `XmpTrailerPi` et d'ajouter tous les paquets avant d'appeler `setXmpData`. |
| **Metadata not visible in Photoshop** | Photoshop attend que le paquet XMP soit correctement enveloppé. | Vérifiez que `XmpTrailerPi(true)` est utilisé et que le paquet est enregistré avec l'image. |
| **File path errors** | Utilisation d'un chemin relatif sans les permissions appropriées. | Utilisez un chemin absolu ou assurez‑vous que l'application a les droits d'écriture sur le dossier cible. |

## Questions fréquentes

**Q : Aspose.PSD est‑il compatible avec différents formats d'image ?**  
**R :** Oui, Aspose.PSD prend en charge PSD, PSB, BMP, GIF, JPEG, PNG, TIFF, et plus encore, vous offrant une flexibilité entre les formats.

**Q : Puis‑je manipuler les métadonnées existantes avec Aspose.PSD ?**  
**R :** Absolument. Vous pouvez charger un PSD existant, récupérer ses données XMP avec `getXmpData()`, modifier le paquet, puis le sauvegarder.

**Q : Existe‑t‑il des limites concernant la taille d'image que Aspose.PSD peut gérer ?**  
**R :** Aspose.PSD est conçu pour travailler avec de très grandes images (jusqu'à plusieurs gigapixels), limitées uniquement par la mémoire disponible.

**Q : Une version d'essai d'Aspose.PSD est‑elle disponible ?**  
**R :** Oui, vous pouvez explorer les capacités d'Aspose.PSD en obtenant un essai gratuit [ici](https://releases.aspose.com/).

**Q : Où puis‑je obtenir de l'aide pour les questions liées à Aspose.PSD ?**  
**R :** Pour toute assistance ou question, consultez le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

## Conclusion

Vous avez maintenant maîtrisé **comment créer des métadonnées XMP**, ajouter XMP à un PSD, et mettre à jour les métadonnées d'image en utilisant Aspose.PSD pour Java. Ces étapes vous donnent un contrôle complet sur les informations descriptives intégrées à vos images, les rendant recherchables, indexables et prêtes pour les flux de travail en aval. N'hésitez pas à expérimenter avec des schémas XMP supplémentaires ou à intégrer ce code dans des pipelines de traitement d'image plus vastes.

---

**Dernière mise à jour :** 2026-01-01  
**Testé avec :** Aspose.PSD for Java 24.12  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}