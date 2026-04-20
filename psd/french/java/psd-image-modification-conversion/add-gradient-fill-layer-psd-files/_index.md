---
date: 2026-03-23
description: Apprenez à créer des fichiers PSD à remplissage dégradé avec Java en
  utilisant Aspose.PSD. Ce guide montre comment modifier les calques de dégradé PSD,
  ajuster les couleurs, la transparence et d’autres propriétés de manière programmatique.
linktitle: Create Gradient Fill PSD with Java – Add Gradient Fill Layer
second_title: Aspose.PSD Java API
title: Créer un PSD de remplissage en dégradé avec Java – Ajouter un calque de remplissage
  en dégradé
url: /fr/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajouter un calque de remplissage dégradé dans les fichiers PSD avec Java

## Introduction

Vous avez toujours rêvé d'ajouter cette touche supplémentaire de magie visuelle à vos fichiers PSD et vous vous demandez **how to create gradient fill PSD** avec Java ? Les dégradés donnent de la profondeur à vos créations, mais les ajuster manuellement peut être fastidieux. Avec **Aspose.PSD for Java**, vous pouvez modifier les dégradés PSD de façon programmatique, changer les couleurs, ajuster la transparence et affiner chaque propriété — ce qui vous fait gagner du temps et assure la cohérence sur des dizaines de fichiers.

## Réponses rapides
- **Quelle bibliothèque vous permet de modifier les dégradés PSD en Java ?** Aspose.PSD for Java.  
- **Quelle méthode charge un fichier PSD ?** `Image.load(path)`.  
- **Comment changer l'angle du dégradé ?** `settings.setAngle(double)`.  
- **Pouvez‑vous ajouter de nouveaux points de couleur ?** Oui—créez des objets `GradientColorPoint` et ajoutez‑les à la liste des points de couleur.  
- **Avez‑vous besoin d'une licence pour une utilisation en production ?** Une licence commerciale est requise ; un essai gratuit est disponible pour l'évaluation.

## Qu'est‑ce que “create gradient fill PSD” ?
Créer un gradient fill PSD signifie insérer ou modifier de façon programmatique un calque de remplissage basé sur un dégradé à l'intérieur d'un document Photoshop. Cela permet une stylisation automatisée, un traitement par lots et la génération d'images dynamiques sans ouvrir Photoshop.

## Pourquoi utiliser Aspose.PSD pour modifier les dégradés PSD ?
- **Prise en charge complète du .PSD** – fonctionne avec tous les types de calques, y compris les objets dynamiques.  
- **Pas besoin de Photoshop** – s'exécute sur n'importe quel serveur ou pipeline CI.  
- **Contrôle fin** – ajustez l'angle, les décalages, le tramage, les points de couleur et les points de transparence via une API Java claire.  

## Prérequis

Avant de commencer, assurez‑vous de disposer de ce qui suit :

- Java Development Kit (JDK) : une version stable du JDK est nécessaire pour exécuter du code Java. Vous pouvez le télécharger depuis le site d'Oracle : [Link to Oracle JDK download page]
- Aspose.PSD for Java : cette bibliothèque puissante vous permet de travailler avec des fichiers PSD dans vos applications Java. Téléchargez‑la depuis le site d'Aspose : [Link to Aspose.PSD for Java download] (Essai gratuit disponible)

## Importer les packages

Commençons par importer les packages Aspose.PSD essentiels nécessaires pour travailler avec des fichiers PSD :

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.imageoptions.PsdOptions;
import java.util.ArrayList;
import java.util.Collections;
import java.util.List;
```

Ces imports donnent accès aux classes et méthodes pour charger, manipuler et enregistrer des fichiers PSD.

Maintenant, attachez votre ceinture pour le passionnant voyage de modification des calques de remplissage dégradé !

## Comment créer un Gradient Fill PSD avec Java

### Étape 1 : Charger le fichier PSD

Tout d'abord, nous devons charger le fichier PSD contenant le calque de remplissage dégradé que vous souhaitez modifier. Utilisez la méthode `Image.load`, en spécifiant le chemin du fichier :

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ComplexGradientFillLayer.psd";
String outputFile = dataDir + "ComplexGradientFillLayer_output.psd";
PsdImage image = (PsdImage)Image.load(sourceFileName);
```

Cet extrait de code charge le fichier PSD depuis le répertoire spécifié et le stocke dans la variable `image`.

### Étape 2 : Identifier le calque de remplissage dégradé

Les fichiers PSD peuvent contenir de nombreux calques. Nous devons isoler le calque spécifique contenant le remplissage dégradé que nous voulons éditer. Parcourez le tableau `image.getLayers()` pour trouver le calque souhaité :

```java
for (int i = 0; i < image.getLayers().length; i++) {
if (image.getLayers()[i] instanceof FillLayer) {
   FillLayer fillLayer = (FillLayer) image.getLayers()[i];
   // Further checks and modifications will happen here
   break;
}
}
```

Cette boucle vérifie chaque calque. Si un calque est un `FillLayer`, il est casté au type `FillLayer` et stocké dans la variable `fillLayer` pour un traitement ultérieur. Vous pouvez ajouter des vérifications supplémentaires dans la boucle si vous avez des critères spécifiques pour identifier le calque cible (par ex., le nom du calque).

### Étape 3 : Vérifier le type de remplissage dégradé

Tous les calques de remplissage n'utilisent pas de dégradés. Cet extrait de code confirme si le calque identifié contient réellement un remplissage dégradé :

```java
if (fillLayer.getFillSettings().getFillType() != FillType.Gradient) {
   throw new Exception("Wrong Fill Layer");
}
```

