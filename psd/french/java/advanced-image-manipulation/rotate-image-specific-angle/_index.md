---
date: 2026-02-12
description: Apprenez à faire pivoter une image à un angle précis en Java avec Aspose.PSD.
  Ce guide montre comment faire pivoter une image, la faire pivoter de degrés, et
  gérer les couleurs d'arrière-plan.
linktitle: How to Rotate Image on a Specific Angle
second_title: Aspose.PSD Java API
title: Comment faire pivoter une image à un angle précis avec Aspose.PSD pour Java
url: /fr/java/advanced-image-manipulation/rotate-image-specific-angle/
weight: 20
---

 with Aspose.PSD for Java" etc.

Also note "step‑by‑step" etc.

Also "Pro tip:" etc.

Also "Common Issues and Solutions" table.

Also "Frequently Asked Questions".

Also "Conclusion".

Also "Last Updated", "Tested With", "Author".

Also any other text.

Make sure to keep code block placeholders unchanged.

Also keep the shortcodes exactly.

Let's produce final output.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment faire pivoter une image à un angle précis avec Aspose.PSD pour Java

## Introduction

Si vous devez **faire pivoter une image** de façon programmatique dans une application Java, Aspose.PSD pour Java propose une API propre et haute performance qui se charge du travail lourd. Que vous construisiez un éditeur de photos, génériez des vignettes ou prépariez des ressources pour un service web, faire pivoter une image d’un degré exact est une exigence courante. Dans ce tutoriel, nous parcourrons le processus complet — du chargement d’un fichier PSD à l’enregistrement du résultat pivoté — tout en soulignant les meilleures pratiques telles que la mise en cache et la gestion en arrière‑plan.

## Réponses rapides
- **Quelle bibliothèque est la meilleure pour faire pivoter des images en Java ?** Aspose.PSD pour Java.  
- **Puis‑je pivoter à n’importe quel degré ?** Oui, la méthode `rotate` accepte un angle `float` (positif ou négatif).  
- **Ai‑je besoin d’une licence pour le développement ?** Un essai gratuit suffit pour les tests ; une licence est requise pour la production.  
- **Quels formats d’image sont pris en charge ?** PSD, JPEG, PNG, TIFF, GIF, BMP, et bien d’autres.  
- **Comment définir une couleur d’arrière‑plan pour l’espace vide ?** Passez une instance `Color` à la méthode `rotate`.

## Qu’est‑ce que la rotation d’image en Java ?

La rotation d’image consiste à faire tourner la matrice de pixels autour d’un point pivot (généralement le centre) d’un angle donné. En Java, vous pouvez le faire manuellement avec `Graphics2D`, mais Aspose.PSD abstrait les calculs, gère les différentes profondeurs de couleur et préserve les informations de calque lorsqu’on travaille avec des fichiers PSD.

## Pourquoi utiliser Aspose.PSD pour faire pivoter des images ?

- **Précision :** Pivotez à n’importe quel degré fractionnaire sans perte de qualité.  
- **Performance :** La mise en cache intégrée (`image.cacheData()`) accélère le traitement des gros fichiers.  
- **Contrôle de l’arrière‑plan :** Spécifiez une couleur d’arrière‑plan pour combler les espaces créés par la rotation.  
- **Flexibilité des formats :** Chargez un PSD, exportez en JPEG, PNG ou tout autre format supporté.

## Prérequis

Avant de commencer, assurez‑vous d’avoir les éléments suivants :

