---
date: 2025-12-08
description: Apprenez à faire pivoter une image à un angle spécifique en Java avec
  Aspose.PSD. Le guide couvre la rotation d’image en Java, la rotation d’image à un
  angle précis, la gestion de l’arrière‑plan et bien plus encore.
linktitle: How to Rotate Image on a Specific Angle
second_title: Aspose.PSD Java API
title: Comment faire pivoter une image à un angle spécifique avec Aspose.PSD pour
  Java
url: /fr/java/advanced-image-manipulation/rotate-image-specific-angle/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment faire pivoter une image à un angle spécifique avec Aspose.PSD pour Java

## Introduction

Si vous devez **how to rotate image** de façon programmatique dans une application Java, Aspose.PSD for Java propose une API propre et haute performance qui se charge du travail lourd. Que vous construisiez un éditeur de photos, génériez des miniatures ou prépariez des ressources pour un service web, faire pivoter une image d’un degré précis est une exigence courante. Dans ce tutoriel, nous parcourrons le processus complet — du chargement d’un fichier PSD à l’enregistrement du résultat pivoté — tout en soulignant les meilleures pratiques telles que la mise en cache et la gestion du fond.

> **Réponses rapides**  
> - **Quelle bibliothèque est la meilleure pour faire pivoter des images en Java ?** Aspose.PSD for Java.  
> - **Puis-je pivoter de n’importe quel degré ?** Oui, la méthode `rotate` accepte un angle de type `float` (positif ou négatif).  
> - **Ai‑je besoin d’une licence pour le développement ?** Un essai gratuit suffit pour les tests ; une licence est requise pour la production.  
> - **Quels formats d’image sont pris en charge ?** PSD, JPEG, PNG, TIFF, GIF, BMP, et bien d’autres.  
> - **Comment définir une couleur de fond pour les espaces vides ?** Passez une instance `Color` à la méthode `rotate`.

## Qu’est‑ce que la rotation d’image en Java ?

La rotation d’image consiste à tourner la matrice de pixels autour d’un point pivot (généralement le centre) d’un angle donné. En Java, vous pouvez le faire manuellement avec `Graphics2D`, mais Aspose.PSD abstrait les calculs, gère les différentes profondeurs de couleur et préserve les informations de calque lors du travail avec des fichiers PSD.

## Pourquoi utiliser Aspose.PSD pour faire pivoter des images ?

- **Précision :** Faire pivoter de n’importe quel degré fractionnaire sans perte de qualité.  
- **Performance :** La mise en cache intégrée (`image.cacheData()`) accélère les gros fichiers.  
- **Contrôle du fond :** Spécifier une couleur de fond pour combler les espaces créés par la rotation.  
- **Flexibilité des formats :** Charger un PSD, exporter en JPEG, PNG ou tout format pris en charge.

## Prérequis

Avant de commencer, assurez‑vous d’avoir les éléments suivants :

1. **Java Development Kit (JDK 8 ou ultérieur)** – un IDE Java fonctionnel ou une configuration en ligne de commande.  
2. **Aspose.PSD for Java** – téléchargez le dernier JAR depuis la [page Aspose.PSD Java](https://reference.aspose.com/psd/java/).  
3. **Fichier PSD d’exemple** – par ex., `sample.psd` placé dans un dossier que vous pouvez référencer depuis votre code.

## Importer les packages

Tout d’abord, importez les classes dont nous aurons besoin. Ces importations restent identiques quel que soit l’angle de rotation choisi.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Guide étape par étape

### Étape 1 : Définir le répertoire de vos documents

Définissez le dossier qui contient le PSD source et où la sortie sera écrite.

```java
String dataDir = "Your Document Directory";
```

> **Astuce :** Utilisez un chemin absolu ou `System.getProperty("user.dir")` pour éviter les surprises liées aux chemins relatifs.

### Étape 2 : Spécifier les chemins des fichiers source et destination

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

Vous pouvez modifier `destName` avec n’importe quelle extension prise en charge (`.png`, `.tiff`, etc.) selon vos besoins de sortie.

### Étape 3 : Charger l’image

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

`Image.load` détecte automatiquement le format du fichier et renvoie un `RasterImage` concret pour les opérations raster.

### Étape 4 : Mettre en cache les données de l’image (Optionnel mais recommandé)

```java
if (!image.isCached())
{
    image.cacheData();
}
```

La mise en cache stocke les pixels de l’image en mémoire, ce qui accélère les transformations ultérieures — particulièrement utile pour les gros fichiers PSD.

### Étape 5 : Faire pivoter l’image

```java
image.rotate(20f, true, Color.getRed());
```

- **20f** – l’angle de rotation en degrés (float). Modifiez cette valeur pour pivoter de n’importe quel angle, par ex., `-45f` pour une rotation dans le sens antihoraire.  
- **true** – conserve le rapport d’aspect original tout en agrandissant le canevas pour contenir l’image pivotée.  
- **Color.getRed()** – couleur de fond qui remplit les coins vides créés par la rotation. Remplacez‑la par `Color.getWhite()` ou toute couleur personnalisée selon vos besoins.

### Étape 6 : Enregistrer le résultat

```java
image.save(destName, new JpegOptions());
```

`JpegOptions` vous permet de contrôler la qualité, la compression et d’autres paramètres spécifiques au JPEG. Pour une sortie sans perte, remplacez‑le par `PngOptions`.

## Problèmes courants et solutions

| Problème | Cause | Solution |
|----------|-------|----------|
| **Coins vides après rotation** | Aucun couleur de fond fournie | Passer une `Color` (par ex., `Color.getWhite()`) à `rotate`. |
| **Erreur de mémoire insuffisante sur de gros PSD** | Image non mis en cache | Appeler `image.cacheData()` avant le traitement. |
| **Direction d’angle incorrecte** | Confusion entre angle négatif et positif | Utiliser des valeurs négatives pour une rotation horaire (ou l’inverse selon votre système de coordonnées). |
| **Modifications non enregistrées** | Oubli d’appeler `save` | S’assurer que `image.save(...)` est exécuté après la rotation. |

## Questions fréquentes

**Q : Puis‑je faire pivoter des images avec transparence en utilisant Aspose.PSD pour Java ?**  
R : Oui. La bibliothèque préserve les canaux alpha ; évitez simplement de spécifier une couleur de fond opaque si vous souhaitez des coins transparents.

**Q : Existe‑t‑il des limitations concernant les formats de fichiers image pris en charge pour la rotation ?**  
R : Non. Aspose.PSD prend en charge PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF, et bien d’autres.

**Q : Puis‑je faire pivoter des images d’un angle négatif ?**  
R : Absolument. Passez un float négatif à `rotate` (par ex., `-30f`) pour une rotation horaire.

**Q : Aspose.PSD fournit‑il un aperçu d’image en temps réel pendant la rotation ?**  
R : L’API est uniquement côté serveur. Pour des aperçus en direct, intégrez le bitmap pivoté dans un framework UI (Swing, JavaFX) et rafraîchissez la vue.

**Q : Existe‑t‑il un forum communautaire pour Aspose.PSD où je peux obtenir de l’aide ?**  
R : Oui, rendez‑vous sur le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour poser des questions et partager des expériences.

## Conclusion

Vous savez maintenant **how to rotate image** à un angle spécifique en utilisant Aspose.PSD for Java. En tirant parti de la mise en cache, du contrôle de la couleur de fond et des options de sortie flexibles, vous pouvez intégrer une fonctionnalité de rotation précise dans n’importe quel flux de travail d’image basé sur Java.

---

**Dernière mise à jour :** 2025-12-08  
**Testé avec :** Aspose.PSD for Java 24.11 (dernière version au moment de la rédaction)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}