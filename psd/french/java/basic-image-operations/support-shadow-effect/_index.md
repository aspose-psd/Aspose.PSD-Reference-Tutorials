---
date: 2026-06-18
description: Apprenez comment modifier la couleur de l'ombre en Java et personnaliser
  les effets d'ombre à l'aide d'Aspose.PSD for Java. Suivez ce tutoriel étape par
  étape sur les effets d'ombre.
keywords:
- change shadow color java
- Aspose.PSD shadow effect
- Java PSD manipulation
linktitle: Support de l'effet d'ombre
schemas:
- author: Aspose
  dateModified: '2026-06-18'
  description: Learn how to change shadow color java and customize shadow effects
    using Asprose.PSD for Java. Follow this step‑by‑step shadow effect tutorial.
  headline: Change Shadow Color Java with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to change shadow color java and customize shadow effects
    using Asprose.PSD for Java. Follow this step‑by‑step shadow effect tutorial.
  name: Change Shadow Color Java with Aspose.PSD for Java
  steps:
  - name: Load the PSD Image
    text: 'First, load the source PSD while enabling the loading of effect resources:'
  - name: Retrieve the Existing Drop Shadow Effect
    text: 'Locate the shadow effect on the desired layer (in this example, the second
      layer):'
  - name: Verify the Default Settings (Optional)
    text: 'Running these assertions helps you understand the original values before
      you modify them:'
  - name: '**Change Shadow Color** and Customize Other Properties'
    text: Now we actually **change shadow color** to green, adjust opacity, distance,
      size, and other attributes. This demonstrates the **customize shadow effect**
      capabilities of Aspose.PSD. The `setOpacity(byte)` method sets the shadow's
      opacity level (0‑255).
  - name: Save the Modified Image
    text: 'Finally, write the updated PSD back to disk using the `save` method of
      `PsdImage`:'
  type: HowTo
