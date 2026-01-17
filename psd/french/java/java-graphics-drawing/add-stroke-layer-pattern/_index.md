---
date: 2026-01-17
description: Apprenez à ajouter un motif de contour en Java avec Aspose.PSD pour Java.
  Suivez ce guide étape par étape pour améliorer rapidement vos images PSD.
linktitle: How to Add Stroke Layer Pattern in Java
second_title: Aspose.PSD Java API
title: Comment ajouter un motif de trait Java avec Aspose.PSD
url: /fr/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment ajouter un motif de contour Java avec Aspose.PSD

## Introduction
If you need to **add stroke pattern java** to a Photoshop file, Aspose.PSD for Java makes it surprisingly simple. Whether you’re building a graphic‑design tool, automating batch edits, or just experimenting with layer effects, this tutorial walks you through every step—from loading the PSD to verifying the new pattern. Let’s dive in and see how quickly you can enhance your images.

## Réponses rapides
- **Quelle bibliothèque faut‑il ?** Aspose.PSD for Java  
- **Quelle version de Java est prise en charge ?** JDK 8 ou ultérieure  
- **Ai‑je besoin d’une licence pour les tests ?** Un essai gratuit suffit pour le développement ; une licence est requise pour la production  
- **Combien de temps prend l’implémentation ?** Environ 10‑15 minutes pour un contour de motif basique  
- **Puis‑je réutiliser le motif sur plusieurs calques ?** Oui, il suffit d’assigner le même `PattResource` aux autres calques  

## Qu’est‑ce que add stroke pattern java ?
Adding a stroke pattern in Java means applying a custom fill (often a repeating bitmap) to a layer’s stroke effect. This technique lets you create stylized outlines—think of a dashed line, a brick texture, or a custom graphic border—directly inside a PSD file without opening Photoshop.

## Pourquoi utiliser Aspose.PSD pour add stroke pattern java ?
- **Fidélité totale du PSD** – All layer effects, resources, and blending modes are preserved.  
- **Pas besoin de Photoshop natif** – Works on any OS with a JDK.  
- **Contrôle programmatique** – Automate batch processing or integrate into server‑side services.  
- **API riche** – Access to global resources, pattern fills, and blend modes in a single fluent interface.

## Prérequis
- **Java Development Kit (JDK)** – Ensure JDK 8 or newer is installed.  
- **Aspose.PSD for Java** – Download the library from [here](https://releases.aspose.com/psd/java/) and add the JAR to your project’s classpath.  
- **IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.

## Importer les packages
First, import the classes you’ll need for handling PSD files, colors, rectangles, and stroke effects.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```

## Étape 1 : Charger le fichier PSD
Load the source PSD so you can work with its layers and resources.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Étape 2 : Préparer les nouvelles données du motif
Create a simple 4 × 4 pixel pattern that will be used for the stroke.

```java
int[] newPattern = new int[]
{
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
};
Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
UUID guid = UUID.randomUUID();
```

## Étape 3 : Accéder à l’effet de contour
Locate the stroke effect on the target layer (in this example, the fourth layer).

```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```

## Étape 4 : Modifier l’effet de contour
### Mettre à jour les propriétés de l’effet de contour
Adjust opacity and blend mode to see the visual impact of the new pattern.

```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```

### Mettre à jour la ressource du motif
Replace the existing global pattern resource with the one you just created.

```java
PattResource resource;
for (int i = 0; i < im.getGlobalLayerResources().length; i++)
{
    if (im.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
        resource.setPattern(newPattern, newPatternBounds);
    }
}
```

## Étape 5 : Appliquer le nouveau motif
Bind the updated pattern resource to the stroke effect and save the PSD.

```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## Étape 6 : Vérifier les modifications
Reload the file and confirm that the new pattern, opacity, and blend mode are correctly applied.

```java
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
PattResource resource1 = null;
for (int i = 0; i < img.getGlobalLayerResources().length; i++)
{
    if (img.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource1 = (PattResource)img.getGlobalLayerResources()[i];
    }
}
try
{
    Assert.areEqual(newPattern, resource1.getPatternData());
    Assert.areEqual(newPatternBounds, new Rectangle(0, 0, resource1.getWidth(), resource1.getHeight()));
    Assert.areEqual(guid.toString(), resource1.getPatternId());
    Assert.areEqual(BlendMode.Color, patternStrokeEffect.getBlendMode());
    Assert.areEqual(127, patternStrokeEffect.getOpacity());
    Assert.areEqual(true, patternStrokeEffect.isVisible());
    PatternFillSettings fillSettings1 = (PatternFillSettings)patternStrokeEffect.getFillSettings();
    Assert.areEqual(FillType.Pattern, fillSettings1.getFillType());
}
catch (Exception e)
{
    System.out.println(e.getMessage());
}
```

## Problèmes courants et solutions
| Problème | Cause | Solution |
|----------|-------|----------|
| Le motif n’apparaît pas | Référence `PatternId` incorrecte | Assurez‑vous que le `PatternId` défini sur `PattResource` correspond à celui utilisé dans `PatternFillSettings`. |
| Le contour disparaît après l’enregistrement | Opacité réglée à 0 ou effet masqué | Vérifiez que `setOpacity` est compris entre 0‑255 et que `isVisible()` renvoie `true`. |
| Couleurs inattendues | Incohérence du mode de fusion | Utilisez `BlendMode.Color` (ou un autre mode) qui correspond à votre intention de conception. |

## FAQ
### Qu’est‑ce qu’Aspose.PSD pour Java ?
Aspose.PSD for Java is a library that allows developers to create, edit, and convert PSD (Photoshop Document) files programmatically.

### Puis‑je utiliser Aspose.PSD pour Java dans un projet commercial ?
Yes, you can use it in commercial projects. You can purchase a license from [here](https://purchase.aspose.com/buy).

### Existe‑t‑il un essai gratuit disponible pour Aspose.PSD pour Java ?
Yes, you can download a free trial version from [here](https://releases.aspose.com/).

### Comment obtenir du support pour Aspose.PSD pour Java ?
You can get support from the Aspose community forums [here](https://forum.aspose.com/c/psd/34).

### Quelles sont les exigences système pour Aspose.PSD pour Java ?
You need JDK installed and an IDE for development. The library supports multiple operating systems including Windows, Linux, and macOS.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-17  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose