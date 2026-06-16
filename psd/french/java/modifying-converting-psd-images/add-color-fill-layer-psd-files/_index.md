---
date: 2026-03-02
description: Apprenez comment ajouter un remplissage en créant un calque de remplissage
  de couleur dans les fichiers PSD à l’aide de Java et d’Aspose.PSD. Suivez notre
  guide étape par étape pour définir rapidement la couleur du calque de remplissage.
linktitle: Add Color Fill Layer to PSD Files using Java
second_title: Aspose.PSD Java API
title: 'Comment ajouter un remplissage : ajouter un calque de remplissage de couleur
  aux fichiers PSD avec Java'
url: /fr/java/modifying-converting-psd-images/add-color-fill-layer-psd-files/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajouter un calque de remplissage de couleur aux fichiers PSD avec Java

## Introduction
Vous êtes déjà tombé sur le besoin de manipuler des fichiers Photoshop de façon programmatique, peut‑être pour ajouter une touche de couleur à un design ? Si vous vous demandez **how to add fill** à un PSD, vous êtes au bon endroit. Dans ce tutoriel, nous allons parcourir les étapes pour ajouter un calque de remplissage de couleur à des fichiers PSD (Photoshop Document) en utilisant Java et la bibliothèque Aspose.PSD. Considérez votre PSD comme une toile numérique — à la fin, vous saurez créer un calque de remplissage de couleur, définir la couleur du calque de remplissage et enregistrer le fichier mis à jour en quelques lignes de code seulement.

## Quick Answers
- **What library is needed?** Aspose.PSD for Java  
- **Primary use case?** Programmatically add or change PSD fill colors  
- **How long does implementation take?** About 10‑15 minutes for a basic scenario  
- **Do I need a license?** A free trial works for evaluation; a commercial license is required for production  
- **Supported Java version?** Java 8 and above  

## What is a Color Fill Layer?
Un calque de remplissage de couleur est une superposition de couleur unie qui se situe au-dessus des autres calques dans un document Photoshop. Il est souvent utilisé pour ajouter une couleur d’arrière‑plan, créer des masques, ou changer rapidement le thème visuel d’un design sans modifier les pixels individuellement.

## Why add a color fill layer with code?
- **Automation :** Générer des actifs de marque cohérents à travers de nombreux fichiers.  
- **Batch processing :** Mettre à jour des dizaines de PSD en quelques secondes au lieu de le faire manuellement.  
- **Dynamic designs :** Modifier les couleurs à la volée en fonction des entrées utilisateur ou de sources de données.

## Prerequisites
Avant de plonger dans le code, assurons‑nous que vous avez tout le nécessaire :

1. **Java Development Kit (JDK)** – JDK 8 ou version plus récente installé.  
2. **Aspose.PSD Library** – Téléchargez le JAR le plus récent depuis la [Aspose Releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, NetBeans, ou tout éditeur de votre choix.  
4. **Basic Java knowledge** – Familiarité avec les objets, les boucles et la gestion des exceptions.

## Import Packages
Maintenant que les bases sont couvertes, importons les classes nécessaires. Ces imports nous donnent accès à la manipulation des PSD et des calques de remplissage.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IColorFillSettings;
```

## How to Add Fill – Step‑by‑Step Guide

### Step 1: Set Up Your Environment
Définissez où se trouve votre PSD source et où le fichier modifié sera enregistré, puis chargez le document.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ColorFillLayer.psd";
String exportPath     = dataDir + "ColorFillLayer_output.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- `dataDir` pointe vers le dossier contenant votre PSD.  
- `sourceFileName` est le fichier original que vous allez modifier.  
- `exportPath` est l’endroit où le nouveau fichier avec le **add color fill layer** sera écrit.  

### Step 2: Loop Through the Layers
Nous devons localiser les éventuels calques de remplissage existants afin de les modifier ou d’en créer un nouveau.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof FillLayer) {
        FillLayer fillLayer = (FillLayer) im.getLayers()[i];
```

- La boucle `for` parcourt chaque calque du PSD.  
- La vérification `instanceof FillLayer` garantit que nous ne travaillons qu’avec des calques de remplissage.

### Step 3: Verify the Fill Type
Assurez‑vous que le calque trouvé est un **color fill layer** avant d’essayer de changer sa couleur.

```java
if (fillLayer.getFillSettings().getFillType() != FillType.Color) {
    throw new Exception("Wrong Fill Layer");
}
```

Si le type de remplissage n’est pas `FillType.Color`, nous interrompons l’opération afin d’éviter de modifier accidentellement des remplissages en dégradé ou en motif.

### Step 4: Set the Fill Color
C’est ici que nous **set fill layer color**. L’exemple change le calque en rouge, mais vous pouvez remplacer `Color.getRed()` par n’importe quel autre `Color` dont vous avez besoin (par ex., `Color.getBlue()`, `new Color(255, 165, 0)` pour l’orange).

```java
IColorFillSettings settings = (IColorFillSettings) fillLayer.getFillSettings();
settings.setColor(Color.getRed());
fillLayer.update();
```

- `settings.setColor(...)` modifie réellement la couleur du remplissage.  
- `fillLayer.update()` rafraîchit le calque afin que la nouvelle couleur soit appliquée.  

### Step 5: Save the Changes
Enfin, écrivez le PSD modifié sur le disque.

```java
im.save(exportPath);
break;
```

- Le `break` arrête la boucle après la première mise à jour du calque de remplissage correspondant, ce qui est généralement ce que vous voulez lorsque vous devez **change PSD fill color** une seule fois.

## Common Issues & Tips
- **No FillLayer found :** Si votre PSD ne contient pas de calque de remplissage, vous devrez en créer un avec `new FillLayer(im)` et l’ajouter à `im.getLayers()`.  
- **Color not updating :** Assurez‑vous d’appeler `fillLayer.update()` après avoir défini la couleur.  
- **File not saved :** Vérifiez que `exportPath` pointe vers un répertoire accessible en écriture et que vous avez les permissions nécessaires.

## Frequently Asked Questions

**Q : What is Aspose.PSD ?**  
A : Aspose.PSD est une bibliothèque Java robuste qui vous permet de créer, modifier et convertir des fichiers Photoshop PSD sans avoir besoin d’Adobe Photoshop.

**Q : Can I use Aspose.PSD for free ?**  
A : Yes, a free trial is available on the [Aspose Releases page](https://releases.aspose.com/).  

**Q : Which file formats can I work with besides PSD ?**  
A : Aspose.PSD supports PSD, PSB, BMP, JPEG, PNG, GIF, TIFF, and more.

**Q : How do I get support if I run into problems ?**  
A : You can ask questions on the [Aspose Support Forum](https://forum.aspose.com/c/psd/34).  

**Q : Where can I purchase a full license ?**  
A : Licenses are sold through the [Aspose Purchase page](https://purchase.aspose.com/buy).

## Conclusion
Vous savez maintenant **how to add fill** à un document Photoshop de façon programmatique avec Java. En créant ou en localisant un calque de remplissage de couleur, en définissant sa couleur et en enregistrant le résultat, vous pouvez automatiser des tâches de design répétitives, générer des actifs dynamiques, ou intégrer la manipulation de PSD dans des applications Java plus larges. Essayez‑vous — expérimentez avec différentes couleurs, ajoutez plusieurs calques de remplissage, ou combinez cette technique avec d’autres fonctionnalités d’Aspose.PSD pour des pipelines de traitement d’image puissants.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-02  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

---