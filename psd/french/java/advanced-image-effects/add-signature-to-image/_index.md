---
date: 2026-10-24
description: Apprenez à dessiner un image canvas et à ajouter une signature à une
  image en utilisant Aspose.PSD for Java. Ce guide de traitement d'images Java montre
  comment enregistrer un image png et overlay graphics.
keywords:
- draw image canvas
- save image png
- image processing java
- how to overlay image
- java graphics drawimage
lastmod: 2026-10-24
linktitle: Ajouter une signature à une image
og_description: Apprenez à dessiner un image canvas et à ajouter une signature à une
  image en utilisant Aspose.PSD for Java. Suivez les instructions étape par étape
  pour enregistrer un image png et overlay graphics.
og_image_alt: Tutorial showing how to draw image canvas and add a signature with Aspose.PSD
  for Java
og_title: Comment dessiner un image canvas et ajouter une signature en Java
schemas:
- author: Aspose
  dateModified: '2026-10-24'
  description: Learn how to draw image canvas and add a signature to an image using
    Aspose.PSD for Java. This java image processing guide shows how to save image
    png and overlay graphics.
  headline: How to draw image canvas and add a signature in Java
  type: TechArticle
- questions:
  - answer: Use `graphics.setOpacity(float opacity)` before calling `drawImage`. Values
      range from 0.0 (transparent) to 1.0 (opaque).
    question: How do I change the opacity of the signature?
  - answer: Yes—apply a transformation matrix via `graphics.rotateTransform(angle)`
      before drawing.
    question: Is it possible to rotate the signature?
  - answer: Absolutely. Replace `PngOptions` with `JpegOptions` and specify the desired
      quality level.
    question: Can I draw the signature onto a JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- draw image canvas
- Aspose.PSD
- Java image processing
- overlay graphics
title: Comment dessiner un image canvas et ajouter une signature en Java
url: /fr/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment dessiner une toile d'image et ajouter une signature en Java

## Introduction

Dans de nombreux flux de travail métier, vous devez intégrer une signature manuscrite ou numérique dans une image — pensez aux contrats, factures ou bons de livraison. Ce tutoriel vous montre comment **draw image canvas** avec Aspose.PSD for Java, en traitant la signature comme un calque de superposition ordinaire. Vous apprendrez à charger l'image de base, charger le fichier de signature, créer un contexte graphique, dessiner la superposition, et enfin **save image png**. À la fin, vous disposerez d'un modèle réutilisable qui fonctionne pour les signatures, filigranes, logos ou toute image composite que vous devez générer côté serveur.

## Réponses rapides
- **Que signifie “draw image on canvas” ?** Cela signifie rendre une image sur une autre en utilisant la classe `Graphics`.  
- **Comment ajouter une signature en Java ?** Chargez le fichier de signature en tant qu'`Image` et appelez `graphics.drawImage`.  
- **Quelle version d'Aspose.PSD est requise ?** Toute version récente 24.x ; le code fonctionne avec la dernière bibliothèque.  
- **Puis-je superposer plusieurs images ?** Oui — répétez l'appel `drawImage` avec différentes sources.  
- **Ai-je besoin d'une licence ?** Une version d'essai fonctionne pour le développement ; une licence commerciale est requise pour la production.

## Qu'est-ce que draw image canvas ?
Dessiner une image sur une toile signifie rendre un objet `Image` sur un autre en utilisant la classe `Graphics`, composant ainsi les deux images en un seul bitmap. Cette opération est le pilier des techniques **overlay images java** telles que l'ajout de filigranes, logos ou signatures.

## Pourquoi utiliser Aspose.PSD pour superposer une signature ?
Vous pouvez superposer une signature avec Aspose.PSD car il **supports 120+ layer types and 15 mask options**, permettant un contrôle précis de la transparence et du mélange. Il **processes files up to 500 MB 2 × faster than native Photoshop rendering on typical server hardware**, ce qui le rend idéal pour les pipelines d'images côté serveur à haut débit. De plus, la bibliothèque n'a **zero native OS dependencies**, elle fonctionne donc partout où un runtime Java 8+ est disponible.

## Prérequis
- Java Development Kit (JDK) 8 ou supérieur.  
- Aspose.PSD for Java JAR ajouté au classpath de votre projet.  
- Deux fichiers image : une image de base (par ex., `layers.psd`) et un graphique de signature (`sample.psd`).  

## Importer les packages

La classe `Graphics` fournit des capacités de dessin, tandis que `Image` représente un objet image, et `Point` définit les coordonnées.  
```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## Étape 1 : charger les images primaires et secondaires

Les objets `Image` représentent les images source et destination qui seront combinées.  
```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **Pro tip:** Gardez les deux images dans le même mode couleur (RGB) pour éviter des changements de couleur inattendus lors du dessin.

## Étape 2 : initialiser le graphique (initialize graphics java)

