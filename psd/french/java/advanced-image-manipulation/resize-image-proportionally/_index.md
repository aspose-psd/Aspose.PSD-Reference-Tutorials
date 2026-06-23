---
date: 2026-06-23
description: Apprenez à convertir PSD en PNG et à redimensionner les images proportionnellement
  en Java avec Aspose.PSD. Ce tutoriel étape par étape couvre la mise en cache des
  images, le redimensionnement et l'enregistrement au format PNG.
keywords:
- convert psd to png
- save psd as png
- how to cache image
- resize image without distortion
- proportional image scaling
linktitle: Convertir PSD en PNG et redimensionner proportionnellement
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to convert PSD to PNG and resize images proportionally in
    Java using Aspose.PSD. This step‑by‑step tutorial covers image caching, resizing,
    and saving as PNG.
  headline: How to Convert PSD to PNG and Resize Proportionally with Aspose.PSD for
    Java
  type: TechArticle
- description: Learn how to convert PSD to PNG and resize images proportionally in
    Java using Aspose.PSD. This step‑by‑step tutorial covers image caching, resizing,
    and saving as PNG.
  name: How to Convert PSD to PNG and Resize Proportionally with Aspose.PSD for Java
  steps:
  - name: '**Java Development Kit (JDK)** – Java 8 or later installed.'
    text: '**Java Development Kit (JDK)** – Java 8 or later installed.'
  - name: '**Aspose.PSD for Java** – download the latest JAR from the official site [here](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – download the latest JAR from the official site [here](https://releases.aspose.com/psd/java/).'
  - name: A sample PSD file (`sample.psd`) placed in a directory you can reference
      from your project.
    text: A sample PSD file (`sample.psd`) placed in a directory you can reference
      from your project.
  type: HowTo
