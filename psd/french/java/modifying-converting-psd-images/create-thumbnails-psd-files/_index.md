---
date: 2026-03-13
description: Apprenez à créer des miniatures PSD en Java avec Aspose.PSD. Suivez notre
  guide étape par étape pour générer rapidement des miniatures à partir de fichiers
  PSD.
linktitle: Create Thumbnails from PSD Files using Java
second_title: Aspose.PSD Java API
title: Créer une vignette PSD en Java – Générer des vignettes à partir de PSD
url: /fr/java/modifying-converting-psd-images/create-thumbnails-psd-files/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Créer une miniature PSD Java – Générer des miniatures à partir de PSD

## Introduction
Si vous avez besoin de **create PSD thumbnail Java** code qui extrait les images d'aperçu des fichiers Photoshop, vous êtes au bon endroit. Que vous construisiez un gestionnaire d'actifs numériques, une galerie web ou un pipeline de traitement par lots automatisé, générer des miniatures à partir de fichiers PSD peut améliorer considérablement les performances et l'expérience utilisateur. Dans ce tutoriel, nous passerons en revue l'ensemble du processus avec Aspose.PSD for Java, en vous montrant comment charger un PSD, localiser ses ressources de miniature intégrées et les enregistrer en tant que fichiers image séparés.

## Quick Answers
- **Quelle bibliothèque est la meilleure pour l'extraction de miniatures PSD ?** Aspose.PSD for Java.  
- **Combien de temps prend l'implémentation ?** Environ 10‑15 minutes pour une configuration de base.  
- **Dois‑je installer Photoshop ?** Non, Aspose.PSD fonctionne de façon indépendante.  
- **Quels formats d'image puis‑je exporter la miniature ?** Tout format pris en charge par Aspose.PSD (par ex., BMP, PNG, JPEG).  
- **Une licence est‑elle requise pour la production ?** Oui, une licence commerciale est nécessaire pour une utilisation en production.

## What is “create PSD thumbnail Java”?
Créer une miniature PSD en Java signifie lire de façon programmatique l'aperçu de la miniature stocké à l'intérieur d'un document Photoshop (PSD) et l'écrire en tant que fichier image séparé. Cela est utile pour générer des aperçus rapides sans charger le contenu complet, souvent volumineux, du PSD.

## Why use Aspose.PSD for this task?
- **Pas de dépendance à Photoshop :** Fonctionne sur n'importe quelle plateforme avec un JDK.  
- **Support complet du PSD :** Gère toutes les versions et ressources PSD, y compris les miniatures.  
- **API simple :** Quelques lignes de code pour extraire et enregistrer les miniatures.  
- **Optimisé pour les performances :** Gestion efficace de la mémoire pour les gros fichiers.

## Prerequisites
Avant de plonger dans les détails de la création de miniatures, couvrons ce dont vous aurez besoin pour commencer.

### Java Development Environment
- **Java JDK :** Assurez‑vous d'avoir le Java Development Kit (JDK) installé sur votre ordinateur. Vous pouvez le télécharger [ici](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
- **IDE :** Un environnement de développement intégré (IDE) comme IntelliJ IDEA, Eclipse ou NetBeans facilitera le codage.