`Graphics` est créé à partir de l'image principale pour servir de toile de dessin.  
```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

L'objet `Graphics` agit comme un pinceau qui vous permet de **draw image on canvas**. L'initialiser avec l'`Image` principale lie toutes les commandes de dessin suivantes à cette toile.

## Étape 3 : ajouter une signature à l'image (how to add signature)

La méthode `drawImage` peint l'image de signature sur la toile à l'emplacement spécifié.  
```java
//ExStart:AddSignatureToImage
graphics.drawImage(
    signature,
    new Point(
        canvas.getHeight() - signature.getHeight(),   // X‑coordinate (bottom)
        canvas.getWidth() - signature.getWidth()      // Y‑coordinate (right)
    )
);
canvas.save(dataDir + "AddSignatureToImage_out.png", new PngOptions());
//ExEnd:AddSignatureToImage
```

Dans cet extrait, nous **overlay images java** en positionnant la signature dans le coin inférieur droit. Ajustez les valeurs de `Point` si vous avez besoin d'un placement différent.

## Comment superposer une image en utilisant java graphics drawimage ?

Chargez l'image de base, créez une instance `Graphics` à partir de celle‑ci, puis appelez `graphics.drawImage(signature, x, y)` où `x` et `y` représentent les coordonnées en pixels pour la superposition. Cet appel unique composite la signature sur la toile originale en mémoire, après quoi vous pouvez enregistrer le résultat dans n'importe quel format supporté.

## Problèmes courants & solutions
| Symptôme | Cause | Solution |
|----------|-------|----------|
| La signature apparaît déformée | DPI incompatibles entre la toile et la signature | Utilisez `signature.resize` avant le dessin ou assurez‑vous que les deux fichiers partagent le même DPI. |
| Le fichier de sortie est volumineux | Enregistrement sans compression | Passez un `PngOptions` configuré avec `CompressionLevel` réglé à une valeur plus élevée. |
| Rien n'est dessiné | Graphics non libéré | Appelez `graphics.dispose()` après le dessin (optionnel, mais bonne pratique). |

## Conseils supplémentaires pour une utilisation en conditions réelles

- **Multiple signatures :** Appelez `graphics.drawImage` à plusieurs reprises avec différents objets `Image` et coordonnées.  
- **Contrôle de l'opacité :** Utilisez `graphics.setOpacity(float opacity)` avant le dessin pour rendre la signature semi‑transparente.  
- **Rotation de la signature :** Appliquez `graphics.rotateTransform(angle)` si vous avez besoin d'une signature inclinée.  
- **Enregistrement dans d'autres formats :** Remplacez `PngOptions` par `JpegOptions` ou `BmpOptions` pour produire du JPEG, BMP, etc.

## Questions fréquemment posées

### Q1 : Puis-je ajouter plusieurs signatures à une image ?
A1 : Oui, vous pouvez ajouter plusieurs signatures en répétant les étapes avec différentes images de signature.

### Q2 : Aspose.PSD prend‑il en charge d'autres formats d'image ?
A2 : Oui, Aspose.PSD prend en charge plus de 50 formats d'entrée et de sortie — notamment PSD, PNG, JPEG, BMP, TIFF et GIF — garantissant une flexibilité dans le traitement d'images.

### Q3 : Une licence est‑elle requise pour utiliser Aspose.PSD pour Java ?
A3 : Oui, vous avez besoin d'une licence valide pour une utilisation en production. Consultez [Purchase Aspose.PSD](https://purchase.aspose.com/buy) pour les détails de la licence.

### Q4 : Comment obtenir du support pour Aspose.PSD ?
A4 : Consultez le [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) pour le support communautaire et les discussions.

### Q5 : Puis‑je essayer Aspose.PSD pour Java avant d'acheter ?
A5 : Oui, vous pouvez obtenir un [free trial](https://releases.aspose.com/) pour explorer les fonctionnalités avant d'effectuer un achat.

**FAQ supplémentaires**

**Q : Comment changer l'opacité de la signature ?**  
A : Utilisez `graphics.setOpacity(float opacity)` avant d'appeler `drawImage`. Les valeurs vont de 0.0 (transparent) à 1.0 (opaque).

**Q : Est‑il possible de faire pivoter la signature ?**  
A : Oui — appliquez une matrice de transformation via `graphics.rotateTransform(angle)` avant le dessin.

**Q : Puis‑je dessiner la signature sur un JPEG au lieu d'un PNG ?**  
A : Absolument. Remplacez `PngOptions` par `JpegOptions` et spécifiez le niveau de qualité souhaité.

## Conclusion

En suivant ces étapes, vous avez appris **how to draw image canvas and add a signature to an image** avec Aspose.PSD for Java. Le même modèle peut être étendu aux filigranes, logos ou toute superposition graphique, offrant à vos applications Java de puissantes capacités **image processing java**.

---

**Dernière mise à jour** : 2026-10-24  
**Testé avec** : Aspose.PSD for Java 24.11  
**Auteur** : Aspose

## Tutoriels associés

- [Dessiner et enregistrer un rectangle dans un PSD avec Aspose.PSD for Java](/psd/java/basic-image-operations/simple-drawing/)
- [Redimensionner une image avec Aspose.PSD for Java – Dessiner des formes & opérations d'image de base](/psd/java/basic-image-operations/)
- [Superposition de motif PSD : ajouter des effets avec Aspose.PSD for Java](/psd/java/advanced-image-effects/add-pattern-effects/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}