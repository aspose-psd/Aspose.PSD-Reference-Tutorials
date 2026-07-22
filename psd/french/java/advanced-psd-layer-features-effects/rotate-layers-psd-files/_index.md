---
date: 2026-07-22
description: Apprenez comment enregistrer un PSD en PNG, préserver la transparence
  du PNG et faire pivoter les calques PSD en Java avec Aspose.PSD. Guide étape par
  étape, explications sans code et conseils de dépannage.
keywords:
- save psd as png
- export psd layers png
- convert photoshop file png
- psd to png transparency
lastmod: 2026-07-22
linktitle: enregistrer un PSD en PNG et faire pivoter les calques en Java avec Aspose.PSD
og_description: enregistrez un PSD en PNG avec Aspose.PSD pour Java. Préservez la
  transparence, faites pivoter les calques et exportez le PNG en quelques lignes de
  code seulement—idéal pour les flux de travail automatisés.
og_image_alt: 'Developer guide: save PSD as PNG and rotate layers using Aspose.PSD
  for Java'
og_title: enregistrer un PSD en PNG et faire pivoter les calques en Java avec Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to save psd as png, preserve PNG transparency, and rotate
    PSD layers in Java with Aspose.PSD. Step‑by‑step guide, code‑free explanations,
    and troubleshooting tips.
  headline: save psd as png and rotate layers in Java using Aspose.PSD
  type: TechArticle
- description: Learn how to save psd as png, preserve PNG transparency, and rotate
    PSD layers in Java with Aspose.PSD. Step‑by‑step guide, code‑free explanations,
    and troubleshooting tips.
  name: save psd as png and rotate layers in Java using Aspose.PSD
  steps:
  - name: Set Up Your Java Project
    text: Create a new Java project in your IDE and add the Aspose.PSD JAR to the
      project’s build path.
  - name: Import Required Classes
    text: '`PsdImage` is the core class that represents a Photoshop document in memory.
      `PngOptions` controls PNG‑specific settings, and `RotateFlipType` defines rotation
      and flip operations. These imports give you access to image loading, rotation,
      and PNG‑specific options.'
  - name: Define File Paths
    text: Specify where your source PSD lives and where the output files should be
      written. Using absolute paths during testing avoids “file not found” errors.
      > **Pro tip:** Store paths in a configuration file for easier maintenance in
      larger projects.
  - name: Load the PSD File
    text: '`PsdImage` loads the entire Photoshop document, including all layers, masks,
      and effects, into a manipulable object. Now `im` represents the whole PSD, ready
      for transformations.'
  - name: Rotate the Image (How to rotate PSD)
    text: '`RotateFlipType` enumerates all supported rotations and flips. In this
      example we rotate 270° and flip both axes, which swaps width and height while
      mirroring the image. Feel free to experiment with other values such as `Rotate90FlipNone`
      or `Rotate180FlipX`.'
  - name: Save the Rotated Image as PNG (save PSD as PNG)
    text: Configure `PngOptions` to keep transparency (`PngColorType.TruecolorWithAlpha`)
      and then call `save`. The PNG retains layer transparency, ensuring it works
      seamlessly in web or mobile apps. The resulting PNG preserves alpha channels,
      making it suitable for compositing or further processing.
  - name: Save the Modified PSD (optional)
    text: If you also need a new PSD with the rotation applied, you can save the modified
      `PsdImage` back to disk. You now have both a PNG preview and an updated PSD
      file.
  type: HowTo