- questions:
  - answer: Aspose.PSD supports PSD, PNG, JPEG, BMP, GIF, and many more. See the full
      list in the [documentation](https://reference.aspose.com/psd/java/). For the
      full API reference, see the guide **here**.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Yes. Purchase a commercial license on the [Aspose store](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for commercial projects?
  - answer: Absolutely – request a temporary license [here](https://purchase.aspose.com/temporary-license/)
      for evaluation purposes.
    question: Are temporary licenses available for testing?
  - answer: The [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) is a great place
      to ask questions and share solutions.
    question: Where can I find community support?
  - answer: Detailed API docs are available [here](https://reference.aspose.com/psd/java/).
    question: How do I access the full API reference?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Comment convertir PSD en PNG et redimensionner proportionnellement avec Aspose.PSD
  pour Java
url: /fr/java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment convertir un PSD en PNG et redimensionner proportionnellement avec Aspose.PSD pour Java

## Introduction

Si vous devez **convertir PSD en PNG** tout en conservant le ratio d'aspect d'origine, vous êtes au bon endroit. Dans ce tutoriel **Aspose.PSD Java**, nous parcourrons un **tutoriel complet de traitement d'images Java** qui vous montre **comment redimensionner les images** proportionnellement, mettre en cache l'image pour des performances optimales, et enfin enregistrer le résultat au format PNG. À la fin, vous pourrez intégrer ce flux de travail dans n'importe quel pipeline de traitement d'images basé sur Java.

## Réponses rapides
- **Aspose.PSD peut-il convertir PSD en PNG ?** Oui – il suffit de charger le PSD et de l'enregistrer avec `PngOptions`.
- **La bibliothèque prend-elle en charge le redimensionnement proportionnel ?** Absolument ; utilisez `resizeWidthProportionally` et `resizeHeightProportionally`.
- **Dois‑je mettre en cache l'image d'abord ?** Le cache (`image.cacheData()`) améliore les performances pour les gros fichiers PSD.
- **Quelle version de Java est requise ?** Java 8 ou plus récent est entièrement pris en charge.
- **Une licence est‑elle nécessaire en production ?** Oui, une licence commerciale supprime les filigranes d'évaluation.

## Qu'est‑ce que « convertir PSD en PNG » et pourquoi est‑ce important ?

**convert PSD to PNG** signifie transformer un document Photoshop à calques en un fichier PNG sans perte, à couche unique, qui préserve la transparence et la fidélité visuelle. Cette conversion vous permet de partager des conceptions sans nécessiter Photoshop, crée des actifs et des vignettes prêts pour le web, et décharge les gros fichiers PSD des navigateurs clients tout en maintenant la qualité requise pour les composants UI et le branding.

## Pourquoi redimensionner une image proportionnellement en Java ?

Redimensionner une image **sans distorsion** conserve le ratio largeur‑hauteur d'origine, de sorte que les graphiques conservent leur apparence prévue sur n'importe quelle taille d'écran. Les méthodes de mise à l'échelle proportionnelle d'Aspose.PSD calculent automatiquement la dimension manquante, éliminant les calculs manuels et le risque d'images étirées ou écrasées.

## Pourquoi cela importe aux développeurs

Pour les développeurs, le redimensionnement proportionnel et la conversion PSD‑vers‑PNG réduisent la consommation de mémoire et améliorent les temps de chargement, garantissant que les applications gèrent efficacement les graphiques volumineux. En redimensionnant les images tôt, vous maintenez une cohérence de rendu UI sur tous les appareils et éliminez le besoin de Photoshop sur les serveurs de construction, ce qui simplifie le déploiement et réduit les coûts opérationnels.

- **Réduction de la taille du fichier PSD** – En réduisant la taille des gros PSD avant la conversion, vous diminuez l'utilisation de la mémoire et accélérez le traitement en aval.  
- **Rendu UI cohérent** – Le redimensionnement proportionnel garantit que les icônes et graphiques conservent leur équilibre visuel sur tous les appareils.  
- **Aucune dépendance à Photoshop** – Vous pouvez exécuter ces opérations sur un serveur ou dans une pipeline CI sans installer Photoshop.

## Prérequis

1. **Java Development Kit (JDK)** – Java 8 ou version ultérieure installé.  
2. **Aspose.PSD for Java** – téléchargez le JAR le plus récent depuis le site officiel [here](https://releases.aspose.com/psd/java/).  
3. Un fichier PSD d'exemple (`sample.psd`) placé dans un répertoire que vous pouvez référencer depuis votre projet.

## Importer les packages

La classe `PsdImage` est l'objet principal d'Aspose.PSD qui représente un fichier PSD en mémoire. Importez les espaces de noms nécessaires pour travailler avec le chargement, le cache, le redimensionnement et l'export PNG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## Étape 1 : Charger l'image PSD

**Réponse directe :** Chargez le fichier source avec `new PsdImage("sample.psd")` ; puis appelez `image.cacheData()` pour pré‑charger les données de l'image, ce qui empêche les lectures disque répétées lors des opérations ultérieures.

`cacheData()` charge l'intégralité du PSD en mémoire, permettant un traitement ultérieur plus rapide. La méthode `cacheData()` lit tout le document en mémoire, accélérant le traitement ultérieur pour les gros fichiers. Tout d'abord, chargez le fichier PSD source. Si le fichier est volumineux, mettre en cache les données de l'image réduit les fluctuations de mémoire lors des opérations suivantes.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## Étape 2 : Redimensionner l'image proportionnellement (Java)

**Réponse directe :** Appelez `image.resizeWidthProportionally(targetWidth)` (ou `resizeHeightProportionally`) pour réduire l'image tout en préservant automatiquement le ratio d'aspect d'origine.

`resizeWidthProportionally(int targetWidth)` ajuste la largeur de l'image et calcule automatiquement la hauteur correspondante pour préserver le ratio d'aspect d'origine. Décidez maintenant des nouvelles dimensions. Dans cet exemple, nous réduisons l'image à **la moitié** de sa taille originale tout en conservant le ratio d'aspect. Vous pouvez ajuster la largeur ou la hauteur cible selon vos besoins.

La méthode `resizeWidthProportionally` calcule la hauteur correspondante en fonction du ratio original, de sorte que l'image est redimensionnée **sans distorsion**. Utilisez l'une ou l'autre méthode — Aspose.PSD gère la dimension complémentaire pour vous.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **Astuce :** Utilisez soit `resizeWidthProportionally` *ou* `resizeHeightProportionally` — la bibliothèque calcule automatiquement l'autre dimension pour garder l'image proportionnelle.

## Étape 3 : Enregistrer l'image redimensionnée au format PNG

**Réponse directe :** Créez une instance de `PngOptions`, assignez‑la à l'image, puis invoquez `image.save("output.png", pngOptions)` pour écrire le fichier redimensionné au format PNG.

`PngOptions` spécifie les paramètres d'export PNG tels que le niveau de compression et la profondeur de couleur. Enfin, exportez l'image redimensionnée au format PNG. Cette étape finalise le flux de travail **convert PSD to PNG**.

Lorsque le code s'exécute, vous trouverez un fichier PNG qui fait moitié moins que le PSD original, avec la même qualité visuelle et aucune distorsion.

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

Lorsque le code s'exécute, vous trouverez un fichier PNG qui fait moitié moins que le PSD original, avec la même qualité visuelle et aucune distorsion.

## Problèmes courants et solutions

| Problème | Cause | Solution |
|----------|-------|----------|
| **OutOfMemoryError** | Gros PSD non mis en cache | Appelez `image.cacheData()` avant le redimensionnement |
| **Sortie PNG vide** | Chemin de fichier incorrect | Vérifiez `dataDir` et les permissions d'écriture |
| **Ratio d'aspect incorrect** | Utilisation manuelle de la largeur et de la hauteur | Utilisez les méthodes proportionnelles fournies par Aspose.PSD |

## Conseils pour réduire la taille des fichiers PSD

- **Recadrer les calques inutiles** avant de charger le fichier.  
- **Redimensionner proportionnellement** comme montré ci‑dessus pour réduire les dimensions tôt.  
- **Enregistrer en PNG avec une profondeur de bits appropriée** afin d'éviter les données superflues.

## Questions fréquemment posées

**Q : Aspose.PSD est‑il compatible avec tous les formats d'image ?**  
R : Aspose.PSD prend en charge PSD, PNG, JPEG, BMP, GIF et bien d'autres. Consultez la liste complète dans la [documentation](https://reference.aspose.com/psd/java/). Pour la référence complète de l'API, voir le guide **here**.

**Q : Puis‑je utiliser Aspose.PSD pour des projets commerciaux ?**  
R : Oui. Achetez une licence commerciale sur le [Aspose store](https://purchase.aspose.com/buy).

**Q : Des licences temporaires sont‑elles disponibles pour les tests ?**  
R : Absolument – demandez une licence temporaire [here](https://purchase.aspose.com/temporary-license/) à des fins d'évaluation.

**Q : Où puis‑je trouver du support communautaire ?**  
R : Le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) est un excellent endroit pour poser des questions et partager des solutions.

**Q : Comment accéder à la référence complète de l'API ?**  
R : La documentation détaillée de l'API est disponible [here](https://reference.aspose.com/psd/java/).

## Conclusion

Vous savez maintenant comment **convertir PSD en PNG**, **redimensionner une image proportionnellement**, et gérer le cache efficacement avec Aspose.PSD pour Java. Intégrez ces étapes dans vos propres applications pour offrir un traitement d'image rapide et de haute qualité sans dépendre d'installations Photoshop natives. Cette approche **aspose psd java** constitue une partie fiable de tout **java image processing tutorial** et vous aide à maîtriser la taille des fichiers PSD tout en préservant la fidélité visuelle.

---

**Last Updated:** 2026-06-23  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose

{{< blocks/products/products-backtop-button >}}

## Tutoriels associés

- [Simple Resizing with Aspose.PSD – Java Image Manipulation Library](/psd/java/basic-image-operations/simple-resizing/)
- [Resize Image Java - Using Resize Type Enumeration in Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)
- [High Quality Image Scaling with Bicubic Resampler in Aspose.PSD for Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}