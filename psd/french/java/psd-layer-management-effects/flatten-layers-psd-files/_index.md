---
date: 2026-04-03
description: Apprenez comment réduire la taille des fichiers PSD en aplatissant les
  calques avec Aspose.PSD pour Java. Ce guide étape par étape montre comment aplatir
  rapidement les fichiers PSD.
keywords:
- reduce psd file size
- how to flatten psd
- flatten visible layers psd
linktitle: Réduire la taille du fichier PSD en aplatissant les calques – Aspose.PSD
  Java
second_title: Aspose.PSD Java API
title: Réduire la taille du fichier PSD en aplatissant les calques – Aspose.PSD Java
url: /fr/java/psd-layer-management-effects/flatten-layers-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Réduire la taille du fichier PSD en aplatissant les calques – Aspose.PSD Java

## Introduction

If you’ve ever opened a Photoshop document and wondered how to **reduce PSD file size**, flattening layers is one of the most effective tricks. With Aspose.PSD for Java you can programmatically flatten an entire PSD or merge only the layers you choose, giving you fine‑grained control over file weight without sacrificing visual quality. In this tutorial we’ll walk through both approaches—flattening the whole image and merging specific layers—so you can quickly shrink your PSD files and keep your workflow smooth.

## Réponses rapides
- **Qu'est‑ce que l'aplatissement fait ?** Il fusionne les calques visibles en un seul calque d'arrière‑plan, supprime les informations de calque et réduit souvent la taille du fichier.  
- **Puis‑je aplatir uniquement les calques sélectionnés ?** Oui, vous pouvez fusionner des calques spécifiques tout en laissant les autres intacts.  
- **Ai‑je besoin d'une licence ?** Un essai gratuit fonctionne pour le développement ; une licence commerciale est requise pour la production.  
- **Quelle version de Java est requise ?** JDK 8 ou supérieur.  
- **L'aplatissement affectera‑t‑il la qualité de l'image ?** Non, l'apparence visuelle reste la même ; seule la structure des calques change.

## Qu'est‑ce que « réduire la taille d'un fichier PSD » ?

Réduire la taille d'un fichier PSD signifie supprimer les données inutiles — comme des calques supplémentaires, des canaux masqués ou des métadonnées excessives — afin que le fichier devienne plus léger et plus rapide à charger, partager ou traiter. L'aplatissement des calques est une technique courante car elle élimine les objets de calque séparés tout en préservant l'image composite finale.

## Pourquoi aplatir les calques avec Aspose.PSD pour Java ?

- **Automatisation :** Pas besoin d'ouvrir Photoshop manuellement ; intégrez directement dans vos applications Java.  
- **Précision :** Choisissez d'aplatir tout le document ou uniquement les calques visibles (`flattenImage`) ou de fusionner des calques sélectionnés (`mergeLayers`).  
- **Performance :** Les fichiers plus petits se chargent plus rapidement et consomment moins de mémoire dans les processus en aval.  
- **Cross‑platform :** Fonctionne sur tout OS supportant Java.

## Prérequis

1. **Java Development Kit (JDK) :** JDK 8 ou plus récent installé.  
2. **Aspose.PSD for Java :** Téléchargez la bibliothèque depuis [here](https://releases.aspose.com/psd/java/).  
3. **IDE :** IntelliJ IDEA, Eclipse ou tout IDE compatible Java.  
4. **Connaissances de base en Java :** Utile mais pas obligatoire pour suivre les étapes.  
5. **PSD d'exemple :** Un fichier avec plusieurs calques (nous utiliserons `ThreeRegularLayersSemiTransparent.psd`).

Maintenant que tout est configuré, plongeons dans le code.

## Importer les packages

Pour commencer, importez les classes essentielles d'Aspose.PSD :

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

Ces imports nous permettent de charger des fichiers PSD, de travailler avec leurs calques et d'enregistrer les résultats.

## Étape 1 : Aplatir l'image PSD entière

Aplatir l'image entière est la façon la plus rapide de **réduire la taille du fichier PSD** car cela supprime toutes les données de calques individuelles.

### 1.1 Charger le fichier PSD

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ThreeRegularLayersSemiTransparent.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### 1.2 Aplatir l'image

```java
im.flattenImage();
```

### 1.3 Enregistrer l'image aplatie

```java
String exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattened.psd";
im.save(exportPath);
```

Votre nouveau fichier contient maintenant un seul calque d'arrière‑plan, ce qui entraîne généralement une taille PSD plus petite.

## Étape 2 : Fusionner des calques spécifiques (Comment aplatir le PSD sélectivement)

Parfois, vous ne souhaitez **aplatir que les calques visibles** ou combiner un sous‑ensemble de calques tout en laissant les autres modifiables.

### 2.1 Recharger le fichier PSD

```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

### 2.2 Identifier et sélectionner les calques

```java
Layer bottomLayer = img.getLayers()[0];
Layer middleLayer = img.getLayers()[1];
Layer topLayer = img.getLayers()[2];
```

### 2.3 Fusionner les calques

```java
Layer layer1 = img.mergeLayers(bottomLayer, middleLayer);
Layer layer2 = img.mergeLayers(layer1, topLayer);
```

### 2.4 Remplacer les calques existants par le calque fusionné

```java
img.setLayers(new Layer[]{layer2});
```

### 2.5 Enregistrer le fichier PSD mis à jour

```java
exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";
img.save(exportPath);
```

Le PSD ne contient maintenant que le calque fusionné, obtenant une taille de fichier réduite tout en conservant les calques que vous souhaitiez garder.

## Problèmes courants et astuces

- **Sauvegarde avant l'aplatissement :** Une fois les calques aplatis, l'opération ne peut pas être annulée. Conservez une copie du PSD original.  
- **La visibilité compte :** `flattenImage()` ne fusionne que les calques *visibles*. Masquez les calques que vous ne voulez pas inclure.  
- **Utilisation de la mémoire :** Les gros PSD peuvent consommer beaucoup de RAM ; envisagez de les traiter sur une machine disposant de suffisamment de mémoire.  
- **Modes de fusion :** La fusion respecte le mode de fusion de chaque calque, de sorte que le résultat visuel correspond à ce que vous verriez dans Photoshop.

## Questions fréquemment posées

**Q : Puis‑je annuler l'aplatissement des calques dans Aspose.PSD ?**  
R : Non, l'aplatissement est irréversible. Conservez toujours une sauvegarde du fichier original.

**Q : Est‑il possible d'aplatir uniquement les calques visibles ?**  
R : Oui. `flattenImage()` respecte la visibilité des calques, donc masquez les calques que vous ne voulez pas aplatir avant d'appeler la méthode.

**Q : L'aplatissement des calques réduit‑il la taille du fichier ?**  
R : Généralement, oui. La suppression des données de calque et des métadonnées conduit souvent à un PSD plus petit, bien que la réduction exacte dépende du contenu.

**Q : Puis‑je fusionner des calques avec des modes de fusion différents ?**  
R : Absolument. Aspose.PSD fusionne les calques tout en préservant l'apparence visuelle créée par leurs modes de fusion.

**Q : Que se passe‑t‑il si j'essaie de fusionner des calques non adjacents ?**  
R : Aspose.PSD permet de fusionner n'importe quels calques, quel que soit leur ordre dans la pile ; le résultat reflète l'apparence combinée.

---

**Dernière mise à jour :** 2026-04-03  
**Testé avec :** Aspose.PSD 24.11 for Java  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}