---
date: 2025-12-08
description: Apprenez à convertir des fichiers PSD en PNG et à redimensionner les
  images proportionnellement en Java avec Aspose.PSD. Ce tutoriel étape par étape
  couvre la mise en cache des images, le redimensionnement et l'enregistrement au
  format PNG.
linktitle: Convert PSD to PNG & Resize Proportionally
second_title: Aspose.PSD Java API
title: Comment convertir un PSD en PNG et redimensionner proportionnellement avec
  Aspose.PSD pour Java
url: /fr/java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment convertir un PSD en PNG et redimensionner proportionnellement avec Aspose.PSD pour Java

## Introduction

Si vous devez **convertir un PSD en PNG** tout en conservant le rapport d’aspect d’origine, vous êtes au bon endroit. Dans ce tutoriel, nous parcourrons un **tutoriel Aspose.PSD** complet qui montre comment **redimensionner proportionnellement les images** en Java, mettre en cache l’image pour des performances optimales, puis enregistrer le résultat au format PNG. À la fin, vous pourrez intégrer ce flux de travail dans n’importe quel pipeline de traitement d’images basé sur Java.

## Réponses rapides
- **Aspose.PSD peut‑il convertir un PSD en PNG ?** Oui – il suffit de charger le PSD et de l’enregistrer avec `PngOptions`.
- **La bibliothèque prend‑elle en charge le redimensionnement proportionnel ?** Absolument ; utilisez `resizeWidthProportionally` et `resizeHeightProportionally`.
- **Dois‑je mettre l’image en cache d’abord ?** Le cache (`image.cacheData()`) améliore les performances pour les gros fichiers PSD.
- **Quelle version de Java est requise ?** Java 8 ou supérieur est pleinement pris en charge.
- **Une licence est‑elle nécessaire en production ?** Oui, une licence commerciale supprime les filigranes d’évaluation.

## Qu’est‑ce que « convertir PSD en PNG » et pourquoi est‑ce important ?

Convertir un document Photoshop (PSD) en fichier Portable Network Graphics (PNG) vous permet de partager des conceptions à calques sous un format léger et adapté au web. Le PNG conserve la transparence et la qualité sans perte, ce qui le rend idéal pour les actifs UI, les vignettes ou tout scénario où la fidélité de l’image est cruciale.

## Pourquoi redimensionner une image proportionnellement en Java ?

Redimensionner **sans déformer le rapport d’aspect** garantit que les graphiques restent naturels sur différents écrans. L’API `Aspose.PSD` propose des méthodes dédiées au redimensionnement proportionnel, qui calculent automatiquement la hauteur ou la largeur correspondante, vous évitant ainsi les erreurs de calcul manuelles.

## Prérequis

Avant de plonger dans le code, assurez‑vous d’avoir :

1. **Java Development Kit (JDK)** – Java 8 ou version ultérieure installé.
2. **Aspose.PSD for Java** – téléchargez le dernier JAR depuis le site officiel [ici](https://releases.aspose.com/psd/java/).
3. Un fichier PSD d’exemple (`sample.psd`) placé dans un répertoire que vous pouvez référencer depuis votre projet.

## Importer les packages

Ajoutez les imports nécessaires à votre classe Java. Ces classes vous donnent accès au chargement d’image, au cache, au redimensionnement et aux options de sortie PNG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## Étape 1 : charger l’image PSD

Tout d’abord, chargez le fichier PSD source. Si le fichier est volumineux, mettre en cache les données de l’image réduit la consommation de mémoire lors des opérations suivantes.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## Étape 2 : redimensionner l’image proportionnellement (Java)

Déterminez maintenant les nouvelles dimensions. Dans cet exemple, nous réduisons l’image à **la moitié** de sa taille originale tout en préservant le rapport d’aspect. Vous pouvez ajuster la largeur ou la hauteur cible selon vos besoins.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **Astuce :** Utilisez soit `resizeWidthProportionally` *soit* `resizeHeightProportionally` — la bibliothèque calcule automatiquement l’autre dimension pour garder l’image proportionnelle.

## Étape 3 : enregistrer l’image redimensionnée au format PNG

Enfin, exportez l’image redimensionnée au format PNG. Cette étape finalise le flux de travail **convertir PSD en PNG**.

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

Lorsque le code s’exécute, vous trouverez un fichier PNG qui fait moitié moins grand que le PSD d’origine, avec la même qualité visuelle et aucune distorsion.

## Problèmes courants et solutions

| Problème | Cause | Solution |
|----------|-------|----------|
| **OutOfMemoryError** | Grand PSD non mis en cache | Appelez `image.cacheData()` avant le redimensionnement |
| **PNG de sortie vide** | Chemin de fichier incorrect | Vérifiez `dataDir` et les permissions d’écriture |
| **Le rapport d’aspect semble incorrect** | Utilisation simultanée de la largeur et de la hauteur manuellement | Utilisez les méthodes proportionnelles fournies par Aspose.PSD |

## Questions fréquentes

**Q : Aspose.PSD est‑il compatible avec tous les formats d’image ?**  
A : Aspose.PSD prend en charge PSD, PNG, JPEG, BMP, GIF et bien d’autres. Consultez la liste complète dans la [documentation](https://reference.aspose.com/psd/java/).

**Q : Puis‑je utiliser Aspose.PSD pour des projets commerciaux ?**  
A : Oui. Achetez une licence commerciale sur la [boutique Aspose](https://purchase.aspose.com/buy).

**Q : Des licences temporaires sont‑elles disponibles pour les tests ?**  
A : Absolument – demandez une licence temporaire [ici](https://purchase.aspose.com/temporary-license/) pour les évaluations.

**Q : Où puis‑je trouver du support communautaire ?**  
A : Le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) est un excellent endroit pour poser des questions et partager des solutions.

**Q : Comment accéder à la référence complète de l’API ?**  
A : La documentation détaillée de l’API est disponible [ici](https://reference.aspose.com/psd/java/).

## Conclusion

Vous savez maintenant comment **convertir un PSD en PNG**, redimensionner l’image proportionnellement et gérer le cache efficacement avec Aspose.PSD pour Java. Intégrez ces étapes dans vos propres applications pour offrir un traitement d’image rapide et de haute qualité sans dépendre d’une installation native de Photoshop.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Dernière mise à jour :** 2025-12-08  
**Testé avec :** Aspose.PSD 24.12 for Java  
**Auteur :** Aspose