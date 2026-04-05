---
date: 2026-04-05
description: Apprenez à exporter des PSD en PNG et à améliorer facilement le contraste
  de l'image avec Aspose.PSD pour Java. Maîtrisez les calques de réglage des niveaux
  grâce à ce guide pas à pas.
keywords:
- export psd to png
- how to adjust levels
- batch process psd files
linktitle: Exporter le PSD en PNG et rendre le calque de réglage de niveau en Java
second_title: Aspose.PSD Java API
title: Exporter le PSD en PNG et rendre le calque de réglage de niveaux en Java
url: /fr/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter PSD en PNG et rendre le calque d'ajustement de niveaux en Java

## Introduction

Vous avez déjà ouvert un fichier PSD pour constater que les couleurs semblent ternes ou que le contraste est mauvais ? Vous pouvez rapidement **exporter PSD en PNG** tout en ajustant finement l'image avec un calque d'ajustement de niveaux à l'aide d'Aspose.PSD pour Java. Dans ce tutoriel, nous parcourrons l'ensemble du processus — du chargement d'un PSD, à l'ajustement de ses niveaux, jusqu'à l'enregistrement du résultat en PNG — afin que vous puissiez augmenter la vivacité et préparer des ressources prêtes pour le web en quelques minutes.

## Réponses rapides
- **Qu'est-ce que « exporter PSD en PNG » signifie ?** Cela convertit un document Photoshop en une image PNG sans perte tout en préservant la transparence.  
- **Puis-je ajuster les niveaux avant d'exporter ?** Oui, Aspose.PSD vous permet de modifier les niveaux d'entrée et de sortie de façon programmatique.  
- **Ai-je besoin d'une licence ?** Un essai gratuit suffit pour le développement ; une licence commerciale est requise pour la production.  
- **Le traitement par lots est‑il possible ?** Absolument — vous pouvez placer le code dans une boucle pour gérer plusieurs fichiers PSD.  
- **Quelle version de Java est requise ?** Java 8 ou plus récent est recommandé.

## Qu'est-ce que « exporter PSD en PNG » ?
Exporter un PSD en PNG signifie prendre le fichier Photoshop à calques et le rasteriser en une image Portable Network Graphics. PNG prend en charge la compression sans perte et un canal alpha, ce qui le rend idéal pour les graphiques web et les ressources d'interface utilisateur.

## Pourquoi ajuster les niveaux avant d'exporter ?
L'ajustement des niveaux vous permet de contrôler les ombres, les tons moyens et les hautes lumières, améliorant le contraste global et l'équilibre des couleurs. Cette étape garantit que le PNG final apparaît soigné sans nécessiter de retouche manuelle dans Photoshop.

## Prérequis

