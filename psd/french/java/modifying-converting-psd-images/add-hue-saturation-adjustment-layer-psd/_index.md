---
date: 2026-03-13
description: Apprenez comment ajouter un calque de teinte et saturation aux fichiers
  PSD en utilisant Aspose.PSD pour Java. Ce guide montre également comment traiter
  en lot les fichiers PSD et créer un calque d’ajustement de teinte de manière programmatique.
linktitle: Add Hue Saturation Layer to PSD
second_title: Aspose.PSD Java API
title: Ajouter un calque de teinte et saturation au PSD avec Aspose.PSD pour Java
url: /fr/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
weight: 14
---

 Solutions
Translate bullet points.

## Frequently Asked Questions
Translate Q&A.

## Conclusion
Translate.

Then closing shortcodes.

Then backtop button shortcode.

Then the horizontal rule and metadata lines: translate "Last Updated", "Tested With", "Author". Keep dates same.

Ok produce final.

Be careful to preserve markdown formatting.

Let's craft French translation.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajouter une couche Hue Saturation à un PSD

## Introduction
En conception graphique, la manipulation des couleurs joue un rôle essentiel — notamment, ajuster la teinte, la saturation et la luminosité peut transformer radicalement l’ambiance et la qualité d’une image. Une façon efficace d’y parvenir est d’utiliser les calques de réglage dans Photoshop (fichiers PSD). Si vous souhaitez **ajouter une couche de teinte saturation** de façon programmatique avec Java, la bibliothèque Aspose.PSD est là pour vous aider ! Ce tutoriel vous guidera à travers les étapes pour ajouter un calque de réglage Hue Saturation à vos fichiers PSD, rendant votre flux de travail plus productif et efficace.

## Quick Answers
- **Quelle bibliothèque permet d’ajouter une couche hue saturation en Java ?** Aspose.PSD for Java.  
- **Dois‑je installer Photoshop ?** Non, la bibliothèque fonctionne indépendamment de Photoshop.  
- **Puis‑je traiter plusieurs fichiers PSD en lot avec cette approche ?** Oui — une fois les étapes automatisées, vous pouvez les appliquer à de nombreux fichiers.  
- **Quelle version de Java est requise ?** JDK 8 ou supérieur.  
- **Une licence est‑elle nécessaire pour la production ?** Oui, une licence commerciale est requise après la période d’essai.

## What is an “add hue saturation layer” operation?
Une opération **add hue saturation layer** crée un calque de réglage non destructif qui vous permet de modifier les valeurs de teinte, saturation et luminosité sans altérer les données de pixels d’origine. Cela est idéal pour affiner les couleurs sur l’ensemble d’une composition ou sur des plages de couleurs spécifiques.

## Why use Aspose.PSD for Java?
- **Pas de dépendance à Photoshop** – fonctionne sur n’importe quelle plateforme exécutant Java.  
- **Fidélité totale au PSD** – préserve toutes les informations de calques, masques et effets.  
- **Prêt pour le traitement par lots** – vous pouvez parcourir des dossiers et appliquer le même réglage à des dizaines de fichiers.  
- **Optimisé pour la performance** – conçu pour les documents volumineux et l’automatisation côté serveur.

## Prerequisites
Avant de plonger dans le code, assurez‑vous d’avoir les éléments suivants :

