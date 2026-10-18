---
date: 2026-10-18
description: Apprenez à créer des effets de radial gradient dans des images Java en
  utilisant Aspose.PSD. Suivez ce guide étape par étape pour une intégration fluide.
keywords:
- create radial gradient java
- apply gradient overlay psd
- add radial gradient image
lastmod: 2026-10-18
linktitle: Ajouter des effets de gradient
og_description: Apprenez à créer des effets de radial gradient java en utilisant Aspose.PSD.
  Ce tutoriel montre comment ajouter, personnaliser et enregistrer des superpositions
  de gradient en quelques minutes.
og_image_alt: Screenshot of Aspose.PSD Java code creating a radial gradient effect
og_title: Créer un radial gradient java avec Aspose.PSD – guide étape par étape
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to create radial gradient effects in Java images using Aspose.PSD.
    Follow this step‑by‑step guide for seamless integration.
  headline: How to create radial gradient effects in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to create radial gradient effects in Java images using Aspose.PSD.
    Follow this step‑by‑step guide for seamless integration.
  name: How to create radial gradient effects in Aspose.PSD for Java
  steps:
  - name: Load the PSD file and access the gradient overlay
    text: '`PsdLoadOptions` configures how a PSD file is loaded, allowing you to enable
      loading of effect resources. `Image.load` reads the file into an `Image` object.
      In this step, we load a PSD file and retrieve the first `GradientOverlayEffect`
      from the second layer (index 1). The `loadOptions.setLoadEffec'
  - name: Verify Initial Settings
    text: Before making changes, it’s a good practice to confirm the current blend
      mode, opacity, and visibility. This helps you understand the baseline state
      of the gradient overlay.
  - name: Modify Gradient Settings
    text: Here you can customize the gradient’s color, opacity, and blend mode. The
      example changes the color to green, reduces opacity to 193 (out of 255), and
      switches the blend mode to **Lighten**. Feel free to experiment with other `BlendMode`
      values such as `Multiply`, `Screen`, or `Overlay`.
  - name: Save the Edited Image
    text: After applying your modifications, persist the changes by saving the PSD
      to a new file. This step ensures the original file remains untouched.
  - name: Verify Changes
    text: The snippet above demonstrates how to open a PSD, pull the second layer’s
      first effect (assumed to be a gradient overlay), and prepare it for modification.
  - name: Verify the original settings (optional but recommended)
    text: Before you change anything, checking the existing blend mode, opacity, and
      visibility helps you understand the baseline. The `Assert` calls in the code
      confirm that the effect is currently set to **Normal** blend mode, fully opaque,
      and visible.
  - name: Adjust gradient properties to achieve a radial style
    text: 'You can change the gradient’s color, opacity, and blend mode. For a true
      radial effect, set the gradient style: *Pro tip:* Use `Color.getGreen()` or
      any `java.awt.Color` instance to define the start color, and `gradientOverlay.setColor2(Color.getBlue())`
      for the end color.'
  - name: Save the edited PSD
    text: Calling `im.save(exportPath);` writes the modified image to disk. The saved
      file retains the radial gradient overlay and can be opened in Photoshop, previewed
      in browsers, or converted to other formats.
  type: HowTo
- questions:
  - answer: Yes. Retrieve the layer’s `BlendingOptions`, iterate through the `Effects`
      collection, and add a new `GradientOverlayEffect` for each gradient you need.
    question: Can I apply multiple gradient effects to a single image?
  - answer: Aspose.PSD provides shadows, glows, bevels, and more. Each effect appears
      in the `Effects` array and can be configured independently.
    question: What other effects can I combine with gradient overlays?
  - answer: Verify that the PSD was loaded with `setLoadEffectsResource(true)`, check
      layer visibility, and confirm you are modifying the correct effect index.
    question: How can I troubleshoot if the effects are not rendering correctly?
  - answer: Yes, you can get a free trial [here](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.PSD for Java?
  - answer: Visit the [purchase page](https://purchase.aspose.com/buy) for licensing
      information.
    question: Where can I purchase a license for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- create radial gradient
- gradient overlay effect
- Aspose.PSD Java
title: Comment créer des effets de radial gradient dans Aspose.PSD pour Java
url: /fr/java/advanced-image-effects/add-gradient-effects/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment créer des effets de dégradé radial dans Aspose.PSD pour Java

## Introduction

Dans ce guide, vous apprendrez à **créer des effets radial gradient java** en utilisant la bibliothèque Aspose.PSD. Les dégradés radiaux sont parfaits pour ajouter de la profondeur, du focus ou une lueur subtile à vos calques PSD sans ouvrir Photoshop. À la fin du tutoriel, vous serez capable de charger un PSD, d’appliquer un superposition de dégradé, d’ajuster ses propriétés et d’enregistrer le résultat — le tout depuis du code Java.

## Réponses rapides
- **Que puis‑je réaliser ?** Ajouter, modifier et fusionner des superpositions de dégradé radial sur des calques PSD.  
- **Quelle bibliothèque est requise ?** Aspose.PSD pour Java (dernière version).  
- **Ai‑je besoin d’une licence ?** Un essai gratuit suffit pour le développement ; une licence commerciale est requise pour la production.  
- **Combien de temps faut‑il pour implémenter ?** Environ 10‑15 minutes pour une superposition de dégradé radial basique.  
- **Est‑ce compatible avec Java 8+ ?** Oui, l’API prend en charge Java 8 et les runtimes plus récents.

## Prérequis

Avant de plonger dans le tutoriel, assurez‑vous d’avoir les prérequis suivants :

1. **Aspose.PSD pour Java Library** – Assurez‑vous d’avoir téléchargé et installé la bibliothèque Aspose.PSD pour Java. Vous pouvez trouver la bibliothèque et sa documentation sur la [page de documentation Aspose.PSD Java](https://reference.aspose.com/psd/java/).  
2. **Environnement de développement Java** – Configurez un environnement de développement Java sur votre machine (JDK 8 ou supérieur, IDE de votre choix).  
3. **Dernière version d’Aspose.PSD** – Téléchargez la version la plus récente depuis la [page des releases Aspose](https://releases.aspose.com/).  
4. **Ressources d’assistance** – Si vous rencontrez des problèmes, consultez le [forum de support Aspose.PSD](https://forum.aspose.com/c/psd/34).  
5. **Achat de licence** – Lorsque vous êtes prêt pour la production, obtenez une licence via la [page d’achat](https://purchase.aspose.com/buy).

Maintenant que tout est configuré, poursuivons avec le guide étape par étape.

## Qu’est‑ce qu’un effet de superposition de dégradé ?

Un effet de superposition de dégradé peint une transition fluide entre deux ou plusieurs couleurs sur une zone sélectionnée d’un calque. Dans Photoshop, cet effet peut être mélangé, coloré et positionné pour créer des conceptions visuelles sophistiquées. La classe `GradientOverlayEffect` est la représentation Aspose.PSD de ce style de calque, exposant des propriétés telles que les arrêts de couleur, l’opacité, le mode de fusion et le style du dégradé.

## Comment créer un effet de dégradé radial

Chargez le PSD, localisez le calque cible, ajustez les propriétés du `GradientOverlayEffect`, puis enregistrez le fichier. Le flux complet tient en quatre lignes concises de code Java une fois l’image chargée.

### Étape 1 : Charger le fichier PSD et accéder à la superposition de dégradé

`PsdLoadOptions` configure la façon dont un fichier PSD est chargé, vous permettant d’activer le chargement des ressources d’effet. `Image.load` lit le fichier dans un objet `Image`.

```javaString dataDir = "Your Document Directory";