- questions:
  - answer: Absolutely! Aspose.PSD for Java is a powerful library designed for professional
      graphic design tasks.
    question: Is Aspose.PSD for Java suitable for professional graphic design projects?
  - answer: Yes, Aspose.PSD for Java is a commercial product. You can purchase it
      [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for Java in commercial applications?
  - answer: Yes, you can explore a free trial version [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Refer to the comprehensive documentation [here](https://reference.aspose.com/psd/java/).
    question: Where can I find detailed documentation?
  - answer: Join the community forum [here](https://forum.aspose.com/c/psd/34) for
      any support queries.
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Modifier la couleur de l'ombre en Java avec Aspose.PSD for Java
url: /fr/java/basic-image-operations/support-shadow-effect/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Modifier la couleur de l'ombre Java avec Aspose.PSD pour Java

## Introduction

Ajouter de la profondeur à vos graphiques signifie souvent **modifier la couleur de l'ombre** pour correspondre à l'ambiance du design. Avec Aspose.PSD pour Java, vous pouvez facilement ajouter ou modifier des effets d'ombre portée, contrôler l'opacité et ajuster finement d'autres paramètres — le tout depuis du code Java. Dans ce **tutoriel sur les effets d'ombre**, nous allons charger un PSD, lire l'ombre existante, personnaliser sa couleur, son opacité, sa distance, puis enregistrer le fichier mis à jour. Ce guide montre exactement comment **modifier la couleur de l'ombre java** de manière reproductible.

## Réponses rapides
- **Que signifie « modifier la couleur de l'ombre » ?** Cela met à jour la propriété de couleur d'un DropShadowEffect appliqué à un calque PSD.  
- **Quelle bibliothèque prend‑en charge cela ?** Aspose.PSD pour Java offre une prise en charge complète des effets d'ombre.  
- **Ai‑je besoin d’une licence ?** Une version d'essai fonctionne pour le développement ; une licence commerciale est requise pour la production.  
- **Puis‑je définir l'opacité de l'ombre ?** Oui – utilisez `setOpacity(byte)` pour définir la transparence (0‑255).  
- **Le code est‑il compatible avec Java 8+ ?** Absolument, l'API cible Java 8 et versions ultérieures.

## Qu’est‑ce que « modifier la couleur de l'ombre » dans les fichiers PSD ?

Modifier la couleur de l'ombre change la teinte visuelle de l'ombre portée qui apparaît derrière un calque. Cet ajustement permet aux concepteurs de simuler différentes conditions d'éclairage, d'aligner les ombres avec les palettes de couleurs de la marque et d'ajouter une touche artistique aux compositions. En modifiant la teinte, vous pouvez rendre les ombres plus chaudes, plus froides, ou les faire correspondre exactement à un schéma de couleurs spécifique, améliorant ainsi l'impact visuel global.

## Pourquoi utiliser Aspose.PSD pour Java afin de personnaliser les effets d'ombre ?

Aspose.PSD pour Java prend en charge **plus de 100 formats d'image** et peut traiter des fichiers PSD jusqu'à **2 Go** sans charger l'intégralité du document en mémoire, offrant des performances de niveau entreprise. La bibliothèque vous donne un contrôle complet sur chaque attribut de l'ombre — couleur, opacité, distance, angle, diffusion et bruit — sans nécessiter l'installation de Photoshop. Elle fonctionne sur les JVM Windows, Linux et macOS, ce qui en fait le choix le plus fiable pour les pipelines graphiques automatisés.

## Prérequis

- Connaissances de base en programmation Java.  
- Aspose.PSD pour Java installé. Vous pouvez le télécharger [ici](https://releases.aspose.com/psd/java/).  

## Importer les packages

Avant de commencer, importez les classes requises afin de travailler avec les images et les effets d'ombre :

La classe `Color` représente une valeur de couleur utilisée dans toute l'API.  
La classe `Image` est le type de base pour tous les objets image.  
La classe `PsdImage` fournit des fonctionnalités spécifiques aux fichiers PSD.  
La classe `PsdLoadOptions` vous permet de spécifier des options de chargement des fichiers PSD, comme l'activation des ressources d'effets.  
La classe `DropShadowEffect` représente un filtre d'ombre portée appliqué à un calque PSD et vous donne accès à toutes ses propriétés réglables.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Guide étape par étape

### Étape 1 : Charger l'image PSD

Tout d'abord, chargez le PSD source tout en activant le chargement des ressources d'effets :

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Shadow.psd";
String psdPathAfterChange = dataDir + "ShadowChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### Étape 2 : Récupérer l'effet d'ombre portée existant

Trouvez l'effet d'ombre sur le calque souhaité (dans cet exemple, le deuxième calque) :

```java
DropShadowEffect shadowEffect = (DropShadowEffect)(im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Étape 3 : Vérifier les paramètres par défaut (facultatif)

L'exécution de ces assertions vous aide à comprendre les valeurs originales avant de les modifier :

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

Nous allons maintenant réellement **modifier la couleur de l'ombre** en vert, ajuster l'opacité, la distance, la taille et d'autres attributs. Cela démontre les capacités de **personnalisation de l'effet d'ombre** d'Aspose.PSD. La méthode `setOpacity(byte)` définit le niveau d'opacité de l'ombre (0‑255).  

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

Enfin, écrivez le PSD mis à jour sur le disque en utilisant la méthode `save` de `PsdImage` :

```java
im.save(psdPathAfterChange);
```

## Problèmes courants et astuces

- **NullPointerException lors de la récupération des effets** – assurez‑vous que `setLoadEffectsResource(true)` est appelé ; sinon les effets ne sont pas chargés.  
- **La couleur ne change pas** – vérifiez que vous modifiez le bon indice de calque (`im.getLayers()[1]` dans cet exemple).  
- **L'opacité semble inchangée** – rappelez‑vous que l'opacité est un byte (0‑255). Un cast en `(byte)` est requis.  

## Conclusion

En suivant ces étapes, vous pouvez **modifier la couleur de l'ombre**, **définir l'opacité de l'ombre** et personnaliser entièrement les paramètres de **l'effet d'ombre** dans n'importe quel fichier PSD à l'aide d'Aspose.PSD pour Java. Cela vous permet de créer des graphiques plus riches de manière programmatique sans intervention manuelle de Photoshop, idéal pour les pipelines de conception automatisés et le traitement par lots.

## Questions fréquemment posées

**Q : Aspose.PSD pour Java convient‑il aux projets de conception graphique professionnelle ?**  
R : Absolument ! Aspose.PSD pour Java est une bibliothèque puissante conçue pour les tâches de conception graphique professionnelle.

**Q : Puis‑je utiliser Aspose.PSD pour Java dans des applications commerciales ?**  
R : Oui, Aspose.PSD pour Java est un produit commercial. Vous pouvez l'acheter [ici](https://purchase.aspose.com/buy).

**Q : Une version d'essai gratuite est‑elle disponible ?**  
R : Oui, vous pouvez explorer une version d'essai gratuite [ici](https://releases.aspose.com/).

**Q : Où puis‑je trouver une documentation détaillée ?**  
R : Consultez la documentation complète [ici](https://reference.aspose.com/psd/java/).

**Q : Comment obtenir du support pour Aspose.PSD pour Java ?**  
R : Rejoignez le forum communautaire [ici](https://forum.aspose.com/c/psd/34) pour toute question de support.

---

**Dernière mise à jour**: 2026-06-18  
**Testé avec**: Aspose.PSD for Java 24.10  
**Auteur**: Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriels associés

- [Manipulation d'images Java - Ajouter des effets à l'exécution avec Aspose.PSD pour Java](/psd/java/advanced-techniques/add-effects-runtime/)
- [Enregistrer le PSD en PNG et appliquer une ombre portée de rendu dans Aspose.PSD pour Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Flouter une image Java avec Aspose.PSD – Ajouter un effet de flou](/psd/java/advanced-techniques/blur-image/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}