---
date: 2025-12-30
description: Apprenez à modifier la couleur de l’ombre et à personnaliser les effets
  d’ombre avec Aspose.PSD pour Java. Suivez ce tutoriel pas à pas sur les effets d’ombre.
linktitle: Support Shadow Effect
second_title: Aspose.PSD Java API
title: Comment changer la couleur de l'ombre avec Aspose.PSD pour Java
url: /fr/java/basic-image-operations/support-shadow-effect/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Modifier la couleur de l'ombre avec Aspose.PSD pour Java

## Introduction

Ajouter de la profondeur à vos graphiques signifie souvent **modifier la couleur de l'ombre** pour correspondre à l'ambiance du design. Avec Aspose.PSD pour Java, vous pouvez facilement ajouter ou modifier les effets d'ombre portée, contrôler l'opacité et ajuster finement d'autres paramètres — le tout depuis le code Java. Dans ce **tutoriel sur les effets d'ombre**, nous allons charger un PSD, lire l'ombre existante, personnaliser sa couleur, son opacité, sa distance, puis enregistrer le fichier mis à jour.

## Réponses rapides
- **What does “change shadow color” mean?** It updates the color property of a DropShadowEffect applied to a PSD layer.  
- **Which library supports this?** Aspose.PSD for Java provides full support for shadow effects.  
- **Do I need a license?** A trial works for development; a commercial license is required for production.  
- **Can I set shadow opacity?** Yes – use `setOpacity(byte)` to define transparency (0‑255).  
- **Is the code compatible with Java 8+?** Absolutely, the API targets Java 8 and later.

## Qu'est-ce que « modifier la couleur de l'ombre » dans les fichiers PSD ?

Modifier la couleur de l'ombre change la teinte visuelle de l'ombre portée qui apparaît derrière un calque. Cela est utile pour créer un éclairage réaliste, assortir les couleurs de la marque ou simplement ajouter une touche artistique.

## Pourquoi utiliser Aspose.PSD pour Java afin de personnaliser les effets d'ombre ?

- **Full PSD fidelity** – all layer effects, including shadows, are preserved.  
- **No Photoshop required** – manipulate files programmatically on any server.  
- **Fine‑grained control** – adjust color, opacity, distance, angle, spread, and noise.  
- **Cross‑platform** – works on Windows, Linux, and macOS JVMs.

## Prérequis

- Connaissances de base en programmation Java.  
- Aspose.PSD pour Java installé. Vous pouvez le télécharger [ici](https://releases.aspose.com/psd/java/).  

## Importer les packages

Before you start, import the required classes so you can work with images and shadow effects:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Guide étape par étape

### Étape 1 : Charger l'image PSD

First, load the source PSD while enabling the loading of effect resources:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Shadow.psd";
String psdPathAfterChange = dataDir + "ShadowChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### Étape 2 : Récupérer l'effet d'ombre portée existant

Locate the shadow effect on the desired layer (in this example, the second layer):

```java
DropShadowEffect shadowEffect = (DropShadowEffect)(im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Étape 3 : Vérifier les paramètres par défaut (facultatif)

Running these assertions helps you understand the original values before you modify them:

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

### Étape 4 : **Modifier la couleur de l'ombre** et personnaliser les autres propriétés

Now we actually **change shadow color** to green, adjust opacity, distance, size, and other attributes. This demonstrates the **customize shadow effect** capabilities of Aspose.PSD:

```java
shadowEffect.setColor(Color.getGreen());          // change shadow color
shadowEffect.setOpacity((byte)128);               // set shadow opacity (50% transparent)
shadowEffect.setDistance(11);                     // move shadow farther from the object
shadowEffect.setUseGlobalLight(false);            // use local lighting
shadowEffect.setSize(9);                          // adjust blur radius
shadowEffect.setAngle(45);                        // rotate light source
shadowEffect.setSpread(3);                        // increase spread
shadowEffect.setNoise(50);                        // add texture noise
```

### Étape 5 : Enregistrer l'image modifiée

Finally, write the updated PSD back to disk:

```java
im.save(psdPathAfterChange);
```

## Problèmes courants et astuces

- **NullPointerException when retrieving effects** – ensure `setLoadEffectsResource(true)` is called; otherwise effects are not loaded.  
- **Color not changing** – verify you are editing the correct layer index (`im.getLayers()[1]` in this example).  
- **Opacity looks unchanged** – remember opacity is a byte (0‑255). Casting to `(byte)` is required.  

## Conclusion

By following these steps you can **change shadow color**, **set shadow opacity**, and fully **customize shadow effect** parameters in any PSD file using Aspose.PSD for Java. This empowers you to create richer graphics programmatically without manual Photoshop work.

## Questions fréquemment posées

**Q: Is Aspose.PSD for Java suitable for professional graphic design projects?**  
A: Absolutely! Aspose.PSD for Java is a powerful library designed for professional graphic design tasks.

**Q: Can I use Aspose.PSD for Java in commercial applications?**  
A: Yes, Aspose.PSD for Java is a commercial product. You can purchase it [here](https://purchase.aspose.com/buy).

**Q: Is there a free trial available?**  
A: Yes, you can explore a free trial version [here](https://releases.aspose.com/).

**Q: Where can I find detailed documentation?**  
A: Refer to the comprehensive documentation [here](https://reference.aspose.com/psd/java/).

**Q: How can I get support for Aspose.PSD for Java?**  
A: Join the community forum [here](https://forum.aspose.com/c/psd/34) for any support queries.

---

**Dernière mise à jour :** 2025-12-30  
**Testé avec :** Aspose.PSD for Java 24.10  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}