---
date: 2026-01-01
description: Maîtrisez le traitement d'images Java en apprenant à recadrer des images
  avec Aspose.PSD pour Java. Un tutoriel complet pour une manipulation d'images fluide.
linktitle: Crop Image by Shifts
second_title: Aspose.PSD Java API
title: Traitement d'images Java – Recadrer l'image par décalages avec Aspose.PSD
url: /fr/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Traitement d'images Java – Rogner une image par décalages avec Aspose.PSD

## Introduction

Si vous travaillez sur le **traitement d'images Java**, vous découvrirez rapidement que le rognage précis est un bloc de construction fondamental pour tout flux de travail graphique. Que vous ayez besoin de couper les bordures, de supprimer un arrière‑plan indésirable ou de préparer des actifs pour la diffusion sur le web, savoir **comment rogner une image** de façon programmatique vous fait gagner d'innombrables heures de travail manuel. Dans ce tutoriel, nous parcourrons le rognage d’une image raster en spécifiant des valeurs de décalage pour chaque côté, à l’aide de la puissante bibliothèque **Aspose.PSD for Java**. À la fin, vous serez capable d'**utiliser la méthode de rognage** en toute confiance et même d'**optimiser le rognage d'images** pour de meilleures performances.

## Réponses rapides
- **Quelle bibliothèque gère le traitement d'images Java ?** Aspose.PSD for Java  
- **Quelle méthode rogne une image raster ?** `RasterImage.crop(left, right, top, bottom)`  
- **Dois‑je mettre en cache les données au préalable ?** Oui – le cache améliore la vitesse pour les gros fichiers PSD  
- **Puis‑je définir des marges de rognage personnalisées ?** Absolument – spécifiez les décalages gauche, droite, haut et bas  
- **Quels formats de sortie sont pris en charge ?** JPEG, PNG, BMP, et bien d’autres via `ImageOptions`

## Qu’est‑ce que le traitement d'images Java ?
Le traitement d'images Java désigne la manipulation de graphiques bitmap et vectoriels à l’aide d’API basées sur Java. Les tâches incluent le redimensionnement, le filtrage, la conversion de format et les **ajustements de marges de rognage d’image** – le tout pouvant être automatisé dans des applications côté serveur ou de bureau.

## Pourquoi utiliser Aspose.PSD pour le traitement d'images Java ?
Aspose.PSD propose une solution pure Java qui comprend les fichiers PSD compatibles Photoshop, les calques, les canaux et les masques. Elle élimine le besoin de bibliothèques natives, fonctionne sur toutes les plateformes et fournit une API **crop raster image** simple à intégrer dans les projets Java existants.

## Prérequis

- **Java Development Kit (JDK)** – téléchargez la dernière version depuis [ici](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **Aspose.PSD for Java Library** – obtenez la version la plus récente depuis la [page de téléchargement](https://releases.aspose.com/psd/java/).  
- **Environnement de développement intégré (IDE)** – Eclipse, IntelliJ IDEA, ou tout autre éditeur de votre choix.

## Importer les packages

Dans votre projet Java, importez les classes nécessaires pour démarrer le flux de travail de rognage :

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Guide étape par étape

### Étape 1 : Charger l’image (comment rogner une image)

Tout d’abord, chargez le fichier PSD source dans une instance `RasterImage`. Cela vous donne un accès direct au niveau des pixels.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### Étape 2 : Mettre en cache les données de l’image (optimiser le rognage d’image)

Mettre en cache les données de l’image en mémoire réduit la surcharge d’E/S lors de l’exécution de plusieurs opérations telles que le rognage.

```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### Étape 3 : Définir les marges de rognage (marges de rognage d’image)

Spécifiez le nombre de pixels à supprimer de chaque côté. Ajustez ces valeurs pour correspondre aux **marges de rognage d’image** souhaitées.

```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### Étape 4 : Appliquer le rognage (utiliser la méthode crop)

Appelez maintenant la méthode `crop` avec les valeurs de décalage. Cette opération **crop raster image** modifie le bitmap sous‑jacent.

```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

### Étape 5 : Enregistrer les résultats (comment rogner une image vers un nouveau format)

Enfin, écrivez l’image rognée sur le disque. Dans cet exemple nous choisissons le JPEG, mais tout format pris en charge par Aspose.PSD peut être utilisé.

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

Félicitations ! Vous avez réussi à **rogner une image par décalages** à l’aide d’Aspose.PSD for Java, une compétence essentielle dans toute boîte à outils de **traitement d'images Java**.

## Problèmes courants et solutions

| Problème | Solution |
|----------|----------|
| **`OutOfMemoryError` sur de gros fichiers PSD** | Assurez‑vous d’appeler `cacheData()` (Étape 2) et envisagez d’augmenter la taille du tas JVM (`-Xmx`). |
| **Bordures transparentes inattendues** | Vérifiez que vos valeurs de décalage reflètent correctement les marges souhaitées ; des valeurs négatives peuvent agrandir plutôt que réduire. |
| **Enregistrement dans le mauvais format** | Utilisez la sous‑classe `ImageOptions` appropriée (par ex., `PngOptions`) lors de l’appel à `save`. |

## Questions fréquemment posées

**Q : Aspose.PSD est‑il compatible avec tous les formats d’image ?**  
R : Oui, Aspose.PSD prend en charge un large éventail de formats raster et vectoriels, garantissant une grande polyvalence dans vos projets.

**Q : Puis‑je appliquer plusieurs opérations de rognage à la même image ?**  
R : Absolument. Vous pouvez appeler `crop` de façon répétée ; chaque appel agit sur l’état actuel de l’image.

**Q : Existe‑t‑il un forum communautaire pour le support d’Aspose.PSD ?**  
R : Oui, vous pouvez obtenir de l’aide et échanger avec la communauté sur le [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q : Comment obtenir une licence temporaire pour Aspose.PSD ?**  
R : Rendez‑vous [ici](https://purchase.aspose.com/temporary-license/) pour obtenir une licence temporaire.

**Q : Y a‑t‑il des projets d’exemple illustrant les fonctionnalités d’Aspose.PSD ?**  
R : Explorez la documentation et les exemples sur la [Documentation Aspose.PSD Java](https://reference.aspose.com/psd/java/).

## Conclusion

Dans ce guide, nous avons couvert tout ce qu’il faut savoir pour **rogner des fichiers raster image** en spécifiant des valeurs de décalage, une technique essentielle pour un **traitement d'images Java** finement réglé. Vous disposez maintenant d’une base solide pour intégrer le rognage dans des flux de travail plus larges, que ce soit pour préparer des actifs web, générer des miniatures ou nettoyer des documents numérisés.

---

**Dernière mise à jour :** 2026-01-01  
**Testé avec :** Aspose.PSD 24.11 for Java  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}