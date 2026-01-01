---
date: 2026-01-01
description: Apprenez à créer un bitmap Java à l'aide d'un flux dans Aspose.PSD, à
  enregistrer un fichier image Java et à définir le nombre de bits par pixel efficacement.
linktitle: Create Image using Stream
second_title: Aspose.PSD Java API
title: Créer un bitmap Java avec Stream dans Aspose.PSD
url: /fr/java/image-editing/create-image-using-stream/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Créer un bitmap Java en utilisant le flux dans Aspose.PSD

## Introduction

Si vous devez **créer des images bitmap Java** à la volée, Aspose.PSD pour Java vous propose une approche basée sur les flux, à la fois rapide et efficace en mémoire. Dans ce tutoriel, nous parcourrons la génération d’une image bitmap à partir d’un flux, la configuration des bits par pixel, puis **enregistrer le fichier image Java** sur le disque. À la fin, vous comprendrez pourquoi cette méthode est idéale pour le traitement d’images côté serveur, les travaux batch ou tout scénario où vous souhaitez éviter les fichiers temporaires.

## Réponses rapides
- **Que signifie « créer bitmap java » ?** Cela désigne la génération programmatique d’une image BMP à l’aide de code Java.  
- **Quelle bibliothèque gère le flux ?** Les classes `StreamSource` et `FileCreateSource` d’Aspose.PSD.  
- **Puis‑je définir la profondeur de couleur ?** Oui – utilisez `BmpOptions.setBitsPerPixel(int)` (par ex., 24 bpp).  
- **Comment enregistrer le résultat ?** Appelez `image.save(outputPath)` pour **enregistrer le fichier image Java**.  
- **Une licence est‑elle requise pour la production ?** Une licence valide d’Aspose.PSD est nécessaire pour une utilisation commerciale.

## Prérequis pour créer bitmap java

Avant de commencer, assurez‑vous d’avoir :

- **Java Development Kit (JDK)** – toute version récente (8 ou supérieure).  
- **Aspose.PSD pour Java** – téléchargez le dernier JAR depuis la [documentation](https://reference.aspose.com/psd/java/).  
- **IDE** – Eclipse, IntelliJ IDEA, ou tout éditeur compatible Java que vous préférez.

## Importer les packages pour la génération de bitmap

Commencez par importer les espaces de noms requis. Ils vous donnent accès à la création d’images, aux options BMP et à la gestion des flux.

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.BmpOptions;
import com.aspose.psd.sources.FileCreateSource;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.FileMode;
import com.aspose.psd.system.io.FileStream;
import com.aspose.psd.system.io.Stream;
import java.io.FileInputStream;
```

## Étape 1 : Configurer le répertoire du document

```java
String dataDir = "Your Document Directory";
```

Remplacez `"Your Document Directory"` par le chemin absolu où vous conservez vos fichiers source et de sortie.

## Étape 2 : Définir le nom du fichier de sortie

```java
String desName = dataDir + "CreatingImageUsingStream_out.bmp";
```

C’est le chemin où l’opération **enregistrer le fichier image Java** écrira le bitmap.

## Étape 3 : Configurer BmpOptions (définir les bits par pixel)

```java
BmpOptions imageOptions = new BmpOptions();
imageOptions.setBitsPerPixel(24);
```

Ici nous **définissons les bits par pixel** à 24 bpp, ce qui produit un bitmap en couleur vraie. Ajustez la valeur si vous avez besoin d’une profondeur de couleur différente.

## Étape 4 : Créer un FileCreateSource (source de flux)

```java
FileCreateSource stream = new FileCreateSource(dataDir + "sample_out.bmp");
imageOptions.setSource(stream);
```

`FileCreateSource` encapsule un flux de fichier afin qu’Aspose.PSD puisse écrire directement vers la destination sans tampons intermédiaires.

## Étape 5 : Générer l’image bitmap

```java
Image image = Image.create(imageOptions, 500, 500);
```

Cette ligne **génère une image bitmap Java** de 500 × 500 pixels en utilisant les options définies précédemment.

## Étape 6 : Effectuer le traitement d’image et enregistrer

```java
// Perform desired image processing operations here
// For example, you could draw shapes, apply filters, etc.

// Save the processed bitmap to disk
image.save(desName);
```

Après toute manipulation optionnelle, l’appel à `image.save` **enregistre le fichier image Java** à l’emplacement spécifié dans `desName`.

## Conclusion

Vous avez maintenant appris comment **créer des images bitmap Java** en utilisant des flux dans Aspose.PSD, contrôler la profondeur de couleur avec **set bits per pixel**, et **enregistrer le fichier image Java** de manière efficace. Expérimentez avec différentes dimensions, formats de pixel ou étapes de traitement supplémentaires pour répondre aux besoins de votre projet.

## Foire aux questions

### Q1 : Puis‑je utiliser Aspose.PSD avec d’autres bibliothèques Java ?

R1 : Oui, Aspose.PSD est conçu pour s’intégrer de façon transparente avec d’autres bibliothèques Java, offrant une grande polyvalence dans vos projets.

### Q2 : Où puis‑je trouver du support pour les questions relatives à Aspose.PSD ?

R2 : Visitez le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour le support communautaire et les discussions.

### Q3 : Existe‑t‑il un essai gratuit d’Aspose.PSD ?

R3 : Oui, vous pouvez accéder à un essai gratuit [ici](https://releases.aspose.com/).

### Q4 : Comment obtenir une licence temporaire pour Aspose.PSD ?

R4 : Obtenez une licence temporaire [ici](https://purchase.aspose.com/temporary-license/).

### Q5 : Quelles sont les exigences système pour Aspose.PSD ?

R5 : Consultez la [documentation](https://reference.aspose.com/psd/java/) pour les exigences système détaillées.

---

**Dernière mise à jour :** 2026-01-01  
**Testé avec :** Aspose.PSD Java dernière version  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}