- questions:
  - answer: Yes, you can call `layer.rotateFlip(RotateFlipType.Rotate90FlipNone)`
      after iterating through `im.getLayers()`.
    question: Can I rotate a specific layer in a PSD file?
  - answer: The library handles most files efficiently, but extremely large PSDs (>500
      MB) may require additional memory or streaming options.
    question: Is there any performance limitation with Aspose.PSD for Java?
  - answer: Aspose offers a free trial, but a paid license is needed for production.
      See the [temporary license](https://purchase.aspose.com/temporary-license/)
      for testing.
    question: Is Aspose.PSD free to use?
  - answer: Comprehensive docs are available at [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find detailed documentation?
  - answer: Get help via the [Aspose Support Forum](https://forum.aspose.com/c/psd/34).
    question: What if I encounter issues while using Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert PSD
- Aspose.PSD
- Java image processing
- rotate PSD layers
title: enregistrer un PSD en PNG et faire pivoter les calques en Java avec Aspose.PSD
url: /fr/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

## Tutoriels associés

- [Enregistrer le PSD en PNG et appliquer l'ombre portée de rendu dans Aspose.PSD pour Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Comment compresser des fichiers PNG avec Aspose.PSD pour Java](/psd/java/optimizing-png-files/compress-png-files/)
- [Comment faire pivoter une image en Java avec Aspose.PSD](/psd/java/advanced-image-manipulation/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/pf/main-wrap-class >}}

# Enregistrer le PSD en PNG et faire pivoter les calques en Java avec Aspose.PSD

## Introduction
Si vous devez **enregistrer le PSD en PNG** tout en faisant pivoter les calques, ce guide est fait pour vous. Que vous construisiez un outil de traitement par lots, un service web nécessitant une manipulation d'images à la volée, ou que vous automatisiez simplement un flux de travail de conception, le faire de manière programmatique fait gagner du temps et supprime la dépendance à Adobe Photoshop. Dans ce tutoriel, nous allons parcourir **comment faire pivoter les calques PSD** et exporter le résultat en PNG en utilisant la bibliothèque Aspose.PSD pour Java. Enroulons nos manches et faisons fonctionner votre flux de travail de conception sans accroc !

## Réponses rapides
- **Quelle bibliothèque puis‑je utiliser ?** Aspose.PSD for Java  
- **Puis‑je à la fois faire pivoter et enregistrer le PSD en PNG en une seule fois ?** Oui – faites pivoter le PSD puis enregistrez‑le en PNG  
- **Ai‑je besoin d’une licence ?** Un essai gratuit suffit pour les tests ; une licence payante est requise pour la production  
- **Quelle version de Java est prise en charge ?** Java 8 et ultérieure  
- **La sortie PNG est‑elle transparente ?** Oui, lorsque vous définissez `PngColorType.TruecolorWithAlpha`

## Qu’est‑ce que « convertir PSD en PNG » ?
Convertir un document Photoshop (PSD) en image PNG extrait le contenu visuel — y compris les calques, masques et canaux alpha — dans un format raster largement supporté qui préserve la transparence. Cela rend le PNG idéal pour les graphiques web, les miniatures et le traitement d'images en aval. Le PNG résultant peut être utilisé directement dans les pages web, les applications mobiles, ou être traité davantage par d’autres bibliothèques d’images.

## Pourquoi utiliser Aspose.PSD pour Java afin d’enregistrer le PSD en PNG et de faire pivoter les calques PSD ?
Aspose.PSD vous permet d’**enregistrer le PSD en PNG** et de faire pivoter les calques sans installer Photoshop. Il prend en charge **plus de 50 formats d’entrée et de sortie**, traite des fichiers PSD de plusieurs centaines de pages en utilisant moins de 200 Mo de RAM, et fonctionne sous Windows, Linux et macOS. L’API ne nécessite que quelques appels de méthode, offrant des résultats haute fidélité avec une prise en charge intégrée des effets de calque, masques et canaux alpha.

## Prérequis
Avant de plonger dans le code, assurez-vous de disposer de ce qui suit :

- **Java Development Kit (JDK)** – téléchargez-le depuis le [site Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **Environnement de développement intégré (IDE)** – IntelliJ IDEA, Eclipse ou NetBeans conviennent tous.  
- **Bibliothèque Aspose.PSD pour Java** – obtenez le dernier JAR depuis la [page de version](https://releases.aspose.com/psd/java/).  
- **Connaissances de base en Java** – familiarité avec les classes, objets et la gestion des exceptions.

## Guide étape par étape

### Étape 1 : Configurer votre projet Java
Créez un nouveau projet Java dans votre IDE et ajoutez le JAR Aspose.PSD au chemin de construction du projet.

### Étape 2 : Importer les classes requises
`PsdImage` est la classe principale qui représente un document Photoshop en mémoire. `PngOptions` contrôle les paramètres spécifiques au PNG, et `RotateFlipType` définit les opérations de rotation et de retournement.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Ces imports vous donnent accès au chargement d’image, à la rotation et aux options spécifiques au PNG.

### Étape 3 : Définir les chemins de fichiers
Spécifiez où se trouve votre PSD source et où les fichiers de sortie doivent être écrits. Utiliser des chemins absolus pendant les tests évite les erreurs « fichier non trouvé ».

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **Astuce :** Stockez les chemins dans un fichier de configuration pour faciliter la maintenance dans les projets plus importants.

### Étape 4 : Charger le fichier PSD
`PsdImage` charge l’ensemble du document Photoshop, y compris tous les calques, masques et effets, dans un objet manipulable.

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

Maintenant, `im` représente le PSD complet, prêt pour les transformations.

### Étape 5 : Faire pivoter l’image (Comment faire pivoter le PSD)
`RotateFlipType` énumère toutes les rotations et retournements pris en charge. Dans cet exemple, nous faisons pivoter de 270° et retournons les deux axes, ce qui échange la largeur et la hauteur tout en miroir l’image.

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

N’hésitez pas à expérimenter d’autres valeurs comme `Rotate90FlipNone` ou `Rotate180FlipX`.

### Étape 6 : Enregistrer l’image pivotée en PNG (enregistrer le PSD en PNG)
Configurez `PngOptions` pour conserver la transparence (`PngColorType.TruecolorWithAlpha`) puis appelez `save`. Le PNG conserve la transparence des calques, garantissant son bon fonctionnement dans les applications web ou mobiles.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

Le PNG résultant préserve les canaux alpha, le rendant adapté au compositing ou à un traitement ultérieur.

### Étape 7 : Enregistrer le PSD modifié (optionnel)
Si vous avez également besoin d’un nouveau PSD avec la rotation appliquée, vous pouvez enregistrer le `PsdImage` modifié sur le disque.

```java
im.save(psdPath);
```

Vous avez maintenant à la fois un aperçu PNG et un fichier PSD mis à jour.

## Problèmes courants et solutions
- **Fichier non trouvé :** Vérifiez que `dataDir` se termine par un séparateur de chemin (`/` ou `\`).  
- **OutOfMemoryError sur de gros PSD :** Augmentez la taille du tas JVM (`-Xmx2g`).  
- **Transparence perdue :** Assurez‑vous que `PngColorType.TruecolorWithAlpha` est défini ; sinon le PNG sera enregistré sans alpha.  
- **Le retournement de l’image PSD ne se comporte pas comme prévu :** Revérifiez la constante `RotateFlipType` que vous avez sélectionnée ; certaines constantes combinent rotation et retournement en une seule étape.

## Questions fréquemment posées

**Q : Puis‑je faire pivoter un calque spécifique dans un fichier PSD ?**  
R : Oui, vous pouvez appeler `layer.rotateFlip(RotateFlipType.Rotate90FlipNone)` après avoir itéré sur `im.getLayers()`.

**Q : Existe‑t‑il une limitation de performance avec Aspose.PSD pour Java ?**  
R : La bibliothèque gère la plupart des fichiers efficacement, mais les PSD extrêmement volumineux (>500 Mo) peuvent nécessiter de la mémoire supplémentaire ou des options de streaming.

**Q : Aspose.PSD est‑il gratuit à utiliser ?**  
R : Aspose propose un essai gratuit, mais une licence payante est nécessaire pour la production. Voir la [licence temporaire](https://purchase.aspose.com/temporary-license/) pour les tests.

**Q : Où puis‑je trouver une documentation détaillée ?**  
R : Une documentation complète est disponible sur [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).

**Q : Que faire si je rencontre des problèmes en utilisant Aspose.PSD ?**  
R : Obtenez de l’aide via le [Forum de support Aspose](https://forum.aspose.com/c/psd/34).

**Q : La conversion de PSD en PNG préserve‑t‑elle les effets de calque ?**  
R : Oui, lorsque vous enregistrez avec `PngColorType.TruecolorWithAlpha`, la plupart des effets visuels sont rasterisés dans le PNG.

**Q : Puis‑je traiter par lots plusieurs fichiers PSD ?**  
R : Absolument. Enveloppez le code dans une boucle qui itère sur un répertoire de fichiers PSD.

**Q : Est‑il possible de définir le niveau de compression PNG ?**  
R : `PngOptions` fournit une méthode `setCompressionLevel(int)` pour affiner la taille de sortie.

**Q : Dois‑je fermer l’objet image ?**  
R : `PsdImage` implémente `Closeable` ; utilisez try‑with‑resources ou appelez `im.close()` dans un bloc `finally`.

**Q : Le PNG pivoté aura‑t‑il les mêmes dimensions que l’original ?**  
R : Une rotation de 90° ou 270° échange la largeur et la hauteur, ainsi le PNG reflète automatiquement la nouvelle orientation.

## Conclusion
En exploitant Aspose.PSD pour Java, vous pouvez **enregistrer le PSD en PNG**, **préserver la transparence du PNG**, et **faire pivoter les calques PSD** avec seulement quelques lignes de code. Cette approche élimine le besoin de Photoshop, accélère les flux de travail automatisés, et vous donne un contrôle total sur la sortie d’image. Essayez‑le sur vos propres projets et voyez combien de temps vous économisez !

---

**Dernière mise à jour:** 2026-07-22  
**Testé avec:** Aspose.PSD for Java 24.11  
**Auteur:** Aspose  

{{< blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}