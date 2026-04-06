---
date: 2026-01-12
description: Apprenez à convertir des fichiers Illustrator en PNG en Java avec Aspose.PSD.
  Ce guide étape par étape montre comment charger des fichiers AI, définir les options
  PNG et enregistrer l'image au format PNG.
linktitle: Convert AI to PNG in Java
second_title: Aspose.PSD Java API
title: Convertir Illustrator en PNG en Java – Guide Aspose.PSD
url: /fr/java/java-ai-to-image-format-conversion/convert-ai-to-png/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir Illustrator en PNG en Java

## Introduction
Si vous devez **convertir Illustrator en PNG** de façon programmatique, vous êtes au bon endroit. Dans ce tutoriel, nous parcourrons l’ensemble du processus en utilisant la bibliothèque Aspose.PSD for Java. En quelques lignes de code, vous pouvez charger un fichier AI, ajuster les paramètres PNG et enregistrer le résultat sous forme d’image PNG de haute qualité. C’est parti !

## Quick Answers
- **Quelle bibliothèque gère la conversion AI → PNG ?** Aspose.PSD for Java  
- **Combien de lignes de code sont nécessaires ?** Environ 15 lignes (importations + 3 étapes)  
- **Faut‑il une licence pour la production ?** Oui, une licence commerciale est requise (une version d’essai gratuite est disponible)  
- **Versions Java prises en charge ?** JDK 8 et supérieures  
- **Puis‑je traiter par lots plusieurs fichiers AI ?** Absolument – il suffit de boucler sur les étapes présentées ci‑dessous  

## Qu’est‑ce que “convertir illustrator en png” ?
Convertir des fichiers Illustrator (AI) en PNG signifie rendre le dessin vectoriel sous forme d’image raster. PNG conserve la transparence et offre une compression sans perte, ce qui le rend idéal pour les graphiques web, les actifs UI et les miniatures.

## Pourquoi utiliser Aspose.PSD pour cette conversion ?
- **Prise en charge complète des formats** – Gère AI, PSD, PSB et de nombreux autres formats Adobe.  
- **Aucune dépendance externe** – Pure Java, aucune bibliothèque native requise.  
- **Contrôle granulaire** – Vous pouvez spécifier le type de couleur PNG, le niveau de compression, etc.  
- **Scalable** – Fonctionne aussi bien pour des fichiers uniques que pour de gros traitements par lots.

## Prérequis
1. **Java Development Kit (JDK)** – JDK 8 ou version supérieure installé.  
2. **Aspose.PSD for Java** – Téléchargez depuis la [page des releases Aspose](https://releases.aspose.com/psd/java/) ou obtenez un [essai gratuit](https://releases.aspose.com/).  
3. **IDE** – IntelliJ IDEA, Eclipse, NetBeans, ou tout éditeur compatible Java.  
4. **Connaissances de base en Java** – Familiarité avec les classes, les méthodes et les I/O de fichiers.

## Import Packages
Tout d’abord, importez les classes Aspose.PSD dont vous aurez besoin. Cela prépare l’environnement pour les étapes de conversion.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.ai.AiImage;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

## Guide étape par étape

### Étape 1 : Charger le fichier AI
Chargez votre fichier Illustrator dans un objet `AiImage`. Cela prépare les données vectorielles pour le rendu.

```java
String dataDir = "Your Document Directory"; 
String sourceFileName = dataDir + "34992OStroke.ai";       
AiImage image = (AiImage)Image.load(sourceFileName);
```

### Étape 2 : Définir les options PNG
Configurez la façon dont le PNG sera généré. Ici, nous choisissons **Truecolor avec Alpha** pour conserver la transparence.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
```

### Étape 3 : Enregistrer l’image en PNG
Enfin, écrivez l’image rasterisée sur le disque en utilisant les options définies précédemment.

```java
String outFileName = dataDir + "34992OStroke.png";
image.save(outFileName, options);
```

> **Astuce :** Si vous devez convertir de nombreux fichiers AI, placez les trois étapes dans une boucle et modifiez `sourceFileName`/`outFileName` pour chaque itération.

## Problèmes courants et solutions
| Problème | Solution |
|----------|----------|
| **Erreur de mémoire insuffisante sur de gros fichiers AI** | Augmentez la taille du tas JVM (`-Xmx2g`) ou traitez les fichiers un par un. |
| **Le fond transparent apparaît noir** | Assurez‑vous que `PngColorType.TruecolorWithAlpha` est défini ; cela préserve le canal alpha. |
| **Polices manquantes dans le résultat** | Intégrez les polices requises dans le fichier AI avant la conversion, ou utilisez les fonctionnalités de substitution de polices d’`AiImage`. |

## Questions fréquemment posées

### Qu’est‑ce qu’Aspose.PSD ?
Aspose.PSD est une bibliothèque Java qui permet aux développeurs de travailler avec les fichiers PSD (Photoshop) et d’autres formats Adobe. Elle prend en charge diverses opérations telles que l’édition, la conversion et le rendu.

### Puis‑je utiliser Aspose.PSD gratuitement ?
Vous pouvez utiliser Aspose.PSD avec un [essai gratuit](https://releases.aspose.com/), mais pour bénéficier de toutes les fonctionnalités, vous devez acquérir une licence. Vous pouvez également obtenir une [licence temporaire](https://purchase.aspose.com/temporary-license/) à des fins d’évaluation.

### Quels formats de fichiers Aspose.PSD prend‑il en charge ?
Aspose.PSD prend en charge PSD, PSB, AI et d’autres formats Adobe. Il permet la conversion vers divers formats d’image tels que PNG, JPEG, BMP et TIFF.

### Aspose.PSD est‑il compatible avec toutes les versions de Java ?
Aspose.PSD est compatible avec JDK 8 et supérieures. Veillez à disposer de la version appropriée du JDK installée.

### Où puis‑je trouver plus de documentation ?
Vous trouverez une documentation détaillée sur la [page de documentation Aspose.PSD](https://reference.aspose.com/psd/java/).

---

**Dernière mise à jour :** 2026-01-12  
**Testé avec :** Aspose.PSD for Java 24.12  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}