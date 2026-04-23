---
date: 2026-02-17
description: Apprenez à exporter des fichiers PSD en PNG et à gérer les flux d'images
  non compressés avec Aspose.PSD pour Java.
linktitle: Handle Uncompressed Image Stream Object in PSD - Java
second_title: Aspose.PSD Java API
title: Exporter le PSD en PNG – Créer un objet graphique PSD – Flux non compressé
  en Java
url: /fr/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

 no extra explanation.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export PSD en PNG – Créer un objet graphique PSD – Flux non compressé en Java

## Introduction
Bienvenue dans le monde de la manipulation d'images en Java ! Dans ce tutoriel, vous allez **créer un objet graphique PSD**, gérer des objets de flux d'image non compressés, et apprendre comment **exporter PSD en PNG** en utilisant Aspose.PSD pour Java. Que vous soyez un graphiste cherchant à automatiser vos flux de travail ou un développeur logiciel souhaitant intégrer de puissantes capacités de traitement d'images dans vos applications, ce guide est fait pour vous. Nous parcourrons tout, des prérequis à l'exportation finale, en veillant à ce que vous ayez une compréhension solide de l'ensemble du processus.

## Quick Answers
- **Que signifie « créer un objet graphique PSD » ?** Il s'agit d'instancier un contexte graphique pour un fichier PSD afin de pouvoir dessiner ou modifier son contenu.  
- **Quelle bibliothèque gère les flux non compressés ?** Aspose.PSD pour Java fournit une prise en charge complète des données d'image brutes (non compressées).  
- **Puis-je exporter PSD en PNG après modification ?** Oui — une fois que vous avez un objet `Graphics`, vous pouvez rendre le PSD et l'enregistrer au format PNG.  
- **Ai‑je besoin d'une licence pour le développement ?** Une version d'essai gratuite suffit pour les tests ; une licence commerciale est requise pour la production.  
- **L'exportation est‑elle sans perte ?** L'exportation en PNG préserve la qualité de l'image, tandis que la taille du fichier est plus grande que celle d'un JPEG mais plus petite qu'un PSD non compressé.  

## How to export PSD to PNG using Aspose.PSD for Java
Lorsque vous devez **exporter PSD en PNG**, le flux de travail typique est :

1. Charger le fichier PSD (ou en créer un).  
2. Effectuer tout dessin ou manipulation de calque avec un objet `Graphics`.  
3. Enregistrer l'image résultante en utilisant `PngOptions` (la même instance `Graphics` peut être réutilisée).  

Même si ce tutoriel se concentre sur la gestion des flux non compressés, le même objet `Graphics` que vous créez peut être réutilisé pour rendre le PSD dans un fichier PNG plus tard dans votre pipeline.

## Prerequisites
Avant de plonger dans le code, assurons‑nous que vous avez tout ce qu'il faut pour commencer ce voyage. Voici les prérequis :

### Java Development Kit (JDK)
Assurez‑vous d'avoir le JDK installé sur votre machine. Vous pouvez le télécharger depuis le site d'Oracle ou utiliser OpenJDK.