- **Java Development Kit (JDK)** – téléchargez la dernière version depuis le site d'Oracle ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).  
- **Bibliothèque Aspose.PSD pour Java** – obtenez‑la depuis la page officielle de téléchargement ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). Un essai gratuit est disponible ([https://releases.aspose.com/](https://releases.aspose.com/)).  

## Importer les packages

Avant de plonger dans le code, importez les classes qui nous donnent accès à la manipulation de PSD et à l'exportation PNG :

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

## Guide étape par étape

### Étape 1 : Définir les chemins de fichiers (Comment automatiser le traitement PSD)

Définissez des variables claires et descriptives pour le PSD source, le PSD modifié et l'emplacement d'exportation du PNG final.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

### Étape 2 : Charger l'image PSD

Utilisez `Image.load` pour lire le fichier PSD dans un objet `PsdImage`. Aspose.PSD détecte automatiquement le format.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Étape 3 : Parcourir les calques (Comment ajuster les niveaux)

Parcourez chaque calque afin de localiser le calque d'ajustement de niveaux.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (code to check for Levels Layer will be added here)
}
```

### Étape 4 : Identifier le calque de niveaux

Vérifiez chaque calque avec `instanceof LevelsLayer`. Lorsqu'il est trouvé, effectuez un cast afin de pouvoir modifier ses propriétés.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (code to adjust levels will be added here)
   }
}
```

### Étape 5 : Ajuster finement les niveaux (Comment ajuster les niveaux)

Ajustez les niveaux d'entrée et de sortie pour le premier canal (généralement le canal composite). Ces valeurs sont des exemples ; n'hésitez pas à expérimenter.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Adjust Input Levels (0‑255):
	   channel.setInputShadowLevel((short) 10); // Darken shadows slightly
	   channel.setInputMidtoneLevel(2.0f);     // Increase midtones
	   channel.setInputHighlightLevel((short) 230); // Reduce highlights

	   // Adjust Output Levels (0‑255):
	   channel.setOutputShadowLevel((short) 20); // Darken shadows further
	   channel.setOutputHighlightLevel((short) 200); // Brighten highlights
   }
}
```

### Étape 6 : Enregistrer le PSD modifié (Comment automatiser le PSD)

Enregistrez les modifications dans un nouveau fichier PSD.

```java
im.save(psdPathAfterChange);
```

### Étape 7 : Exporter en PNG (Exporter PSD en PNG)

Si vous avez besoin d'une version PNG, configurez `PngOptions` et enregistrez l'image.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

## Cas d'utilisation courants

- **Préparation d'actifs web :** Convertissez les maquettes PSD fournies par le designer en PNG prêts pour les navigateurs.  
- **Traitement par lots :** Automatisez la conversion de dizaines de fichiers PSD dans un pipeline CI.  
- **Génération d'images dynamiques :** Ajustez les niveaux à la volée en fonction des entrées utilisateur avant l'exportation.  

## Dépannage et conseils

- **Null pointer lors de l'accès aux calques :** Assurez‑vous que le PSD contient réellement un calque d'ajustement de niveaux ; sinon, ajoutez une vérification de null.  
- **Couleurs inattendues après l'exportation :** Vérifiez que le type de couleur PNG est réglé sur `TruecolorWithAlpha` pour conserver la transparence.  
- **Performance avec de nombreux fichiers :** Réutilisez la même instance `PsdImage` lors du traitement d'un lot afin de réduire la consommation de mémoire.  

## Questions fréquemment posées

**Q : Puis‑je ajuster séparément les canaux de couleur individuels (RGB) ?**  
R : Oui. Utilisez `levelsLayer.getChannel(index)` où `index` = 0 (Rouge), 1 (Vert), 2 (Bleu) pour modifier chaque canal indépendamment.

**Q : Comment gérer plusieurs calques d'ajustement de niveaux dans un même PSD ?**  
R : La boucle traite chaque calque ; chaque `LevelsLayer` trouvé sera ajusté selon le code à l'intérieur du bloc `if`.

**Q : Existe‑t‑il d'autres moyens d'améliorer le contraste en dehors des niveaux ?**  
R : Aspose.PSD propose également les ajustements Courbes, Luminosité/Contraste et Égalisation d'histogramme.

**Q : Puis‑je automatiser cela pour un dossier de fichiers PSD ?**  
R : Enveloppez l'ensemble du flux de travail dans une boucle `File[] files = new File(dataDir).listFiles((d, name) -> name.endsWith(".psd"));` et traitez chaque fichier séquentiellement.

**Q : Où puis‑je trouver plus de documentation et d'assistance ?**  
R : Consultez la référence officielle ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) et le forum communautaire ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)).

## Conclusion

En maîtrisant le flux de travail **exporter PSD en PNG** et en apprenant **comment ajuster les niveaux** de façon programmatique, vous obtenez un contrôle total sur la qualité de l'image sans quitter votre environnement Java. Que vous prépariez des ressources pour le web, automatisiez un pipeline de conception ou construisiez un processeur par lots, Aspose.PSD pour Java rend la tâche simple et fiable.

---

**Dernière mise à jour :** 2026-04-05  
**Testé avec :** Aspose.PSD 24.11 for Java  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}