1. **Java Development Kit (JDK) :** Vérifiez que vous avez le JDK 8 ou supérieur installé sur votre machine. Vous pouvez le télécharger depuis les [Java SE Development Kit Downloads](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD for Java Library :** Vous devez disposer de la bibliothèque Aspose.PSD, que vous pouvez [download here](https://releases.aspose.com/psd/java/).  
3. **IDE :** Un environnement de développement intégré (IDE) tel qu’IntelliJ IDEA ou Eclipse pour le développement Java.  
4. **Connaissances de base en Java :** Une familiarité avec la programmation Java est un plus, mais ne vous inquiétez pas — nous passerons en revue chaque ligne.

Maintenant que nos prérequis sont en place, passons à la partie amusante — le codage !

## Import Packages
Pour commencer à travailler avec la bibliothèque Aspose.PSD, la première étape consiste à importer les classes nécessaires. Voici comment le faire dans votre fichier Java :

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```

Assurez‑vous que les bibliothèques appropriées sont ajoutées à votre projet afin que ces imports fonctionnent sans problème.

## Step 1: Set Up Your Document Directory
Chaque projet a besoin d’un point de départ, et le nôtre ne fait pas exception. Vous devez spécifier le répertoire où vos fichiers PSD sont stockés. Cela est crucial pour charger et enregistrer correctement les images.

```java
String dataDir = "Your Document Directory"; // Update this path to your actual directory
```

## Step 2: Load an Existing PSD File
Pour manipuler un fichier PSD existant, nous devons d’abord le charger dans notre programme. Voici comment procéder :

```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

Dans ce code, remplacez `"HueSaturationAdjustmentLayer.psd"` par le nom de votre fichier PSD existant que vous souhaitez modifier.

## Step 3: Edit the Hue/Saturation Layer
Ensuite, nous parcourrons les calques de l’image PSD chargée afin de trouver et modifier les calques Hue/Saturation existants. Cette étape implique la modification des valeurs de teinte, saturation et luminosité.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof HueSaturationLayer) {
        HueSaturationLayer hueLayer = (HueSaturationLayer) im.getLayers()[i];
        hueLayer.setHue((short) -25);
        hueLayer.setSaturation((short) -12);
        hueLayer.setLightness((short) 67);
        ColorRangeHsl colorRange = hueLayer.getRange(2);
        colorRange.setHue((short) -40);
        colorRange.setSaturation((short) 50);
        colorRange.setLightness((short) -20);
        colorRange.setMostLeftBorder((short) 300);
    }
}
```

Dans cet exemple :  
- Nous réglons la teinte à **-25**, la saturation à **-12** et la luminosité à **+67**.  
- La méthode `getRange(2)` nous permet d’ajuster des plages de couleurs spécifiques selon les besoins.

## Step 4: Save the Modified PSD File
Après les ajustements, l’étape suivante consiste à enregistrer le fichier. C’est une partie vitale du processus, garantissant que les modifications ne soient pas perdues.

```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```

## Step 5: Add a New Hue/Saturation Layer
Si vous devez **créer un calque de réglage hue** à partir de zéro, vous pouvez ajouter un tout nouveau calque Hue/Saturation à un autre fichier PSD. Suivez le même schéma de chargement mais utilisez la méthode `addHueSaturationAdjustmentLayer()`.

```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```

## Step 6: Set New Hue/Saturation Values for the New Layer
Une fois ce nouveau calque créé, appliquez les réglages de teinte, saturation et luminosité souhaités comme précédemment.

```java
hueLayerNew.setHue((short) -25);
hueLayerNew.setSaturation((short) -12);
hueLayerNew.setLightness((short) 67);
ColorRangeHsl newColorRange = hueLayerNew.getRange(2);
newColorRange.setHue((short) -160);
newColorRange.setSaturation((short) 100);
newColorRange.setLightness((short) 20);
newColorRange.setMostLeftBorder((short) 300);
```

## Step 7: Save the Updated PSD File
Enfin, enregistrez le fichier PSD avec le calque Hue/Saturation ajouté afin de visualiser vos changements.

```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```

Félicitations ! Vous avez manipulé avec succès des fichiers PSD en utilisant Aspose.PSD for Java. Vous pouvez maintenant expérimenter avec différentes images et des altérations plus poussées, donnant vie à vos projets de conception graphique.

## How to batch process PSD files with hue adjustments
Comme le code ci‑dessus est entièrement scriptable, vous pouvez envelopper toute la séquence dans une boucle qui itère sur chaque fichier `.psd` d’un dossier. Cela vous permet de **traiter des fichiers psd en lot** et d’appliquer les mêmes ajustements de teinte, saturation et luminosité en une seule exécution — parfait pour des mises à jour de marque à grande échelle.

## Common Issues and Solutions
- **NullPointerException lors du chargement d’un fichier :** Vérifiez que `dataDir` se termine par le séparateur de fichiers approprié (`/` ou `\`) et que le nom du fichier est correct.  
- **Valeurs de réglage hors limites :** La teinte, la saturation et la luminosité acceptent des valeurs de -255 à 255. Gardez vos nombres dans cette plage.  
- **Calque introuvable :** Si le PSD ne possède pas de calque Hue/Saturation, le test `instanceof` sautera le bloc. Utilisez `addHueSaturationAdjustmentLayer()` pour en créer un d’abord.

## Frequently Asked Questions

**Q : Qu’est‑ce qu’un calque de réglage Hue Saturation ?**  
R : Il vous permet de modifier les propriétés de couleur d’une image sans altérer de façon permanente les pixels d’origine.

**Q : Dois‑je installer Photoshop pour utiliser Aspose.PSD ?**  
R : Non, Aspose.PSD est une bibliothèque autonome qui fonctionne indépendamment de Photoshop.

**Q : Puis‑je utiliser Aspose.PSD pour le traitement par lots ?**  
R : Oui, vous pouvez automatiser et traiter en lot plusieurs fichiers PSD avec Aspose.PSD.

**Q : Aspose.PSD est‑il gratuit ?**  
R : Aspose.PSD propose une version d’essai gratuite, mais une licence est requise pour une utilisation à long terme. Vous pouvez consulter les tarifs [here](https://purchase.aspose.com/buy).

## Conclusion
Travailler avec des graphiques de façon programmatique ouvre un monde de possibilités. Utiliser Aspose.PSD for Java pour **add hue saturation layer** et pour **create hue adjustment layer** offre la flexibilité et l’efficacité qui peuvent rationaliser votre flux de travail de conception. Que vous amélioriez des photos pour un projet ou que vous créiez du contenu visuel époustouflant, maîtriser ces outils peut grandement améliorer votre production.

N’hésitez pas à explorer davantage les fonctionnalités d’Aspose.PSD en consultant la [documentation](https://reference.aspose.com/psd/java/) ou à envisager une [temporary license](https://purchase.aspose.com/temporary-license/) pour tester toute la puissance de la bibliothèque.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Dernière mise à jour :** 2026-03-13  
**Testé avec :** Aspose.PSD for Java 24.12 (dernière version au moment de la rédaction)  
**Auteur :** Aspose