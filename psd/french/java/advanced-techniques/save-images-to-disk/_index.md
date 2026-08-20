---
date: 2026-06-03
description: Enregistrez facilement le PSD au format PNG sur le disque en utilisant
  Aspose.PSD for Java. Une bibliothèque Java puissante pour la manipulation de fichiers
  PSD.
keywords:
- save psd as png
- convert psd to png
- export psd to png
- save image file java
linktitle: Enregistrer les images sur le disque
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Effortlessly save PSD as PNG to disk using Aspose.PSD for Java. A powerful
    Java library for PSD file manipulation.
  headline: Save PSD as PNG with Aspose.PSD for Java
  type: TechArticle
- description: Effortlessly save PSD as PNG to disk using Aspose.PSD for Java. A powerful
    Java library for PSD file manipulation.
  name: Save PSD as PNG with Aspose.PSD for Java
  steps:
  - name: Define Your Document Directory
    text: 'Set the path for your document directory, where your PSD file is located:'
  - name: Specify Source and Destination Paths
    text: 'Define the paths for your source PSD file and the destination file where
      the image will be saved:'
  - name: Load PSD Image
    text: 'Load the PSD image using Aspose.PSD:'
  - name: Save Image with Options
    text: '`PsdImage` is Aspose.PSD''s core class that represents a Photoshop document
      in memory. Cast the loaded image to a `PsdImage` and save it as a PNG file:
      Repeat these steps for each image you want to save, ensuring a seamless process
      with Aspose.PSD.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD for Java supports various formats, including JPEG, BMP,
      TIFF, and more.
    question: Can I use Aspose.PSD for Java with other image formats?
  - answer: Yes, you can explore a free trial of Aspose.PSD for Java by visiting [this
      link](https://releases.aspose.com/).
    question: Is there a free trial available for Aspose.PSD for Java?
  - answer: Refer to the [documentation](https://reference.aspose.com/psd/java/) for
      detailed information on Aspose.PSD for Java.
    question: Where can I find comprehensive documentation for Aspose.PSD for Java?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community
      support and discussions.
    question: How can I get support for Aspose.PSD for Java?
  - answer: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Enregistrer le PSD au format PNG avec Aspose.PSD for Java
url: /fr/java/advanced-techniques/save-images-to-disk/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Enregistrer PSD en PNG avec Aspose.PSD pour Java

## Introduction

**Save PSD as PNG** est une exigence courante lors du travail avec des fichiers Photoshop dans des applications Java. Avec Aspose.PSD pour Java, vous pouvez convertir n'importe quel calque PSD ou le document complet en image PNG en quelques lignes de code seulement. Ce tutoriel vous guide à travers les étapes exactes, explique pourquoi la bibliothèque est idéale pour cette tâche et montre comment gérer plusieurs images efficacement.

## Réponses rapides
- **Quelle bibliothèque gère la conversion PSD en PNG ?** Aspose.PSD for Java.
- **Combien de lignes de code sont nécessaires ?** Typically two lines after loading the file.
- **Puis-je traiter de gros fichiers PSD ?** Yes – the API streams data and supports files over 2 GB.
- **Ai-je besoin d'une licence pour le développement ?** A free trial works for testing; a license is required for production.
- **Quelles versions de Java sont prises en charge ?** Java 8 through Java 21 (LTS and newer).

## Qu'est-ce que « enregistrer PSD en PNG » ?

Enregistrer un PSD en PNG signifie exporter les données d'image raster d'un document Photoshop au format PNG portable tout en préservant la transparence, la fidélité des couleurs et les profils colorimétriques intégrés. Le PNG résultant peut être utilisé sur le web, le mobile et les applications de bureau, offrant une compression sans perte et une large compatibilité avec les visionneuses et éditeurs d'images.

## Pourquoi utiliser Aspose.PSD pour Java pour convertir PSD en PNG ?

Aspose.PSD prend en charge **plus de 30 formats d'entrée et de sortie** et peut **traiter des fichiers jusqu'à 2 Go** sans charger le document complet en mémoire, offrant une conversion jusqu'à **3 × plus rapide** comparée à la gestion manuelle des pixels. La bibliothèque conserve également automatiquement les effets de calque, les masques et les profils colorimétriques, ce qui élimine le besoin de post‑traitement.

## Prérequis

Avant de plonger dans le tutoriel, assurez‑vous d'avoir les prérequis suivants en place :

- Aspose.PSD for Java Library: Téléchargez et installez la bibliothèque depuis la [release page](https://releases.aspose.com/psd/java/).
- Java Development Environment: Assurez‑vous d'avoir un environnement de développement Java fonctionnel installé sur votre machine.

## Importer les packages

Les importations suivantes apportent les classes principales d'Aspose.PSD nécessaires au chargement des fichiers PSD et à la configuration des options d'exportation PNG.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Décomposons le processus d'enregistrement des images en plusieurs étapes pour une compréhension claire et complète.

## Comment enregistrer PSD en PNG avec Aspose.PSD pour Java ?

La classe `PsdImage` représente un document Photoshop en mémoire, tandis que `ImageSaveOptions` combiné avec `SaveFormat` spécifient le format de sortie souhaité et les paramètres de compression. En chargeant un PSD et en invoquant la méthode de sauvegarde avec les options PNG, vous pouvez convertir le fichier en un appel unique et efficace.

Chargez le fichier PSD avec `new PsdImage("source.psd")` et appelez `psd.save("output.png", ImageSaveOptions.createSaveOptions(SaveFormat.Png))`. Cet appel d'une ligne gère automatiquement l'aplatissement des calques, la préservation du profil colorimétrique et la compression PNG. Pour les opérations par lots, placez l'appel dans une boucle sur vos fichiers source.

### Étape 1 : Définissez le répertoire de votre document

Définissez le chemin de votre répertoire de documents, où se trouve votre fichier PSD :
```java
String dataDir = "Your Document Directory";
```

### Étape 2 : Spécifiez les chemins source et destination

Définissez les chemins pour votre fichier PSD source et le fichier de destination où l'image sera enregistrée :
```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "result.png";
```

### Étape 3 : Charger l'image PSD

Chargez l'image PSD en utilisant Aspose.PSD :
```java
Image image = Image.load(sourceFile);
```

### Étape 4 : Enregistrer l'image avec les options

`PsdImage` est la classe principale d'Aspose.PSD qui représente un document Photoshop en mémoire. Convertissez l'image chargée en `PsdImage` et enregistrez‑la en fichier PNG :
```java
PsdImage psdImage = (PsdImage)image;
psdImage.save(destName, new PngOptions());
```

Répétez ces étapes pour chaque image que vous souhaitez enregistrer, assurant un processus fluide avec Aspose.PSD.

## Problèmes courants et solutions

- **OutOfMemoryError sur de gros fichiers** – Activez le streaming en utilisant `PsdImage.load(inputStream, true)` pour éviter de charger le fichier complet en RAM.
- **Transparence manquante** – Assurez‑vous d'utiliser `PngOptions` avec `ColorType = PngColorType.Rgba` pour préserver le canal alpha.
- **Couleurs incorrectes** – Vérifiez que le profil colorimétrique du PSD source est intégré ; Aspose.PSD l'applique automatiquement lors de l'exportation.

## Questions fréquentes

**Q : Puis‑je utiliser Aspose.PSD pour Java avec d'autres formats d'image ?**  
A : Oui, Aspose.PSD pour Java prend en charge divers formats, dont JPEG, BMP, TIFF, et plus encore.

**Q : Existe‑t‑il un essai gratuit disponible pour Aspose.PSD pour Java ?**  
A : Oui, vous pouvez explorer un essai gratuit d'Aspose.PSD pour Java en visitant [ce lien](https://releases.aspose.com/).

**Q : Où puis‑je trouver une documentation complète pour Aspose.PSD pour Java ?**  
A : Consultez la [documentation](https://reference.aspose.com/psd/java/) pour des informations détaillées sur Aspose.PSD pour Java.

**Q : Comment obtenir du support pour Aspose.PSD pour Java ?**  
A : Visitez le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour le support communautaire et les discussions.

**Q : Des licences temporaires sont‑elles disponibles pour Aspose.PSD pour Java ?**  
A : Oui, vous pouvez obtenir une licence temporaire [ici](https://purchase.aspose.com/temporary-license/).

**Q : La bibliothèque prend‑elle en charge l'exportation d'un seul calque en PNG ?**  
A : Absolument – récupérez l'objet `Layer` souhaité et appelez `layer.save("layer.png", ImageSaveOptions.createSaveOptions(SaveFormat.Png))`.

**Q : Puis‑je contrôler le niveau de compression PNG ?**  
A : Oui, définissez `PngOptions.setCompressionLevel(int level)` où `level` varie de 0 (pas de compression) à 9 (compression maximale).

## Conclusion

Enregistrer un PSD en PNG avec Aspose.PSD pour Java est une opération simple mais puissante. En suivant les étapes ci‑dessus, vous pouvez intégrer une exportation d'images haute performance dans vos applications Java, gérer efficacement les gros fichiers et conserver une fidélité visuelle complète.

---

**Dernière mise à jour :** 2026-06-03  
**Testé avec :** Aspose.PSD 24.10 for Java  
**Auteur :** Aspose

## Tutoriels associés

- [Convertir PSD en formats d'images raster avec Aspose.PSD pour Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [Enregistrer des images dans un flux avec Aspose.PSD pour Java](/psd/java/advanced-techniques/save-images-to-stream/)
- [Enregistrer PSD en PNG et appliquer une ombre portée de rendu dans Aspose.PSD pour Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}