### Aspose.PSD Library
- Vous devez inclure la bibliothèque Aspose.PSD dans votre projet. Vous pouvez [télécharger la dernière version ici](https://releases.aspose.com/psd/java/).

### Basic Knowledge of Java
- Une bonne connaissance des bases de Java vous aidera à parcourir le code d'exemple plus efficacement. Des concepts tels que les classes, les objets et les boucles seront fréquemment utilisés.

## Import Packages
Commencez par importer les classes nécessaires de la bibliothèque Aspose.PSD. Cette étape est cruciale car elle vous permet d'exploiter les fonctionnalités de la bibliothèque dans votre code.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.ThumbnailFormat;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

Les prérequis étant réglés, passons à l'essentiel ! La création de miniatures à partir de fichiers PSD implique quelques étapes simples, et je vais les détailler pour vous.

## Comment créer PSD thumbnail Java – Guide étape par étape

### Étape 1 : Configurer votre environnement
Voici comment initier votre projet et préparer la génération de miniatures.

1. **Créer un projet Java**  
   - Ouvrez votre IDE et créez un nouveau projet Java.  
   - Nommez‑le quelque chose comme `"PsdThumbnailGenerator"`.

2. **Inclure la bibliothèque Aspose.PSD**  
   - Ajoutez le fichier JAR Aspose.PSD à votre chemin de construction du projet.  
   - Si vous utilisez Maven, incluez‑le dans votre `pom.xml` :

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-psd</artifactId>
    <version>your_version_here</version>
</dependency>
```

### Étape 2 : Charger le fichier PSD
Ensuite, nous devons charger le fichier PSD à partir duquel nous voulons créer des miniatures.

1. **Spécifier le répertoire de vos documents**  
   Définissez le répertoire où se trouve votre fichier PSD.

```java
String dataDir = "Your Document Directory"; // Replace with your path
```

2. **Charger le fichier PSD**  
   Utilisez la classe `PsdImage` pour charger votre fichier PSD.

```java
PsdImage image = (PsdImage) Image.load(dataDir + "sample.psd");
```

> **Astuce :** Conservez vos fichiers PSD dans un dossier dédié (par ex., `src/main/resources`) pour éviter les problèmes de chemin.

### Étape 3 : Parcourir les ressources PSD
Maintenant que notre image PSD est chargée, l'étape suivante consiste à examiner ses ressources.

1. **Obtenir le nombre de ressources**  
   Nous parcourrons toutes les ressources du fichier PSD.

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // Processing resources
}
```

2. **Identifier les ressources de miniature**  
   À l'intérieur de la boucle, vérifiez si une ressource est une miniature.

```java
if (image.getImageResources()[i] instanceof ThumbnailResource) {
    // Process the thumbnail
}
```

### Étape 4 : Traiter la miniature
Une fois que nous avons identifié une ressource de miniature, nous devons la gérer en conséquence.

1. **Récupérer et vérifier le format de la miniature**  
   Si la ressource est bien une miniature, récupérez‑la et vérifiez son format.

```java
ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
if (thumbnail.getFormat() == ThumbnailFormat.KJpegRgb) {
    // Create and save the thumbnail
}
```

### Étape 5 : Créer et enregistrer la miniature
C'est ici que la magie opère ! Nous créerons une nouvelle image à partir des données de la miniature et l'enregistrerons.

1. **Créer une nouvelle image**  
   Nous utiliserons la largeur et la hauteur de la ressource de miniature pour créer une nouvelle image bitmap.

```java
PsdImage thumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
```

2. **Stocker les pixels dans la nouvelle image**  
   Transférez les données de la miniature vers l'image nouvellement créée.

```java
thumbnailImage.savePixels(thumbnailImage.getBounds(), thumbnail.getThumbnailData());
```

3. **Enregistrer l'image de la miniature**  
   Enfin, enregistrez l'image de la miniature dans votre répertoire de documents avec un nom unique.

```java
thumbnailImage.save(dataDir + "CreateThumbnailsFromPSDFiles_out_" + i + ".bmp");
```

> **Erreur fréquente :** Oublier de fermer les objets `PsdImage` peut entraîner des fuites de mémoire. Enveloppez le code de gestion d'image dans un bloc try‑with‑resources si vous utilisez Java 7+.

## Conclusion
En suivant ces étapes, vous disposez désormais d'une méthode solide et réutilisable pour **create PSD thumbnail Java** qui extrait les images d'aperçu de n'importe quel fichier Photoshop. Cette technique peut être intégrée aux traitements par lots, aux services web ou aux utilitaires de bureau pour accélérer le catalogage d'images et améliorer la réactivité de l'interface utilisateur. Essayez‑la avec votre propre collection de PSD et voyez à quelle vitesse vous pouvez générer des aperçus légers !

## FAQ
### Qu'est‑ce que Aspose.PSD ?
Aspose.PSD est une bibliothèque Java qui permet aux développeurs de travailler avec des fichiers Photoshop, facilitant la manipulation et la gestion des fichiers PSD de manière programmatique.

### Puis‑je utiliser Aspose.PSD gratuitement ?
Oui, Aspose propose un essai gratuit que vous pouvez utiliser pour tester la bibliothèque avant d'acheter une licence.

### Quels formats puis‑je enregistrer les miniatures ?
Dans cet exemple, nous avons enregistré les miniatures au format BMP, mais Aspose.PSD prend en charge divers autres formats également.

### Dois‑je installer Photoshop pour utiliser Aspose.PSD ?
Non, Aspose.PSD fonctionne indépendamment de Photoshop.

### Où puis‑je trouver plus d'informations sur Aspose.PSD ?
Vous pouvez consulter la [documentation Aspose.PSD](https://reference.aspose.com/psd/java/) pour plus de détails, tutoriels et ressources.

## Questions fréquemment posées

**Q : Comment extraire les miniatures d'un PSD protégé par mot de passe ?**  
R : Chargez le PSD avec la surcharge appropriée de `Image.load` qui accepte un paramètre de mot de passe.

**Q : Puis‑je générer des miniatures en PNG au lieu de BMP ?**  
R : Absolument. Modifiez l'extension du fichier dans la méthode `save` et Aspose.PSD gérera la conversion.

**Q : Existe‑t‑il un moyen de traiter plusieurs fichiers PSD par lots ?**  
R : Enveloppez le code dans une boucle qui parcourt un répertoire de fichiers PSD, en réutilisant la même logique d'extraction pour chaque fichier.

**Q : Quelle version de Java est requise ?**  
R : Aspose.PSD prend en charge Java 8 et ultérieur. Utiliser le JDK le plus récent est recommandé pour les performances et la sécurité.

**Q : La bibliothèque gère‑t‑elle efficacement les gros fichiers PSD ?**  
R : Oui, Aspose.PSD utilise le chargement paresseux et une gestion optimisée de la mémoire pour travailler avec de gros fichiers sans épuiser l'espace du tas.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Dernière mise à jour :** 2026-03-13  
**Testé avec :** Aspose.PSD 24.11 for Java (latest at time of writing)  
**Auteur :** Aspose  

---