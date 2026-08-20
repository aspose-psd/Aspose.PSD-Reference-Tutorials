---
date: 2026-04-28
description: Apprenez comment ajouter une signature à une image en dessinant une image
  sur une toile avec Aspose.PSD pour Java. Ce tutoriel de traitement d'images Java
  montre comment enregistrer l'image au format PNG et superposer des graphiques.
keywords:
- add signature to image
- draw image on canvas
- save image as png
- java image processing
- add watermark java
linktitle: Ajouter une signature à une image
second_title: Aspose.PSD Java API
title: Ajouter une signature à l'image – Dessiner l'image sur le canevas avec Aspose.PSD
  pour Java
url: /fr/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajouter une signature à une image – Dessiner une image sur le canevas avec Aspose.PSD pour Java

## Introduction

Ajouter une signature manuscrite ou numérique **add signature to image** est une exigence courante pour les contrats, les factures ou tout document nécessitant une preuve d'authenticité. Dans ce tutoriel, vous verrez comment Aspose.PSD pour Java vous permet de **draw image on canvas** et de traiter la signature comme une simple couche de superposition. Nous parcourrons le chargement de l'image de base, le chargement du fichier de signature, l'initialisation d'un contexte graphique, le dessin de la superposition, et enfin **save image as PNG**. À la fin, vous disposerez d'un modèle réutilisable pour tout scénario de **java image processing**, qu'il s'agisse d'une signature, d'un filigrane ou d'un logo.

## Réponses rapides
- **Que signifie « draw image on canvas » ?** Cela fait référence au rendu d'une image sur une autre en utilisant la classe `Graphics`.  
- **Comment ajouter une signature en Java ?** Chargez le fichier de signature en tant qu'`Image` et utilisez `Graphics.drawImage`.  
- **Quelle version d'Aspose.PSD est requise ?** Toute version récente 24.x ; le code fonctionne avec la dernière bibliothèque.  
- **Puis-je superposer plusieurs images ?** Oui—répétez l'appel `drawImage` avec différentes sources.  
- **Ai-je besoin d'une licence ?** Une version d'essai fonctionne pour le développement ; une licence commerciale est requise pour la production.

## Qu'est-ce que « draw image on canvas » ?
Dans la terminologie d'Aspose.PSD, dessiner une image sur un canevas signifie peindre un objet `Image` sur un autre à l'aide d'un contexte `Graphics`. Cette opération constitue la base des techniques **overlay images java** telles que l'ajout de filigranes, de logos ou de signatures.

## Pourquoi utiliser Aspose.PSD pour superposer une signature ?
- **Full PSD support** – fonctionne avec les calques, les masques et la transparence.  
- **No native OS dependencies** – Java pur, parfait pour le traitement côté serveur.  
- **High‑performance rendering** – optimisé pour les gros fichiers et les compositions complexes.  

## Prérequis
- Java Development Kit (JDK) 8 ou supérieur.  
- JAR Aspose.PSD pour Java ajouté au classpath de votre projet.  
- Deux fichiers **image** : une image de base (par ex., `layers.psd`) et un graphique de signature (`sample.psd`).  

## Importer les packages

```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## Étape 1 : Charger les images primaires et secondaires

```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **Astuce :** Conservez les deux images dans le même mode couleur (RGB) pour éviter des changements de couleur inattendus lors du dessin.

## Étape 2 : Initialiser Graphics (initialize graphics java)

```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

L'objet `Graphics` agit comme un pinceau qui vous permet de **draw image on canvas**. L'initialiser avec l'`Image` principale lie toutes les commandes de dessin suivantes à ce canevas.

## Étape 3 : Ajouter une signature à l'image (how to add signature)

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

Dans cet extrait, nous **overlay images java** en positionnant la signature dans le coin inférieur droit. Ajustez les valeurs du `Point` si vous avez besoin d'un placement différent.

## Problèmes courants & solutions
| Symptôme | Cause | Solution |
|----------|-------|----------|
| La signature apparaît déformée | DPI incompatibles entre le canevas et la signature | Utilisez `signature.resize` avant le dessin ou assurez-vous que les deux fichiers partagent le même DPI. |
| Le fichier de sortie est volumineux | Enregistrement sans compression | Passez un `PngOptions` configuré avec `CompressionLevel` réglé à une valeur plus élevée. |
| Rien n'est dessiné | Graphics non libéré | Appelez `graphics.dispose()` après le dessin (optionnel, mais bonne pratique). |

## Conseils supplémentaires pour une utilisation réelle

- **Multiple signatures** : Appelez `graphics.drawImage` de façon répétée avec différents objets `Image` et coordonnées.  
- **Contrôle de l'opacité** : Utilisez `graphics.setOpacity(float opacity)` avant le dessin pour rendre la signature semi‑transparente.  
- **Rotation de la signature** : Appliquez `graphics.rotateTransform(angle)` si vous avez besoin d'une signature inclinée.  
- **Enregistrement dans d'autres formats** : Remplacez `PngOptions` par `JpegOptions` ou `BmpOptions` pour produire du JPEG, BMP, etc.

## Questions fréquentes

### Q1 : Puis-je ajouter plusieurs signatures à une image ?
R1 : Oui, vous pouvez ajouter plusieurs signatures en répétant les étapes avec différentes images de signature.

### Q2 : Aspose.PSD prend‑il en charge d'autres formats d'image ?
R2 : Oui, Aspose.PSD prend en charge un large éventail de formats d'image, assurant une flexibilité dans le traitement d'images.

### Q3 : Une licence est‑elle requise pour utiliser Aspose.PSD pour Java ?
R3 : Oui, vous avez besoin d'une licence valide pour utiliser Aspose.PSD. Consultez [Purchase Aspose.PSD](https://purchase.aspose.com/buy) pour les détails de licence.

### Q4 : Comment obtenir du support pour Aspose.PSD ?
R4 : Consultez le [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) pour le support communautaire et les discussions.

### Q5 : Puis-je essayer Aspose.PSD pour Java avant d'acheter ?
R5 : Oui, vous pouvez obtenir un [free trial](https://releases.aspose.com/) pour explorer les fonctionnalités avant d'effectuer un achat.

**FAQ supplémentaires**

**Q : Comment modifier l'opacité de la signature ?**  
R : Utilisez `graphics.setOpacity(float opacity)` avant d'appeler `drawImage`. Les valeurs vont de 0,0 (transparent) à 1,0 (opaque).

**Q : Est‑il possible de faire pivoter la signature ?**  
R : Oui—appliquez une matrice de transformation via `graphics.rotateTransform(angle)` avant le dessin.

**Q : Puis‑je dessiner la signature sur un JPEG au lieu d'un PNG ?**  
R : Absolument. Remplacez `PngOptions` par `JpegOptions` et spécifiez le niveau de qualité souhaité.

## Conclusion

En suivant ces étapes, vous avez appris **how to add signature to image** en **drawing an image on canvas** avec Aspose.PSD pour Java. Le même modèle peut être étendu aux filigranes, logos ou toute autre graphique superposée, offrant à vos applications Java de puissantes capacités de **java image processing**.

---

**Dernière mise à jour :** 2026-04-28  
**Testé avec :** Aspose.PSD for Java 24.11  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}