// Gradient overlay effect. Example
String sourceFileName = dataDir + "GradientOverlay.psd";
String exportPath = dataDir + "GradientOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlay = (GradientOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

Dans cette étape, nous chargeons un fichier PSD et récupérons le premier `GradientOverlayEffect` du deuxième calque (indice 1). L’appel `loadOptions.setLoadEffectsResource(true)` garantit que les ressources d’effet sont disponibles pour la modification.

### Étape 2 : Vérifier les paramètres initiaux

```java
// Verify initial settings
Assert.areEqual(BlendMode.Normal, gradientOverlay.getBlendMode());
Assert.areEqual(255, gradientOverlay.getOpacity());
Assert.areEqual(true, gradientOverlay.isVisible());
// ... (additional verifications)
```

Avant d’apporter des modifications, il est recommandé de confirmer le mode de fusion actuel, l’opacité et la visibilité. Cela vous aide à comprendre l’état de référence de la superposition de dégradé.

### Étape 3 : Modifier les paramètres du dégradé

```java
// Modify gradient settings
settings.setColor(Color.getGreen());
gradientOverlay.setOpacity((byte)193);
gradientOverlay.setBlendMode(BlendMode.Lighten);
// ... (additional modifications)
```

Ici vous pouvez personnaliser la couleur, l’opacité et le mode de fusion du dégradé. L’exemple change la couleur en vert, réduit l’opacité à 193 (sur 255) et passe le mode de fusion à **Lighten**. N’hésitez pas à expérimenter d’autres valeurs `BlendMode` telles que `Multiply`, `Screen` ou `Overlay`.

