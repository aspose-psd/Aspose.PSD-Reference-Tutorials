---
date: 2026-02-12
description: Apprenez à redimensionner une image en Java avec Aspose.PSD for Java.
  Guide étape par étape avec l'énumération Resize Type, plus des astuces pour convertir
  un PSD en JPEG.
linktitle: Resizing with Resize Type Enumeration
second_title: Aspose.PSD Java API
title: Redimensionner une image en Java - Utilisation de l'énumération Resize Type
  dans Aspose.PSD pour Java
url: /fr/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
weight: 18
---

 end.

Let's craft final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Redimensionner une image Java : Utilisation de l'énumération Resize Type dans Aspose.PSD pour Java

## Introduction

Redimensionner les images est une exigence courante dans les applications Java, et les opérations **resize image java** deviennent simples avec Aspose.PSD. Dans ce tutoriel, vous apprendrez comment **resize image java** en utilisant la puissante énumération Resize Type, et vous verrez également comment **convert psd to jpeg** après le redimensionnement. Que vous construisiez un outil de bureau ou un service côté serveur, ces étapes vous aideront à gérer les dimensions des images de manière fiable et à obtenir un redimensionnement d’image de haute qualité.

## Réponses rapides
- **Quelle bibliothèque gère le resize image java ?** Aspose.PSD for Java.  
- **Quel type de redimensionnement offre la meilleure qualité ?** `ResizeType.LanczosResample`.  
- **Puis‑je convertir PSD en JPEG après le redimensionnement ?** Oui – il suffit d’enregistrer avec `JpegOptions`.  
- **Ai‑je besoin d’une licence pour la production ?** Une licence Aspose.PSD valide est requise pour une utilisation en production.  
- **Cette approche convient‑elle aux gros lots ?** Absolument ; l’API est optimisée pour les performances.

## Qu’est‑ce que le Resize Image Java ?

Le terme « resize image java » désigne le changement programmatique des dimensions en pixels d’une image à l’aide de code Java. Aspose.PSD fournit une API concise qui abstrait la manipulation bas‑niveau des pixels, vous permettant de vous concentrer sur la logique métier plutôt que sur les détails du traitement d’image.

## Pourquoi utiliser l’énumération Resize Type ?

L’énumération Resize Type vous donne un contrôle fin sur l’algorithme de rééchantillonnage, vous permettant d’équilibrer vitesse et qualité. Pour la plupart des applications, `LanczosResample` offre un excellent compromis, délivrant des résultats nets sans pénalité de performance importante. Choisir le bon type de redimensionnement est essentiel pour obtenir un redimensionnement d’image de haute qualité.

## Prérequis

Avant de commencer ce tutoriel, assurez‑vous d’avoir les prérequis suivants :

1. **Environnement de développement Java** – un JDK 8+ installé et configuré.  
2. **Bibliothèque Aspose.PSD** – téléchargez et installez la bibliothèque Aspose.PSD depuis le [site web](https://releases.aspose.com/psd/java/).  
3. **Fichier PSD d’exemple** – disposez d’un fichier PSD d’exemple prêt pour l’expérimentation. Vous pouvez utiliser le fichier [sample.psd](Your Document Directory/sample.psd) pour ce tutoriel.

## Importer les packages

Pour commencer, importez les packages nécessaires dans votre projet Java :

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Étape 1 : Charger l’image

Commencez par charger une image existante dans une instance de la classe `RasterImage`. Utilisez le fragment de code suivant :

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

## Étape 2 : Redimensionner l’image

Redimensionnez maintenant l’image chargée en utilisant l’énumération Resize Type. Dans cet exemple, nous utilisons la méthode Lanczos Resample, idéale lorsque vous **how to resize image** avec une haute qualité :

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## Étape 3 : Enregistrer l’image redimensionnée

Après le redimensionnement, enregistrez l’image avec les dimensions spécifiées et le type de redimensionnement choisi. Ici, nous montrons également **convert psd to jpeg** en enregistrant le résultat sous forme de fichier JPEG :

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

Vous avez maintenant exécuté un flux complet **resize image java** qui produit un redimensionnement d’image de haute qualité et une sortie JPEG prête à l’emploi.

## Problèmes courants et solutions

- **L’image apparaît floue après le redimensionnement** – Essayez un autre `ResizeType` tel que `Bicubic` ou `NearestNeighbour` pour voir lequel donne le meilleur résultat visuel pour votre image spécifique.  
- **OutOfMemoryError sur de gros fichiers PSD** – Traitez l’image par morceaux plus petits ou augmentez la taille du tas JVM (`-Xmx` flag).  

## FAQ

### Q1 : Aspose.PSD for Java convient‑il aux projets petits et à grande échelle ?

R1 : Absolument ! Aspose.PSD for Java est conçu pour répondre aux projets de toutes tailles, offrant évolutivité et efficacité.

### Q2 : Puis‑je utiliser un type de redimensionnement différent de Lanczos Resample ?

R2 : Oui, Aspose.PSD for Java propose divers types de redimensionnement, tels que Nearest Neighbour, Bicubic, et plus encore. Consultez la documentation pour une liste complète.

### Q3 : Où puis‑je trouver un support supplémentaire pour Aspose.PSD for Java ?

R3 : Pour toute question ou assistance, visitez le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q4 : Existe‑t‑il un essai gratuit d’Aspose.PSD for Java ?

R4 : Oui, vous pouvez accéder à une version d’essai gratuite [ici](https://releases.aspose.com/).

### Q5 : Comment obtenir une licence temporaire pour Aspose.PSD for Java ?

R5 : Pour obtenir une licence temporaire, rendez‑vous sur [ce lien](https://purchase.aspose.com/temporary-license/).

## Questions fréquemment posées

**Q : Comment convertir programmatique un fichier PSD en JPEG sans redimensionner ?**  
R : Chargez le PSD avec `Image.load`, puis appelez `image.save("output.jpg", new JpegOptions());`.

**Q : Est‑il possible de conserver le DPI d’origine lors du redimensionnement ?**  
R : Oui, vous pouvez définir la propriété `Resolution` sur l’objet `Image` avant l’enregistrement.

**Q : Puis‑je chaîner plusieurs opérations de redimensionnement ?**  
R : Bien que vous puissiez appeler `resize` plusieurs fois, il est plus efficace de calculer les dimensions finales et de redimensionner une seule fois.

## FAQ supplémentaires

**Q : L’énumération Resize Type affecte‑t‑elle la vitesse de traitement ?**  
R : Oui, les algorithmes plus simples comme `NearestNeighbour` sont plus rapides mais peuvent produire des résultats de moindre qualité, tandis que `LanczosResample` offre une meilleure qualité avec un coût de performance modéré.

**Q : Puis‑je redimensionner des images dans un environnement multithread ?**  
R : L’API Aspose.PSD est thread‑safe pour les opérations en lecture seule. Pour un redimensionnement concurrent, créez des instances `Image` séparées par thread.

**Q : Comment gérer les images avec canal alpha lors du redimensionnement ?**  
R : La bibliothèque préserve la transparence alpha par défaut. Si vous devez aplatir l’image, définissez la couleur d’arrière‑plan avant l’enregistrement.

---

**Dernière mise à jour :** 2026-02-12  
**Testé avec :** Aspose.PSD for Java 24.12  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}