### Aspose.PSD for Java
Vous devez télécharger et installer la bibliothèque Aspose.PSD. Cette puissante bibliothèque vous permet de manipuler facilement les fichiers PSD. Vous pouvez obtenir la dernière version via [ce lien](https://releases.aspose.com/psd/java/).

### Integrated Development Environment (IDE)
Il est recommandé d'utiliser un IDE pour écrire et tester votre code Java. Vous pouvez choisir IntelliJ IDEA, Eclipse ou tout autre IDE qui vous convient.

### Basic Understanding of Java
Une bonne connaissance de la programmation Java facilitera le processus. Assurez‑vous de maîtriser les bases telles que les classes, les méthodes et la gestion des exceptions.

Avec tout en place, retroussons nos manches et passons à la partie passionnante – le codage !

## Import Packages
Pour démarrer, nous devons importer les packages nécessaires pour travailler avec Aspose.PSD. Vous trouverez ci‑dessous les imports généralement requis pour la manipulation de fichiers PSD.

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

Décomposons maintenant le code en étapes digestes afin que vous puissiez suivre facilement. Nous allons configurer, charger un fichier PSD, le manipuler et enregistrer le résultat.

## Step 1: Define Your Document Directory
Avant de coder, définissez l'emplacement de votre fichier PSD. Cela constitue le point de départ de votre projet.

```java
String dataDir = "Your Document Directory";
```

Remplacez `"Your Document Directory"` par le chemin réel où se trouve votre fichier PSD (par ex., `layers.psd`). Cela facilite la localisation de vos fichiers sans tracas.

## Step 2: Create a Byte Array Output Stream
Vous avez besoin d'un endroit pour stocker l'image modifiée avant toute autre opération. Un `ByteArrayOutputStream` vous permettra de capturer facilement les données de l'image.

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

Cette ligne initialise un nouvel objet `ByteArrayOutputStream` nommé `ms`. Vous utiliserez cet objet pour enregistrer votre image non compressée.

## Step 3: Load the PSD File
Il est temps de charger le fichier PSD réel. C’est ici que la magie commence !

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Cette ligne charge votre fichier PSD dans un objet `PsdImage`. Assurez‑vous d'utiliser le bon chemin ; sinon, une erreur apparaîtra comme un quiz surprise non contrôlé.

## Step 4: Set Up the PsdOptions for Saving
Vous devez spécifier comment vous souhaitez enregistrer votre image — non compressée, bien sûr !

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

Ici, vous créez un objet `PsdOptions` et définissez la méthode de compression sur `Raw`. Cette méthode garantit que l'image conserve toute sa qualité et est enregistrée sans aucune compression.

## Step 5: Save the Image to the Output Stream
```java
psdImage.save(ms, saveOptions);
```

Cette ligne enregistre votre image modifiée dans le `ByteArrayOutputStream` créé à l'étape 2, en utilisant les options définies à l'étape 4. La méthode `save` se charge d'encoder correctement l'image selon vos paramètres.

## Step 6: Reset the Output Stream
Après l'enregistrement, votre flux de sortie se trouve à la fin. Vous devez le réinitialiser pour pouvoir lire depuis le début.

```java
ms.reset();
```

Cette méthode `reset` prépare votre `ByteArrayOutputStream` à être lu à nouveau depuis le début. Pensez‑y comme à rembobiner une cassette avant d'écouter votre chanson préférée !

## Step 7: Load the Newly Created Image
```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

Ici, nous chargeons l'image à nouveau depuis le `ByteArrayOutputStream` dans un nouveau objet `PsdImage`. C’est le moment de vérifier le résultat de votre travail précédent.

## Step 8: Create Graphics Object
Pour modifier ou rendre davantage l'image, vous devez créer un objet graphique.

```java
Graphics graphics = new Graphics(psdImage);
```

Cette ligne initialise un objet `Graphics` à partir de votre `psdImage`. Vous pouvez maintenant utiliser cet objet graphique pour dessiner ou manipuler l'image selon vos besoins. C’est comme tenir un pinceau en main !

## Manipulate PSD Layers with Graphics Object
Maintenant que vous disposez d’une instance **Graphics**, vous pouvez **manipuler les calques PSD** — par exemple, dessiner des formes, ajouter du texte ou appliquer des filtres à un calque spécifique. Le contexte graphique agit directement sur les données de pixels sous‑jacentes, vous offrant un contrôle granulaire sur l’apparence de chaque calque.

## Common Issues and Solutions
- **NullPointerException lors du chargement du fichier** – vérifiez à nouveau le chemin `dataDir` et assurez‑vous que le nom du fichier est correct.  
- **Sortie compressée malgré l’utilisation de Raw** – assurez‑vous que `saveOptions.setCompressionMethod(CompressionMethod.Raw);` est appelé avant la méthode `save`.  
- **L’objet Graphics apparaît vide** – assurez‑vous de dessiner sur la bonne instance `PsdImage` (utilisez celle que vous avez chargée, pas celle nouvellement créée, sauf si c’est intentionnel).

## FAQ's
### What is Aspose.PSD?
Aspose.PSD est une bibliothèque .NET qui permet aux développeurs de créer, modifier et manipuler des fichiers Photoshop PSD ainsi que les formats d'image associés de manière programmatique.

### How can I download Aspose.PSD for Java?
Vous pouvez le télécharger depuis la [page de version](https://releases.aspose.com/psd/java/).

### Is there a free trial for Aspose.PSD?
Oui, vous pouvez obtenir une version d'essai gratuite [ici](https://releases.aspose.com/).

### Can I get support for Aspose.PSD?
Absolument ! Vous pouvez demander de l'aide sur le [forum de support Aspose](https://forum.aspose.com/c/psd/34).

### How can I obtain a temporary license for Aspose.PSD?
Rendez‑vous simplement sur la [page de licence temporaire](https://purchase.aspose.com/temporary-license/) pour commencer.

## Frequently Asked Questions

**Q : Puis‑je utiliser l’objet graphics pour éditer uniquement un calque spécifique ?**  
R : Oui. Après avoir chargé le PSD, sélectionnez le calque souhaité via `psdImage.getLayers().get_Item(index)` et transmettez‑le au constructeur `Graphics`.

**Q : La méthode de compression Raw affecte‑t‑elle la taille du fichier ?**  
R : Raw stocke les données de pixels sans compression, donc la taille du fichier sera plus grande que celle des PSD compressés, mais la qualité de l'image reste intacte.

**Q : Est‑il possible d'exporter le PSD modifié vers un autre format (par ex., PNG) ?**  
R : Bien sûr. Utilisez la surcharge appropriée de `Image.save` avec `PngOptions` après l'édition — c’est la méthode standard pour **exporter PSD en PNG**.

**Q : Quelle version de Java est requise ?**  
R : Aspose.PSD pour Java prend en charge JDK 8 et les versions ultérieures.

**Q : Comment libérer les ressources après le traitement ?**  
R : Appelez `psdImage.dispose()` et fermez tous les flux pour libérer les ressources natives.

---

**Last Updated:** 2026-02-17  
**Tested With:** Aspose.PSD for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}