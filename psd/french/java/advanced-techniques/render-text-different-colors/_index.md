---
date: 2026-05-29
description: Apprenez à enregistrer un PSD au format PNG avec du texte coloré en utilisant
  Aspose.PSD pour Java. Ce guide étape par étape montre comment convertir un PSD en
  PNG efficacement.
keywords:
- save psd as png
- convert psd to png
- Aspose.PSD Java
linktitle: Rendu du texte avec différentes couleurs dans le calque de texte
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to save PSD as PNG with colored text using Aspose.PSD for
    Java. This step‑by‑step guide shows how to convert PSD to PNG efficiently.
  headline: Save PSD as PNG with Colored Text using Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD is primarily designed for Java, but Aspose provides similar
      libraries for various programming languages.
    question: Can I use Aspose.PSD for Java with other programming languages?
  - answer: Yes, you can obtain a free trial version from [Aspose.PSD](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.PSD for Java?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community
      support and discussions.
    question: Where can I find additional support or assistance?
  - answer: You can request a temporary license from [Aspose.PSD](https://purchase.aspose.com/temporary-license/).
    question: How can I obtain a temporary license for Aspose.PSD for Java?
  - answer: Yes, explore the [Aspose.PSD documentation](https://reference.aspose.com/psd/java/)
      for more tutorials and examples.
    question: Are there other tutorials available for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Enregistrer le PSD au format PNG avec du texte coloré à l'aide d'Aspose.PSD
  pour Java
url: /fr/java/advanced-techniques/render-text-different-colors/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Enregistrer un PSD en PNG avec du texte coloré à l'aide d'Aspose.PSD pour Java

Bienvenue dans notre guide étape par étape sur la façon **d'enregistrer un PSD en PNG** avec du texte de différentes couleurs en utilisant Aspose.PSD pour Java. Aspose.PSD est une puissante bibliothèque Java qui vous permet de manipuler les fichiers Photoshop de manière programmatique, vous offrant des capacités étendues pour travailler avec les formats de fichiers PSD et PSB.

Dans ce tutoriel, nous vous guiderons à travers le processus de rendu de texte avec diverses couleurs dans un calque de texte à l'aide d'Aspose.PSD. À la fin de ce guide, vous comprendrez clairement comment réaliser cette tâche sans effort.

## Réponses rapides
- **Comment enregistrer un PSD en PNG ?** Utilisez la classe `PsdImage` d'Aspose.PSD pour charger le PSD et appelez `save` avec `PngOptions`.
- **Puis-je rendre plusieurs couleurs dans une même couche de texte ?** Oui, attribuez différents objets `Color` à chaque `Portion` du texte.
- **Quelle version de Java est requise ?** Java 8 ou supérieur est pris en charge.
- **Ai-je besoin d'une licence pour la production ?** Une licence commerciale est requise ; une version d'essai gratuite est disponible.
- **La bibliothèque est‑elle efficace en mémoire pour les gros fichiers ?** Elle peut gérer des fichiers jusqu'à 2 GB sans chargement complet en mémoire.

## Comment enregistrer un PSD en PNG avec du texte coloré ?

Chargez votre fichier PSD, modifiez les portions du calque de texte pour leur attribuer des couleurs distinctes, puis enregistrez l'image au format PNG — tout ce flux de travail s'effectue en quelques lignes de code Java. Aspose.PSD rasterise automatiquement le calque modifié, préservant la transparence et la fidélité des couleurs, de sorte que le PNG résultant correspond au design original.

## Qu'est-ce qu'Aspose.PSD pour Java ?

Aspose.PSD pour Java est une bibliothèque qui permet la création, la modification et la conversion programmatiques de fichiers Photoshop (PSD/PSB). Elle prend en charge **plus de 50 formats d'image** et peut traiter des documents de plusieurs centaines de pages sans charger le fichier entier en mémoire, offrant ainsi de hautes performances pour l'automatisation côté serveur.

## Prérequis

- Connaissances de base en programmation Java.
- Bibliothèque Aspose.PSD pour Java installée. Vous pouvez la télécharger depuis la [documentation Aspose.PSD pour Java](https://reference.aspose.com/psd/java/).

## Importer les packages

`Image` est la classe de base pour charger et enregistrer des fichiers image. `PsdImage` représente un document Photoshop, tandis que `TextLayer` donne accès aux propriétés du calque de texte. `PngOptions` définit les paramètres d'exportation PNG.  
```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## Étape 1 : Configurer votre projet

Créez un nouveau projet Java et incluez la bibliothèque Aspose.PSD. Assurez‑vous de disposer des autorisations nécessaires pour accéder et modifier les fichiers dans le répertoire de votre projet.

## Étape 2 : Définir les répertoires source et de sortie

Spécifiez les répertoires source et de sortie où se trouvent vos fichiers PSD et où les images résultantes seront enregistrées. Mettez à jour les variables `sourceDir` et `outputDir` en conséquence.  
```java
String sourceDir = "Your Document Directory";
String outputDir = "Your Document Directory";
```

## Étape 3 : Charger le fichier PSD et accéder au calque de texte

`PsdImage` charge un fichier PSD en mémoire, et `TextLayer` permet de manipuler le contenu texte de ce calque.  
```java
String targetFilePath = sourceDir + "text_ethalon_different_colors.psd";
String resultFilePath = outputDir + "RenderTextWithDifferentColorsInTextLayer_out.png";

PsdImage psdImage = null;
try
{
    psdImage = (PsdImage) Image.load(targetFilePath);
    TextLayer txtLayer = (TextLayer)psdImage.getLayers()[1];
    txtLayer.getTextData().updateLayerData();
```

## Étape 4 : Définir les options PNG et enregistrer l'image résultante

`PngOptions` configure les paramètres de sortie PNG tels que le type de couleur et la compression.  
```java
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
    psdImage.save(resultFilePath, pngOptions);
}
finally
{
    if (psdImage != null) psdImage.dispose();
}
```

## Problèmes courants et solutions

- **Exception de licence manquante :** Assurez‑vous d'avoir appliqué un fichier de licence valide avant d'appeler toute opération d'enregistrement.  
- **Couleur non appliquée :** Vérifiez que chaque `Portion` du calque de texte a bien sa propriété `Color` définie correctement.  
- **Utilisation mémoire pour les gros fichiers :** Utilisez la surcharge `load` de `PsdImage` avec `loadOptions` pour diffuser les gros fichiers.

## Questions fréquemment posées

**Q : Puis-je utiliser Aspose.PSD pour Java avec d'autres langages de programmation ?**  
A : Aspose.PSD est principalement conçu pour Java, mais Aspose propose des bibliothèques similaires pour divers langages de programmation.

**Q : Existe-t-il une version d'essai disponible pour Aspose.PSD pour Java ?**  
A : Oui, vous pouvez obtenir une version d'essai gratuite depuis [Aspose.PSD](https://releases.aspose.com/).

**Q : Où puis‑je trouver un support ou une assistance supplémentaires ?**  
A : Visitez le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour obtenir de l'aide communautaire et des discussions.

**Q : Comment obtenir une licence temporaire pour Aspose.PSD pour Java ?**  
A : Vous pouvez demander une licence temporaire depuis [Aspose.PSD](https://purchase.aspose.com/temporary-license/).

**Q : Existe-t-il d'autres tutoriels disponibles pour Aspose.PSD ?**  
A : Oui, explorez la [documentation Aspose.PSD](https://reference.aspose.com/psd/java/) pour plus de tutoriels et d'exemples.

**Q : La bibliothèque prend‑elle en charge la conversion par lots de plusieurs fichiers PSD en PNG ?**  
A : Oui, vous pouvez parcourir un dossier de fichiers PSD, appliquer la même logique de couleur de texte, et enregistrer chaque fichier en PNG à l'aide d'une boucle.

**Q : Le PNG de sortie est‑il sans perte ?**  
A : Le PNG enregistré via Aspose.PSD conserve une qualité totalement sans perte, préservant toutes les informations de couleur et de transparence.

---

**Dernière mise à jour :** 2026-05-29  
**Testé avec :** Aspose.PSD 24.12 pour Java  
**Auteur :** Aspose

{{< blocks/products/products-backtop-button >}}

## Tutoriels associés

- [Exporter le PSD en PNG & ajouter un nouveau calque régulier avec Aspose.PSD pour Java](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [Enregistrer le PSD en PNG et appliquer une ombre portée lors du rendu avec Aspose.PSD pour Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Convertir le PSD en PNG avec superposition de couleur – Aspose.PSD pour Java](/psd/java/advanced-image-manipulation/rendering-color-effect/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}