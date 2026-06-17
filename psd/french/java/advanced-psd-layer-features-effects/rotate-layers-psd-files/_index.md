---
date: 2026-02-17
description: Apprenez à convertir les fichiers PSD en PNG, à préserver la transparence
  du PNG et à faire pivoter les calques PSD en Java avec Aspose.PSD. Guide étape par
  étape avec des exemples de code.
linktitle: Convert PSD to PNG and Rotate Layers in PSD Files using Java
second_title: Aspose.PSD Java API
title: Convertir PSD en PNG et faire pivoter les calques dans les fichiers PSD avec
  Java
url: /fr/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir PSD en PNG et faire pivoter les calques dans les fichiers PSD avec Java

## Introduction
Si vous devez **convertir PSD en PNG** tout en faisant pivoter les calques, ce guide est fait pour vous. Que vous construisiez un outil de traitement par lots, un service web nécessitant une manipulation d’image à la volée, ou que vous automatisiez simplement un flux de travail de conception, le faire de façon programmatique fait gagner du temps et supprime la dépendance à Adobe Photoshop. Dans ce tutoriel, nous allons parcourir **comment faire pivoter les calques PSD** et exporter le résultat en PNG en utilisant la bibliothèque Aspose.PSD pour Java. Enroulons nos manches et faisons fonctionner votre flux de travail de conception sans accroc !

## Quick Answers
- **Quelle bibliothèque puis‑je utiliser ?** Aspose.PSD pour Java  
- **Puis‑je à la fois faire pivoter et convertir en une seule opération ?** Oui – faites pivoter le PSD puis enregistrez‑le en PNG  
- **Ai‑je besoin d’une licence ?** Un essai gratuit suffit pour les tests ; une licence payante est requise en production  
- **Quelle version de Java est prise en charge ?** Java 8 et ultérieure  
- **Le PNG de sortie est‑il transparent ?** Oui, lorsque vous définissez `PngColorType.TruecolorWithAlpha`

## What is “convert PSD to PNG”?
Convertir un document Photoshop (PSD) en image PNG signifie extraire le contenu visuel — y compris tous les calques, masques et la transparence — dans un format raster largement supporté. Le PNG conserve les canaux alpha, ce qui le rend idéal pour les graphiques web, les miniatures et les traitements d’image ultérieurs.

## Why use Aspose.PSD for Java to convert PSD to PNG and rotate PSD layers?
- **Pas besoin de Photoshop** – fonctionne sur n’importe quel serveur ou environnement CI  
- **Prise en charge complète des calques** – conserve la transparence et les effets de calque intacts  
- **API simple** – faites pivoter, retournez et enregistrez avec seulement quelques appels de méthode  
- **Cross‑platform** – s’exécute sous Windows, Linux et macOS  
- **Java image conversion** rendue facile avec une seule bibliothèque  

## Prerequisites
Avant de plonger dans le code, assurez‑vous de disposer de :