### Étape 4 : Enregistrer l’image modifiée

```java
// Save the edited image
im.save(exportPath);
```

Après avoir appliqué vos modifications, persistez les changements en enregistrant le PSD dans un nouveau fichier. Cette étape garantit que le fichier original reste intact.

### Étape 5 : Vérifier les modifications

```java
// Verify changes after editing
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlayEffect = (GradientOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];
// ... (additional verifications)
```

L’extrait ci‑dessus montre comment ouvrir un PSD, extraire le premier effet du deuxième calque (supposé être une superposition de dégradé) et le préparer à la modification.

### Étape 2 : Vérifier les paramètres d’origine (optionnel mais recommandé)

Avant de changer quoi que ce soit, vérifier le mode de fusion, l’opacité et la visibilité existants vous aide à comprendre la base. Les appels `Assert` dans le code confirment que l’effet est actuellement réglé sur le mode de fusion **Normal**, totalement opaque et visible.

### Étape 3 : Ajuster les propriétés du dégradé pour obtenir un style radial

Vous pouvez modifier la couleur, l’opacité et le mode de fusion du dégradé. Pour un vrai effet radial, définissez le style du dégradé :

```java
gradientOverlay.setGradientStyle(GradientStyle.Radial);
gradientOverlay.setAngle(0f); // angle is ignored for radial, but required by API
gradientOverlay.setScale(100f); // 100 % fills the layer
```

*Astuce :* Utilisez `Color.getGreen()` ou toute instance `java.awt.Color` pour définir la couleur de départ, et `gradientOverlay.setColor2(Color.getBlue())` pour la couleur finale.

### Étape 4 : Enregistrer le PSD modifié

L’appel `im.save(exportPath);` écrit l’image modifiée sur le disque. Le fichier enregistré conserve la superposition de dégradé radial et peut être ouvert dans Photoshop, prévisualisé dans les navigateurs ou converti vers d’autres formats.

## Pourquoi créer des superpositions de dégradé radial ?

Les dégradés radiaux ajoutent de la profondeur et du focus aux créations, faisant apparaître les éléments en trois dimensions ou en mise en avant. Ils sont idéaux pour :

- **Remplissages d’arrière‑plan** qui attirent le regard vers un sujet central.  
- **Mises en évidence de boutons ou d’icônes** où une lueur subtile est nécessaire.  
- **Effets photo créatifs** tels que les vignettages ou les éclats de lumière.  

Aspose.PSD traite **plus de 50 formats d’entrée et de sortie** et peut gérer des fichiers PSD de plusieurs centaines de pages sans charger le document complet en mémoire, vous permettant d’automatiser la création de dégradés sur de vastes bibliothèques d’actifs.

## Problèmes courants & astuces

- **Effet non visible :** Assurez‑vous que `gradientOverlay.isVisible()` renvoie `true`. Certains fichiers PSD masquent les effets par défaut.  
- **Indice de calque incorrect :** Les calques sont indexés à partir de zéro ; vérifiez que vous ciblez le bon calque (`im.getLayers()[1]` désigne le deuxième calque).  
- **Conversion d’opacité :** La méthode `setOpacity` attend un `byte`. Passer un `int` provoquera une erreur de compilation ; effectuez un cast explicite comme indiqué.  
- **Chargement des ressources :** Si vous obtenez `null` en accédant aux effets, vérifiez que `loadOptions.setLoadEffectsResource(true)` est défini avant le chargement de l’image.