1. **Java Development Kit (JDK 8 ou supérieur)** – un IDE Java fonctionnel ou une configuration en ligne de commande.  
2. **Aspose.PSD pour Java** – téléchargez le dernier JAR depuis la [page Aspose.PSD Java](https://reference.aspose.com/psd/java/).  
3. **Fichier PSD d’exemple** – par ex. `sample.psd` placé dans un dossier que vous pouvez référencer depuis votre code.

## Importer les packages

Tout d’abord, importez les classes dont nous aurons besoin. Ces imports restent identiques quel que soit l’angle de rotation choisi.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Guide étape par étape

### Étape 1 : Définir le répertoire de votre document

Définissez le dossier qui contient le PSD source et où le résultat sera écrit.

```java
String dataDir = "Your Document Directory";
```

> **Astuce :** Utilisez un chemin absolu ou `System.getProperty("user.dir")` pour éviter les surprises liées aux chemins relatifs.

### Étape 2 : Spécifier les chemins de fichier source et destination

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

Vous pouvez changer `destName` avec n’importe quelle extension prise en charge (`.png`, `.tiff`, etc.) selon vos besoins de sortie.

### Étape 3 : Charger l’image

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

`Image.load` détecte automatiquement le format du fichier et renvoie un `RasterImage` concret pour les opérations basées sur les pixels.

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

- **20f** – l’angle de rotation en degrés (float). Modifiez cette valeur pour pivoter à n’importe quel angle, par ex. `-45f` pour une rotation dans le sens antihoraire.  
- **true** – conserve le ratio d’aspect original tout en agrandissant le canevas pour accueillir l’image pivotée.  
- **Color.getRed()** – couleur d’arrière‑plan qui remplit les coins vides créés par la rotation. Remplacez‑la par `Color.getWhite()` ou toute couleur personnalisée selon vos besoins.

#### Faire pivoter une image de degrés en Java

La méthode `rotate` accepte n’importe quelle valeur à virgule flottante, vous pouvez donc **faire pivoter une image de degrés** tels que `30f`, `90f` ou `-15f`. Les valeurs positives tournent dans le sens horaire, les valeurs négatives dans le sens antihoraire.

#### Faire pivoter une image à un angle spécifique avec Aspose.PSD

Comme la méthode travaille avec un `float`, vous pouvez spécifier un **angle de rotation d’image spécifique** comme `22.5f` pour un contrôle précis dans les flux de travail de conception graphique.

#### Résumé de l’exemple Java de rotation d’image

Toutes les étapes ci‑dessus démontrent un flux complet **rotate image java** — du chargement du fichier à l’enregistrement du résultat pivoté.

### Étape 6 : Enregistrer le résultat

```java
image.save(destName, new JpegOptions());
```

`JpegOptions` vous permet de contrôler la qualité, la compression et d’autres paramètres spécifiques au JPEG. Pour une sortie sans perte, remplacez‑le par `PngOptions`.

## Problèmes courants et solutions

| Problème | Cause | Solution |
|----------|-------|----------|
| **Coins vides après rotation** | Aucun couleur d’arrière‑plan fournie | Passez un `Color` (ex. `Color.getWhite()`) à `rotate`. |
| **Erreur out‑of‑memory sur de gros PSD** | Image non mise en cache | Appelez `image.cacheData()` avant le traitement. |
| **Direction d’angle incorrecte** | Confusion entre angle négatif et positif | Utilisez des valeurs négatives pour une rotation horaire (ou inverse selon votre système de coordonnées). |
| **Modifications non enregistrées** | Oubli d’appeler `save` | Assurez‑vous que `image.save(...)` est exécuté après la rotation. |

## Questions fréquentes

**Q : Puis‑je faire pivoter des images avec transparence en utilisant Aspose.PSD pour Java ?**  
R : Oui. La bibliothèque préserve les canaux alpha ; évitez simplement de spécifier une couleur d’arrière‑plan opaque si vous voulez des coins transparents.

**Q : Existe‑t‑il des limitations sur les formats de fichiers image supportés pour la rotation ?**  
R : Non. Aspose.PSD prend en charge PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF, et bien d’autres.

**Q : Puis‑je faire pivoter des images avec un angle négatif ?**  
R : Absolument. Passez un float négatif à `rotate` (ex. `-30f`) pour une rotation horaire.

**Q : Aspose.PSD fournit‑il un aperçu en temps réel pendant la rotation ?**  
R : L’API est uniquement côté serveur. Pour des aperçus en direct, intégrez le bitmap pivoté dans un framework UI (Swing, JavaFX) et rafraîchissez la vue.

**Q : Existe‑t‑il un forum communautaire pour Aspose.PSD où je peux demander de l’aide ?**  
R : Oui, visitez le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour poser des questions et partager vos expériences.

## Conclusion

Vous savez maintenant **comment faire pivoter une image** à un angle précis en utilisant Aspose.PSD pour Java. En tirant parti de la mise en cache, du contrôle de la couleur d’arrière‑plan et des options de sortie flexibles, vous pouvez intégrer une fonctionnalité de rotation précise dans n’importe quel flux de travail d’image basé sur Java.

---

**Dernière mise à jour :** 2026-02-12  
**Testé avec :** Aspose.PSD pour Java 24.11 (dernière version au moment de la rédaction)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}