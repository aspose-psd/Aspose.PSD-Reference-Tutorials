---
date: 2025-12-02
description: Apprenez à dessiner une image sur un canvas et à superposer une signature
  en Java avec Aspose.PSD. Suivez ce tutoriel pas à pas de traitement d'images en
  Java et enregistrez le résultat au format PNG.
language: fr
linktitle: Add a Signature to an Image
second_title: Aspose.PSD Java API
title: Dessiner une image sur le canvas – Ajouter une signature avec Aspose.PSD pour
  Java
url: /java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dessiner une image sur le canvas – Ajouter une signature avec Aspose.PSD pour Java

## Introduction

Ajouter une signature manuscrite ou numérique à une image est une exigence fréquente pour les contrats, factures ou tout document nécessitant une preuve d'authenticité. Avec **Aspose.PSD for Java** vous pouvez **draw image on canvas** et traiter la signature comme une autre couche de superposition. Dans ce **java image processing tutorial**, nous parcourrons l’ensemble du flux de travail — du chargement de l’image de base et du fichier de signature, à l’initialisation du graphique, le dessin de la superposition, et enfin le **save image png java**‑style.

## Réponses rapides
- **Que signifie “draw image on canvas” ?** Cela fait référence au rendu d’une image sur une autre en utilisant la classe `Graphics`.  
- **Comment ajouter une signature en Java ?** Chargez le fichier de signature en tant qu’`Image` et utilisez `Graphics.drawImage`.  
- **Quelle version d’Aspose.PSD est requise ?** Toute version récente 24.x ; le code fonctionne avec la dernière bibliothèque.  
- **Puis-je superposer plusieurs images ?** Oui — répétez l’appel `drawImage` avec différentes sources.  
- **Ai-je besoin d’une licence ?** Une version d’essai fonctionne pour le développement ; une licence commerciale est requise pour la production.

## Qu’est‑ce que “Draw Image on Canvas” ?

Dans la terminologie d’Aspose.PSD, dessiner une image sur un canvas signifie peindre un objet `Image` sur un autre en utilisant un contexte `Graphics`. Cette opération est la base des techniques **overlay images java** telles que l’ajout de filigranes, logos ou signatures.

## Pourquoi utiliser Aspose.PSD pour superposer une signature ?

- **Full PSD support** – fonctionne avec les calques, masques et transparence.  
- **No native OS dependencies** – Java pur, parfait pour le traitement côté serveur.  
- **High‑performance rendering** – optimisé pour les gros fichiers et les compositions complexes.  

## Prérequis
- Java Development Kit (JDK) 8 ou supérieur.  
- JAR Aspose.PSD for Java ajouté au classpath de votre projet.  
- Deux fichiers image : une image de base (par ex., `layers.psd`) et un graphique de signature (`sample.psd`).  

## Import Packages

```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## Étape 1 : Charger les images primaires et secondaires

```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **Conseil :** Conservez les deux images dans le même mode couleur (RGB) pour éviter des changements de couleur inattendus lors du dessin.

## Étape 2 : Initialiser le graphique (initialize graphics java)

```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

L’objet `Graphics` agit comme un pinceau qui vous permet de **draw image on canvas**. L’initialiser avec l’`Image` principale lie toutes les commandes de dessin suivantes à ce canvas.

## Étape 3 : Ajouter la signature à l’image (how to add signature)

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

Dans cet extrait, nous **overlay images java** en positionnant la signature dans le coin inférieur droit. Ajustez les valeurs du `Point` si vous avez besoin d’un placement différent.

## Problèmes courants et solutions

| Symptôme | Cause | Solution |
|----------|-------|----------|
| La signature apparaît déformée | DPI incompatibles entre le canvas et la signature | Utilisez `signature.resize` avant le dessin ou assurez‑vous que les deux fichiers partagent le même DPI. |
| Le fichier de sortie est volumineux | Enregistrement sans compression | Passez un `PngOptions` configuré avec `CompressionLevel` réglé à une valeur plus élevée. |
| Rien n’est dessiné | Graphics non libéré | Appelez `graphics.dispose()` après le dessin (optionnel, mais bonne pratique). |

## Conclusion

En suivant ces étapes, vous avez appris **how to draw image on canvas** et à ajouter de façon transparente une **signature** en utilisant Aspose.PSD pour Java. Cette technique peut être étendue aux filigranes, logos ou tout graphique de superposition, offrant à vos applications Java de puissantes capacités de **java image processing**.

## FAQ

### Q1 : Puis-je ajouter plusieurs signatures à une image ?

A1 : Oui, vous pouvez ajouter plusieurs signatures en répétant les étapes avec différentes images de signature.

### Q2 : Aspose.PSD prend‑il en charge d’autres formats d’image ?

A2 : Oui, Aspose.PSD prend en charge un large éventail de formats d’image, garantissant une flexibilité dans le traitement d’image.

### Q3 : Une licence est‑elle requise pour utiliser Aspose.PSD pour Java ?

A3 : Oui, vous avez besoin d’une licence valide pour utiliser Aspose.PSD. Consultez [Purchase Aspose.PSD](https://purchase.aspose.com/buy) pour les détails de la licence.

### Q4 : Comment obtenir du support pour Aspose.PSD ?

A4 : Visitez le [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) pour le support communautaire et les discussions.

### Q5 : Puis‑je essayer Aspose.PSD pour Java avant d’acheter ?

A5 : Oui, vous pouvez obtenir un [free trial](https://releases.aspose.com/) pour explorer les fonctionnalités avant d’effectuer un achat.

## Questions fréquemment posées supplémentaires

**Q : Comment modifier l’opacité de la signature ?**  
A : Utilisez `graphics.setOpacity(float opacity)` avant d’appeler `drawImage`. Les valeurs vont de 0,0 (transparent) à 1,0 (opaque).

**Q : Est‑il possible de faire pivoter la signature ?**  
A : Oui—appliquez une matrice de transformation via `graphics.rotateTransform(angle)` avant le dessin.

**Q : Puis‑je dessiner la signature sur un JPEG au lieu d’un PNG ?**  
A : Absolument. Remplacez `PngOptions` par `JpegOptions` et spécifiez le niveau de qualité souhaité.

---

**Last Updated:** 2025-12-02  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}