Si la méthode `getFillType` ne renvoie pas `FillType.Gradient`, une exception est levée, indiquant que nous travaillons sur le mauvais calque.

## Comment modifier un dégradé PSD avec Aspose.PSD

### Étape 4 : Accéder et modifier les propriétés du dégradé

La magie opère ici ! Aspose.PSD donne accès à diverses propriétés de remplissage dégradé via l'interface `IGradientFillSettings`. Nous pouvons les récupérer et les modifier selon les besoins :

```java
IGradientFillSettings settings = (IGradientFillSettings) fillLayer.getFillSettings();

// Modify properties (replace with desired values)
settings.setAngle(0.0);  // Set angle to 0 degrees
settings.setDither(false);  // Disable dithering
settings.setAlignWithLayer(true); // Align gradient with layer
settings.setReverse(true);  // Reverse gradient direction
settings.setHorizontalOffset(25);  // Set horizontal offset
settings.setVerticalOffset(-15);  // Set vertical offset
```

Ce code récupère l'objet `IGradientFillSettings` puis modifie des propriétés telles que l'angle, le tramage, l'alignement et les décalages. Remplacez les valeurs fournies par les réglages souhaités pour obtenir l'effet de dégradé que vous imaginez.

### Étape 5 : Manipuler les points de couleur et de transparence

Les dégradés sont définis par des points de couleur et de transparence le long d'un spectre. Aspose.PSD vous permet de modifier ces points pour un contrôle précis :

```java
List<IGradientColorPoint> colorPoints = new ArrayList<IGradientColorPoint>();
Collections.addAll(colorPoints, settings.getColorPoints());
List<IGradientTransparencyPoint> transparencyPoints = new ArrayList<IGradientTransparencyPoint>();
Collections.addAll(transparencyPoints, settings.getTransparencyPoints());

// Add a new color point
GradientColorPoint gr1 = new GradientColorPoint();
gr1.setColor(Color.getViolet());
gr1.setLocation(4096);
gr1.setMedianPointLocation(75);
colorPoints.add(gr1);

// Modify an existing color point
colorPoints.get(1).setLocation(3000);

// Add a new transparency point
GradientTransparencyPoint gr2 = new GradientTransparencyPoint();
gr2.setOpacity(80.0);
gr2.setLocation(4096);
gr2.setMedianPointLocation(25);
transparencyPoints.add(gr2);

// Modify an existing transparency point
transparencyPoints.get(2).setLocation(3000);

settings.setColorPoints(colorPoints.toArray(new IGradientColorPoint[0]));
settings.setTransparencyPoints(transparencyPoints.toArray(new IGradientTransparencyPoint[0]));
```

### Étape 6 : Mettre à jour et enregistrer le fichier PSD

Une fois les modifications nécessaires effectuées, mettez à jour le calque de remplissage et enregistrez le fichier PSD :

```java
fillLayer.update();
image.save(outputFile, new PsdOptions(image));
```

La méthode `fillLayer.update()` applique les changements au calque de remplissage dégradé, et `image.save` enregistre le fichier PSD modifié vers le chemin de sortie spécifié.

## Problèmes courants et solutions

- **Exception « Wrong Fill Layer »** – Assurez‑vous de cibler un `FillLayer` qui utilise réellement un dégradé. Vérifiez le nom ou l'index du calque avant le cast.  
- **Les points de couleur ne reflètent pas les changements** – Après avoir modifié la liste des points, appelez toujours `settings.setColorPoints(...)` et `settings.setTransparencyPoints(...)` pour appliquer les mises à jour au calque.  
- **Performance sur les gros PSD** – Si vous traitez de nombreux fichiers, réutilisez la même instance `PsdOptions` et fermez rapidement les images avec `image.dispose()` pour libérer la mémoire.

## FAQ

**Q : Puis‑je ajouter plusieurs points de couleur et de transparence à un dégradé ?**  
R : Absolument ! Vous pouvez ajouter autant de points de couleur et de transparence que nécessaire pour obtenir l'effet de dégradé souhaité. Il suffit de créer de nouveaux points et de les ajouter aux listes correspondantes.

**Q : Comment supprimer un point de couleur ou de transparence d'un dégradé ?**  
R : Utilisez la méthode `remove` de la liste, par ex., `colorPoints.remove(index)`, pour supprimer le point indésirable avant d’appeler `setColorPoints`.

**Q : Puis‑je changer le type de dégradé (linéaire, radial, etc.) ?**  
R : Aspose.PSD prend actuellement en charge les dégradés linéaires. De futures versions pourraient ajouter d'autres types, mais vous pouvez simuler d'autres effets en manipulant les points de couleur et de transparence.

**Q : Y a‑t‑il un impact sur les performances lors de la modification des dégradés ?**  
R : L'impact dépend de la complexité du dégradé et du nombre de modifications. Pour les cas d’utilisation typiques, la surcharge est minimale, mais le traitement par lots de gros fichiers peut bénéficier d’ajustements de gestion de la mémoire.

**Q : Puis‑je appliquer cette technique à plusieurs calques de remplissage dégradé dans un fichier PSD ?**  
R : Oui. Parcourez `image.getLayers()`, vérifiez chaque `FillLayer` pour `FillType.Gradient`, et appliquez les mêmes modifications selon les besoins.

**Q : Ai‑je besoin d’une licence commerciale pour une utilisation en production ?**  
R : Une licence Aspose.PSD valide est requise pour les déploiements en production. Un essai gratuit est disponible à des fins d’évaluation.

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**Dernière mise à jour :** 2026-03-23  
**Testé avec :** Aspose.PSD for Java 24.11 (latest)  
**Auteur :** Aspose