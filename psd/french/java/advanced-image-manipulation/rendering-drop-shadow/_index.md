---
date: 2026-04-22
description: Apprenez à enregistrer un PSD au format PNG, à exporter un PNG avec canal
  alpha et à ajouter un calque d’ombre portée en utilisant Aspose.PSD pour Java –
  un guide complet, étape par étape.
keywords:
- save psd as png
- convert psd to png
- export png with alpha
- batch psd to png
- preserve png transparency
linktitle: Appliquer l’ombre portée de rendu
second_title: Aspose.PSD Java API
title: Enregistrer le PSD au format PNG et appliquer l'ombre portée lors du rendu
  dans Aspose.PSD pour Java
url: /fr/java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Enregistrer le PSD en PNG et appliquer une ombre portée lors du rendu avec Aspose.PSD pour Java

## Introduction

Si vous travaillez avec des fichiers Photoshop en Java, **enregistrer un PSD en PNG** est l’une des tâches les plus courantes que vous rencontrerez. Dans de nombreux projets, vous devrez **enregistrer le PSD en PNG** pour livrer des actifs sur le web ou les applications mobiles, tout en préservant la transparence et les effets visuels. Avec Aspose.PSD, vous pouvez non seulement **convertir le PSD en PNG**, mais aussi améliorer l’image en **ajoutant un calque d’ombre portée**. Dans ce tutoriel, nous parcourrons l’ensemble du processus — chargement d’un PSD, application d’une ombre portée lors du rendu, puis **enregistrement du PSD au format PNG** — afin que vous puissiez intégrer ce flux de travail dans vos propres projets en toute confiance.

## Réponses rapides
- **Quelle bibliothèque gère la conversion PSD vers PNG ?** Aspose.PSD pour Java.  
- **Combien de temps prend l’implémentation de l’ombre portée ?** Environ 10‑15 minutes pour un exemple de base.  
- **Ai‑je besoin d’une licence pour exécuter le code ?** Une version d’essai gratuite suffit pour l’évaluation ; une licence est requise en production.  
- **Puis‑je appliquer l’ombre à plusieurs calques ?** Oui — il suffit de parcourir les calques souhaités, ce qui permet également d’effectuer une conversion par lots de PSD en PNG.  
- **Quelle version de Java est requise ?** Java 8 ou supérieure.

## Qu’est‑ce que « enregistrer le PSD en PNG » et pourquoi est‑ce important ?

**Enregistrer un PSD en PNG** crée une image sans perte, largement prise en charge, qui conserve la transparence. C’est essentiel lorsque vous devez afficher des actifs Photoshop sur le web, dans des applications mobiles ou dans le cadre d’un pipeline de traitement d’images plus vaste. Ajouter une ombre portée en même temps vous permet de produire un effet visuel soigné sans ouvrir Photoshop.

## Pourquoi utiliser Aspose.PSD pour ce flux de travail ?

* **Contrôle total depuis le code** – Aucun besoin de lancer Photoshop ou de dépendre d’outils externes.  
* **Préserve les effets de calque** – Les ombres portées, lueurs et autres effets sont rendus exactement comme ils apparaissent dans le fichier original.  
* **Export PNG avec alpha** – La sortie PNG conserve le fond transparent, garantissant que vous **préservez la transparence PNG** pour les interfaces utilisateur ou le web.  
* **Multiplateforme** – Fonctionne sur tout système d’exploitation supportant Java 8+.

## Prérequis

Avant de commencer, assurez‑vous d’avoir :

