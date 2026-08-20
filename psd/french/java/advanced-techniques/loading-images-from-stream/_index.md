---
date: 2026-05-29
description: Apprenez à convertir PSD en PNG en chargeant des images depuis un flux
  avec Aspose.PSD for Java. Ce tutoriel pas à pas de traitement d'images Java vous
  montre comment lire, convertir et enregistrer les fichiers PSD efficacement.
keywords:
- convert psd to png
- how to load psd
- read image from memory
- save image to stream
- java image processing tutorial
linktitle: Chargement d'images depuis un flux
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn to convert PSD to PNG by loading images from a stream with Aspose.PSD
    for Java. This step‑by‑step Java image processing tutorial shows you how to read,
    convert, and save PSD files efficiently.
  headline: Convert PSD to PNG – Load Images from Stream (Java)
  type: TechArticle
- questions:
  - answer: Absolutely. The library’s streaming architecture lets you loop through
      thousands of PSD files, convert each to PNG, and write directly to output streams
      without excessive memory consumption.
    question: Is Aspose.PSD for Java suitable for batch image processing?
  - answer: Yes, you can explore a free trial version [here](https://releases.aspose.com/).
    question: Can I try Aspose.PSD for Java before purchasing?
  - answer: Join the community at the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34)
      for assistance and discussions.
    question: Where can I find support for Aspose.PSD for Java?
  - answer: Obtain a temporary license [here](https://purchase.aspose.com/temporary-license/)
      for testing Aspose.PSD for Java.
    question: Do I need a temporary license for testing purposes?
  - answer: Visit the [purchase page](https://purchase.aspose.com/buy) to acquire
      Aspose.PSD for Java.
    question: Where can I purchase Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Convertir PSD en PNG – Charger des images depuis un flux (Java)
url: /fr/java/advanced-techniques/loading-images-from-stream/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir PSD en PNG – Charger les images depuis un flux (Java)

## Introduction

Dans ce tutoriel, vous découvrirez comment **convertir PSD en PNG** en chargeant une image PSD directement depuis un `InputStream` Java. Aspose.PSD pour Java simplifie la lecture d'un fichier PSD depuis la mémoire, sa transformation, et l'écriture du résultat dans un flux sous forme d'image PNG. Nous parcourrons chaque étape, expliquerons pourquoi chaque appel d'API est important, et vous donnerons des conseils pour éviter les pièges courants.

## Réponses rapides
- **Quelle est la façon la plus simple de convertir un PSD en PNG en Java ?** Chargez le PSD avec `Image.load(stream)`, cast à `PsdImage`, puis appelez `save(outputStream, new PngOptions())`.  
- **Ai-je besoin d'une licence pour exécuter le code ?** Une licence temporaire fonctionne pour les tests ; une licence complète est requise pour la production.  
- **Puis-je traiter de gros fichiers PSD sans une forte utilisation de mémoire ?** Oui – Aspose.PSD traite les fichiers en mode flux, gérant des fichiers jusqu'à 2 Go sans charger le document complet en mémoire.  
- **Quelles versions de Java sont prises en charge ?** Java 8 à Java 21 sont entièrement prises en charge.  
- **Où puis‑je trouver plus d'exemples ?** La [documentation](https://reference.aspose.com/psd/java/) officielle contient des dizaines d'extraits de code.

## Qu'est-ce que la conversion PSD en PNG ?
**Convertir PSD en PNG** est le processus de lecture d'un fichier Photoshop (.psd) et d'exportation de ses données d'image raster au format Portable Network Graphics (PNG). Avec Aspose.PSD, cette conversion se fait en mémoire, vous permettant de lire ou d'écrire depuis/vers des flux sans toucher au système de fichiers.

## Pourquoi utiliser Aspose.PSD pour Java ?
Aspose.PSD prend en charge **plus de 30 formats d'entrée et de sortie** et peut gérer des **fichiers PSD de plusieurs centaines de pages jusqu'à 2 Go** tout en maintenant l'utilisation de la mémoire en dessous de 200 Mo. La bibliothèque fournit une API pure Java, ce qui signifie qu'aucune bibliothèque native ni installation de Photoshop n'est requise, ce qui est idéal pour les pipelines de traitement d'images côté serveur.

## Prérequis

Avant de commencer, assurez‑vous d'avoir :

- Une expérience de base en développement Java.  
- La bibliothèque Aspose.PSD pour Java installée – téléchargez‑la depuis le site [Aspose](https://releases.aspose.com/psd/java/).  
- Un IDE Java ou un outil de construction (Maven/Gradle) prêt à ajouter le JAR Aspose.PSD à votre projet.

## Importer les packages

La classe `Image` est la classe de base d'Aspose.PSD représentant toute image raster. `PsdImage` fournit des fonctionnalités spécifiques à Photoshop telles que les calques et les canaux. `PngOptions` vous permet de configurer les paramètres spécifiques au PNG. `FileInputStream` et `FileOutputStream` sont des classes d'E/S Java standard pour lire et écrire des fichiers.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.system.io.FileMode;
import com.aspose.psd.system.io.FileStream;
import com.aspose.psd.system.io.MemoryStream;
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
```

## Étape 1 : Configurer votre répertoire de documents

Assurez‑vous d'avoir un répertoire désigné pour vos fichiers source PSD et vos images de sortie. Remplacez `"Your Document Directory"` dans le code par le chemin absolu réel sur votre machine.

```java
String dataDir = "Your Document Directory";
```

## Étape 2 : Définir les chemins source et destination

Spécifiez le chemin du fichier PSD comme source et le chemin de sortie souhaité pour l'image PNG résultante. Cette séparation claire aide lorsque vous passez plus tard à la lecture depuis une base de données ou une requête HTTP.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "result.png";
```

## Étape 3 : Créer le flux d'entrée et charger l'image

`FileInputStream` lit les octets bruts d'un fichier sur le disque. La méthode statique `Image.load(InputStream)` charge une image depuis le flux fourni et renvoie une instance `Image`.

```java
FileInputStream inputStream = new FileInputStream(sourceFile);
Image image = Image.load(inputStream);
```

## Étape 4 : Convertir l'image en PsdImage

`PsdImage` représente un document Photoshop, exposant les calques, les canaux et d'autres données spécifiques au PSD. Cast l'`Image` générique en `PsdImage` pour travailler avec ces fonctionnalités.

```java
PsdImage psdImage = (PsdImage)image;
```

## Étape 5 : Enregistrer l'image dans un flux avec les options PNG

`FileOutputStream` écrit les octets bruts dans un fichier. `PngOptions` configure le niveau de compression, le type de couleur et l'entrelacement pour la sortie PNG.

```java
FileOutputStream outputStream = new FileOutputStream(destName);
psdImage.save(outputStream, new PngOptions());
```

Félicitations ! Vous avez réussi à **convertir PSD en PNG** en chargeant l'image depuis un flux à l'aide d'Aspose.PSD pour Java.

## Problèmes courants et solutions

- **OutOfMemoryError sur des fichiers PSD très volumineux** – Assurez‑vous d'utiliser l'API de streaming (`Image.load(InputStream)`) et évitez d'appeler `save` avec des objets `PsdImage` qui ont été entièrement rasterisés en mémoire.  
- **Calques manquants après la conversion** – Vérifiez que vous travaillez avec une instance `PsdImage` ; les objets `Image` génériques perdent les informations de calque.  
- **Couleurs ou transparence incorrectes** – Définissez `pngOptions.setColorType(PngColorType.TruecolorWithAlpha)` pour préserver les canaux alpha.

## Questions fréquemment posées

**Q : Aspose.PSD pour Java est‑il adapté au traitement d'images par lots ?**  
R : Absolument. L'architecture de streaming de la bibliothèque vous permet de parcourir des milliers de fichiers PSD, de convertir chacun en PNG et d'écrire directement dans des flux de sortie sans consommation excessive de mémoire.

**Q : Puis‑je essayer Aspose.PSD pour Java avant d'acheter ?**  
R : Oui, vous pouvez explorer une version d'essai gratuite [ici](https://releases.aspose.com/).

**Q : Où puis‑je trouver du support pour Aspose.PSD pour Java ?**  
R : Rejoignez la communauté sur le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour obtenir de l'aide et des discussions.

**Q : Ai‑je besoin d'une licence temporaire à des fins de test ?**  
R : Obtenez une licence temporaire [ici](https://purchase.aspose.com/temporary-license/) pour tester Aspose.PSD pour Java.

**Q : Où puis‑je acheter Aspose.PSD pour Java ?**  
R : Visitez la [page d'achat](https://purchase.aspose.com/buy) pour acquérir Aspose.PSD pour Java.

---

**Dernière mise à jour :** 2026-05-29  
**Testé avec :** Aspose.PSD pour Java 24.12  
**Auteur :** Aspose

## Tutoriels associés

- [Enregistrer les images dans un flux avec Aspose.PSD pour Java](/psd/java/advanced-techniques/save-images-to-stream/)
- [Enregistrer les images sur le disque avec Aspose.PSD pour Java](/psd/java/advanced-techniques/save-images-to-disk/)
- [Convertir PSD en formats d'images raster avec Aspose.PSD pour Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}