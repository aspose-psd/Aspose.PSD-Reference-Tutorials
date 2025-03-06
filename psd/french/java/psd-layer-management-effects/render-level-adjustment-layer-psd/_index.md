---
title: Couche de réglage du niveau de rendu dans les fichiers PSD - Java
linktitle: Couche de réglage du niveau de rendu dans les fichiers PSD - Java
second_title: API Java Aspose.PSD
description: Apprenez à améliorer sans effort le contraste et le dynamisme de l'image à l'aide d'Aspose.PSD pour Java. Couches de réglage des niveaux de maîtrise avec ce guide étape par étape.
weight: 17
url: /fr/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Couche de réglage du niveau de rendu dans les fichiers PSD - Java

## Introduction

Avez-vous déjà ouvert un fichier PSD uniquement pour constater que l'image manquait de contraste ou de dynamisme ? N'ayez crainte, guerriers de l'édition d'images ! Aspose.PSD pour Java vient à la rescousse avec ses puissantes capacités de manipulation des couches de réglage des niveaux. Ce guide vous fournira les connaissances nécessaires pour affiner vos images en utilisant les niveaux en un clin d'œil. 

## Conditions préalables

- Kit de développement Java (JDK) : assurez-vous qu'une version récente de JDK est installée sur votre système. Vous pouvez le télécharger depuis le site Web d'Oracle ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).
- Bibliothèque Aspose.PSD pour Java : téléchargez la bibliothèque Aspose.PSD pour Java à partir de la page de téléchargement ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). Vous aurez besoin d'une licence valide pour utiliser toutes les fonctionnalités, mais un essai gratuit est disponible pour vous aider à démarrer ([https://releases.aspose.com/](https://releases.aspose.com/)).

## Importer des packages

Avant de plonger dans le code, nous devons importer les classes Aspose.PSD nécessaires pour interagir avec les fichiers PSD. Voici ce dont vous aurez besoin :

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

 Le`com.aspose.psd` Le package donne accès aux fonctionnalités de manipulation PSD, tandis que`com.aspose.psd.imaging.PngOptions` nous permet de définir des options lors de l'enregistrement de l'image au format PNG.

Maintenant, lançons-nous dans notre aventure d'ajustement des niveaux :

## Étape 1 : Configuration des chemins de fichiers :

- Définissez des variables pour votre répertoire de documents (`dataDir`), nom du fichier PSD source (`sourceFileName`), nom du fichier PSD cible après modification (`psdPathAfterChange`) et le chemin d'exportation PNG final (`pngExportPath`). Pensez à utiliser des noms descriptifs pour améliorer la lisibilité du code.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

## Étape 2 : Chargement de l'image PSD :

-  Utilisez le`Image.load` méthode pour ouvrir le fichier PSD source et le stocker dans un`PsdImage`objet (`im`). Aspose.PSD détecte automatiquement le format de fichier.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Étape 3 : Itération à travers les couches :

- Nous devons trouver le calque de réglage des niveaux dans votre PSD. Aspose fournit un moyen pratique de parcourir toutes les couches à l'aide d'une boucle.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (le code pour vérifier la couche de niveaux sera ajouté ici)
}
```

## Étape 4 : Identification de la couche de niveaux :

- À l'intérieur de la boucle, vérifiez si le calque actuel (`im.getLayers()[i]` ) est une instance de`LevelsLayer` classe en utilisant le`instanceof` opérateur. 
-  Si tel est le cas, convertissez le calque en un`LevelsLayer` objet pour une manipulation ultérieure.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (le code pour ajuster les niveaux sera ajouté ici)
   }
}
```
## Étape 5 : Affiner les niveaux (suite) :

-  Ajustez les niveaux de sortie à l’aide de`setOutputShadowLevel` et`setOutputHighlightLevel` pour contrôler l'obscurité et la clarté de l'image résultante. Ces valeurs déterminent la plage de niveaux d'entrée qui sera mappée à la plage de sortie.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Ajustez les niveaux d'entrée (0-255) :
	   channel.setInputShadowLevel((short) 10); // Assombrir légèrement les ombres
	   channel.setInputMidtoneLevel(2.0f);     // Augmenter les tons moyens
	   channel.setInputHighlightLevel((short) 230); // Réduire les reflets

	   // Ajustez les niveaux de sortie (0-255) :
	   channel.setOutputShadowLevel((short) 20); // Assombrir davantage les ombres
	   channel.setOutputHighlightLevel((short) 200); //Éclaircir les reflets
   }
}
```

## Étape 6 : Enregistrement du PSD modifié :

-  Utilisez le`save` méthode du`PsdImage` objet pour enregistrer l'image modifiée dans le chemin spécifié (`psdPathAfterChange`).

```java
im.save(psdPathAfterChange);
```

## Étape 7 : Exportation au format PNG (facultatif) :

-  Si vous avez besoin d'une version PNG de l'image ajustée, créez un`PngOptions` objet et définissez le type de couleur sur`TruecolorWithAlpha` . Ensuite, utilisez le`save` méthode à nouveau avec le chemin d’exportation PNG et les options.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

Et voilà ! Vous avez ajusté avec succès la couche de réglage des niveaux dans votre fichier PSD à l'aide d'Aspose.PSD pour Java. En comprenant ces étapes et en expérimentant différentes valeurs, vous pouvez améliorer le contraste et l'apparence générale de vos images.

## Conclusion

Aspose.PSD pour Java vous permet de prendre le contrôle de votre processus d'édition d'images. En maîtrisant le calque de réglage des niveaux, vous pouvez insuffler une nouvelle vie à vos photos et créations. N'oubliez pas que la pratique rend parfait, alors n'hésitez pas à expérimenter et à explorer tout le potentiel de cet outil puissant.
 
## FAQ

### Puis-je régler les canaux de couleur individuels (RVB) séparément ? 
Oui, vous pouvez accéder à chaque canal de couleur en utilisant le`getChannel` méthode du`LevelsLayer` objet et modifier ses niveaux indépendamment.

### Comment gérer plusieurs calques de réglage de niveaux dans un PSD ?
Le code parcourt tous les calques, il traitera donc automatiquement tous les calques de niveaux supplémentaires trouvés dans l'image.

### Existe-t-il d'autres moyens de régler le contraste de l'image que les niveaux ?
Absolument! Aspose.PSD propose divers outils de réglage d'image tels que les courbes, la luminosité/contraste, etc.

### Puis-je automatiser ce processus pour plusieurs images ? 
Oui, vous pouvez incorporer ce code dans un script de traitement en boucle ou par lots pour traiter efficacement plusieurs fichiers PSD.

### Où puis-je trouver plus d’informations et d’assistance ?
Aspose fournit une documentation complète ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) et un forum d'assistance ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)) pour toute question ou problème que vous pourriez rencontrer.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