- **Java Development Kit (JDK)** – téléchargez‑le depuis le [site d’Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **Environnement de développement intégré (IDE)** – IntelliJ IDEA, Eclipse ou NetBeans conviennent tous.  
- **Bibliothèque Aspose.PSD pour Java** – obtenez le JAR le plus récent depuis la [page de publication](https://releases.aspose.com/psd/java/).  
- **Connaissances de base en Java** – familiarité avec les classes, objets et la gestion des exceptions.

## Step‑by‑Step Guide

### Step 1: Set Up Your Java Project
Créez un nouveau projet Java dans votre IDE et ajoutez le JAR Aspose.PSD au chemin de construction du projet.

### Step 2: Import Required Classes
Ajoutez les importations suivantes en haut de votre fichier source Java :

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Ces classes vous donnent accès au chargement d’image, à la rotation et aux options spécifiques au PNG.

### Step 3: Define File Paths
Spécifiez où se trouve votre PSD source et où les fichiers de sortie doivent être écrits.

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **Pro tip :** Utilisez un chemin absolu lors des tests pour éviter les erreurs « file not found ».

### Step 4: Load the PSD File
Chargez le PSD dans un objet manipulable.

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

Maintenant, `im` représente l’ensemble du document Photoshop, y compris tous les calques.

### Step 5: Rotate the Image (How to rotate PSD)
Choisissez un type de rotation parmi `RotateFlipType`. Dans cet exemple, nous faisons pivoter de 270° et retournons les deux axes.

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

N’hésitez pas à expérimenter d’autres valeurs comme `Rotate90FlipNone` ou `Rotate180FlipX`. C’est la partie **how to rotate PSD** du tutoriel.

### Step 6: Save the Rotated Image as PNG (convert PSD to PNG)
Configurez les options PNG pour conserver la transparence, puis enregistrez.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

Le PNG résultant conserve la transparence du calque, assurant **preserve PNG transparency** pour les utilisations en aval.

### Step 7: Save the Modified PSD (optional)
Si vous avez également besoin d’un nouveau PSD avec la rotation appliquée, enregistrez‑le à nouveau.

```java
im.save(psdPath);
```

Vous disposez maintenant d’un aperçu PNG et d’un fichier PSD mis à jour.

## Common Issues and Solutions
- **File not found :** Vérifiez que `dataDir` se termine par un séparateur de chemin (`/` ou `\`).  
- **OutOfMemoryError sur de gros PSD :** Augmentez la taille du tas JVM (`-Xmx2g`).  
- **Transparency lost :** Assurez‑vous que `PngColorType.TruecolorWithAlpha` est défini ; sinon le PNG sera enregistré sans canal alpha.  
- **Flip PSD image not behaving as expected :** Revérifiez la constante `RotateFlipType` que vous avez sélectionnée ; certaines constantes combinent rotation et retournement en une seule étape.

## Frequently Asked Questions

**Q : Puis‑je faire pivoter un calque spécifique dans un fichier PSD ?**  
R : Oui, vous pouvez utiliser `Layer.rotateFlip()` sur des calques individuels après avoir parcouru `im.getLayers()`.

**Q : Existe‑t‑il une limitation de performance avec Aspose.PSD pour Java ?**  
R : La bibliothèque gère la plupart des fichiers efficacement, mais les PSD extrêmement volumineux (> 500 Mo) peuvent nécessiter plus de mémoire.

**Q : Aspose.PSD est‑il gratuit à utiliser ?**  
R : Aspose propose un essai gratuit, mais une licence payante est nécessaire en production. Consultez la [licence temporaire](https://purchase.aspose.com/temporary-license/) pour les tests.

**Q : Où puis‑je trouver une documentation détaillée ?**  
R : Vous trouverez une documentation complète sur [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).

**Q : Que faire si je rencontre des problèmes en utilisant Aspose.PSD ?**  
R : Demandez de l’aide via le [Aspose Support Forum](https://forum.aspose.com/c/psd/34).

**Q : La conversion PSD en PNG préserve‑t‑elle les effets de calque ?**  
R : Oui, lorsque vous enregistrez avec `PngColorType.TruecolorWithAlpha`, la plupart des effets visuels sont rasterisés dans le PNG.

**Q : Puis‑je traiter plusieurs fichiers PSD en lot ?**  
R : Absolument. Enveloppez le code dans une boucle qui parcourt un répertoire de fichiers PSD.

**Q : Est‑il possible de définir le niveau de compression PNG ?**  
R : La classe `PngOptions` propose une méthode `setCompressionLevel(int)` pour affiner le réglage.

**Q : Dois‑je fermer l’objet image ?**  
R : `PsdImage` implémente `Closeable` ; appelez `im.close()` dans un bloc `finally` ou utilisez le try‑with‑resources.

**Q : Le PNG pivoté aura‑t‑il les mêmes dimensions que l’original ?**  
R : Une rotation de 90° ou 270° échange largeur et hauteur. Le PNG reflétera la nouvelle orientation.

## Conclusion
En exploitant Aspose.PSD pour Java, vous pouvez **convertir PSD en PNG**, **préserver la transparence PNG** et **faire pivoter les calques PSD** en quelques lignes de code seulement. Cette approche élimine le besoin de Photoshop, accélère les flux de travail automatisés et vous donne un contrôle total sur la sortie d’image. Essayez‑le sur vos propres projets et constatez le temps gagné !

---

**Last Updated:** 2026-02-17  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}