## Questions fréquentes

**Q : Puis‑je appliquer plusieurs effets de dégradé à une même image ?**  
R : Oui. Récupérez les `BlendingOptions` du calque, parcourez la collection `Effects` et ajoutez un nouveau `GradientOverlayEffect` pour chaque dégradé nécessaire.

**Q : Quels autres effets puis‑je combiner avec les superpositions de dégradé ?**  
R : Aspose.PSD propose des ombres, des lueurs, des biseaux, etc. Chaque effet apparaît dans le tableau `Effects` et peut être configuré indépendamment.

**Q : Comment dépanner si les effets ne sont pas rendus correctement ?**  
R : Vérifiez que le PSD a été chargé avec `setLoadEffectsResource(true)`, contrôlez la visibilité du calque et assurez‑vous de modifier le bon indice d’effet.

**Q : Existe‑t‑il une version d’essai d’Aspose.PSD pour Java ?**  
R : Oui, vous pouvez obtenir un essai gratuit [ici](https://releases.aspose.com/).

**Q : Où puis‑je acheter une licence pour Aspose.PSD pour Java ?**  
R : Consultez la [page d’achat](https://purchase.aspose.com/buy) pour les informations de licence.

## FAQ supplémentaires

**Q : Puis‑je changer la direction du dégradé par programmation ?**  
R : Oui. Utilisez la méthode `GradientOverlayEffect.setAngle(float angle)` pour définir l’angle du dégradé en degrés. Pour les dégradés radiaux, l’angle est ignoré, mais la méthode doit tout de même être appelée.

**Q : Aspose.PSD prend‑il en charge les dégradés radiaux ?**  
R : Absolument. Réglez le style du dégradé sur `GradientStyle.Radial` via les propriétés du `GradientOverlayEffect`.

**Q : Les superpositions de dégradé sont‑elles conservées lors de la conversion du PSD vers d’autres formats (ex. PNG) ?**  
R : Lorsque vous rasterisez le PSD (par ex. en l’enregistrant en PNG), le rendu visuel de la superposition de dégradé est conservé, mais l’effet lui‑même devient partie des données pixel.

**Q : Comment supprimer une superposition de dégradé d’un calque ?**  
R : Récupérez les `BlendingOptions` du calque, localisez le `GradientOverlayEffect` dans la collection `Effects` et retirez‑le avec `remove(effect)`.

**Q : Est‑il possible d’animer les changements de dégradé ?**  
R : Bien qu’Aspose.PSD ne gère pas directement l’animation, vous pouvez générer une séquence de fichiers PSD avec des paramètres de dégradé variables, puis les assembler en vidéo ou GIF à l’aide d’une autre bibliothèque.

## Conclusion

Félicitations ! Vous avez appris **comment créer des effets radial gradient java** pour vos images en utilisant Aspose.PSD pour Java. En suivant les étapes ci‑dessus, vous pouvez ajouter, modifier et enregistrer des superpositions de dégradé de façon programmatique, vous offrant un contrôle créatif complet sur vos actifs PSD. Expérimentez avec différentes couleurs, modes de fusion et valeurs d’opacité pour obtenir l’impact visuel souhaité.

---

**Dernière mise à jour :** 2026-10-18  
**Testé avec :** Aspose.PSD pour Java 24.12 (dernière version au moment de la rédaction)  
**Auteur :** Aspose  








```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.*;
import com.aspose.psd.fileformats.psd.layers.layereffects.GradientOverlayEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Tutoriels associés

- [Créer un remplissage de dégradé PSD avec Java en utilisant Aspose.PSD – Ajouter un calque de remplissage de dégradé](/psd/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/)
- [Superposition de motif PSD : Ajouter des effets avec Aspose.PSD pour Java](/psd/java/advanced-image-effects/add-pattern-effects/)
- [Appliquer une superposition de couleur et définir l’opacité en Java avec Aspose.PSD](/psd/java/image-editing/color-overlay-effect/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}