- **Environnement de développement Java** – JDK 8 ou plus récent installé.  
- **Aspose.PSD pour Java** – Téléchargez le JAR le plus récent depuis la [page de téléchargement Aspose.PSD](https://releases.aspose.com/psd/java/).  
- **Un fichier PSD** – Le fichier doit contenir au moins un calque que vous souhaitez enrichir d’une ombre portée (par ex., *Shadow.psd*).

## Importer les packages

Tout d’abord, importez les classes dont nous aurons besoin. Cela nous donne accès au chargement d’image, aux effets de calque et aux options d’export PNG.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

## Guide étape par étape

### Étape 1 : Définir le répertoire du document  
Indiquez au programme où se trouve votre PSD source.

```java
String dataDir = "Your Document Directory";
```

### Étape 2 : Définir les chemins des fichiers PSD et PNG  
Spécifiez à la fois le PSD d’entrée et le PNG de sortie qui contiendra l’ombre portée rendue.

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### Étape 3 : Charger le fichier PSD avec les effets  
Activez le chargement des ressources d’effet afin de pouvoir manipuler l’effet d’ombre portée.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Étape 4 : Accéder à l’effet d’ombre portée  
Récupérez le premier effet d’ombre portée du deuxième calque (indice 1). C’est ici que nous vérifierons ou modifierons les paramètres.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Étape 5 : Valider les propriétés de l’effet d’ombre  
Assurez‑vous que les propriétés de l’effet correspondent à vos attentes avant l’enregistrement. Vous pouvez également ajuster ces valeurs pour obtenir un rendu différent.

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

> **Astuce :** Ajustez `setSpread()` ou `setNoise()` pour créer des ombres plus douces ou plus texturées.

### Étape 6 : Enregistrer en PNG – l’étape « enregistrer le PSD en PNG »  
Exportez l’image modifiée au format PNG, en préservant le canal alpha afin que l’ombre se fonde correctement.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

À ce stade, vous avez réussi à **convertir le PSD en PNG**, **exporter le PNG avec alpha**, et appliquer une ombre portée lors du rendu dans un seul flux de travail.

## Exporter le PNG avec transparence alpha

Lorsque vous avez besoin que la sortie PNG conserve son arrière‑plan transparent—surtout pour les superpositions UI ou les graphiques web—assurez‑vous d’utiliser `PngColorType.TruecolorWithAlpha` comme indiqué dans l’étape d’enregistrement ci‑dessus. Cela garantit que l’ombre portée repose sur un canevas transparent plutôt que sur un fond uni, vous aidant à **préserver la transparence PNG**.

## Ajouter un calque d’ombre portée avec Java

Si votre PSD contient plusieurs calques nécessitant des ombres, répétez simplement **l’Étape 4** et **l’Étape 5** à l’intérieur d’une boucle qui itère sur `im.getLayers()`. Chaque itération peut créer ou modifier une instance `DropShadowEffect`, vous offrant un contrôle granulaire sur l’opacité, la distance, la taille et l’angle pour chaque calque. Cette approche permet également une **conversion par lots de PSD en PNG** où chaque fichier reçoit le même traitement d’ombre.

## Cas d’utilisation courants pour enregistrer le PSD en PNG

* **Pipelines d’actifs web** – Convertir les PSD fournis par les designers en PNG prêts pour le web avec des ombres intégrées.  
* **Ressources d’applications mobiles** – Générer des icônes PNG transparentes à la volée, évitant l’exportation manuelle.  
* **Traitement par lots** – Automatiser la conversion de centaines de fichiers PSD dans un job serveur, en veillant à ce que chaque PNG conserve son canal alpha et ses effets visuels.

## Problèmes courants et solutions

| Problème | Cause probable | Solution |
|----------|----------------|----------|
| **Ombre non visible** | `Opacity` réglé à 0 ou calque masqué | Vérifiez que `shadowEffect.getOpacity()` > 0 et que la visibilité du calque est activée. |
| **Le PNG apparaît plat (pas de transparence)** | Mauvais `PngColorType` utilisé | Utilisez `PngColorType.TruecolorWithAlpha` comme indiqué. |
| **Exception lors du chargement** | Les effets ne sont pas chargés | Assurez‑vous d’appeler `loadOptions.setLoadEffectsResource(true)`. |
| **Indice de calque incorrect** | Structure du PSD différente | Inspectez `im.getLayers()` et choisissez le bon indice. |

## Foire aux questions

**Q : Puis‑je appliquer des ombres portées à plusieurs calques simultanément ?**  
R : Oui. Parcourez `im.getLayers()` et ajoutez ou modifiez un `DropShadowEffect` pour chaque calque cible, ce qui permet également une conversion par lots de PSD en PNG.

**Q : Que contrôle le paramètre « Spread » ?**  
R : `Spread` détermine la rapidité avec laquelle l’ombre passe de l’opacité maximale à la transparence. Une valeur plus élevée crée un bord plus net.

**Q : Aspose.PSD est‑il compatible avec toutes les versions de Photoshop ?**  
R : Aspose.PSD prend en charge les fichiers PSD de Photoshop 3.0 jusqu’à la version la plus récente, en gérant la plupart des types de calques et d’effets.

**Q : Comment tester le code avant d’acheter une licence ?**  
R : Téléchargez la version d’essai gratuite depuis la [page de téléchargement Aspose.PSD](https://releases.aspose.com/psd/java/) et exécutez l’exemple sans clé de licence.

**Q : Où puis‑je obtenir de l’aide en cas de problème ?**  
R : Posez votre question sur le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) où la communauté et les ingénieurs Aspose peuvent vous assister.

## Conclusion

Vous savez maintenant comment **enregistrer le PSD en PNG**, **exporter le PNG avec alpha**, **convertir le PSD en PNG**, et **appliquer un calque d’ombre portée** en utilisant Aspose.PSD pour Java. Cette combinaison vous permet d’automatiser la préparation d’images de haute qualité pour le web, le mobile ou les applications de bureau—sans jamais ouvrir Photoshop.

---

**Dernière mise à jour :** 2026-04-22  
**Testé avec :** Aspose.PSD 24.11 pour Java  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}