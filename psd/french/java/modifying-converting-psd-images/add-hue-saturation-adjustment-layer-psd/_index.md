---
title: Ajouter un calque de réglage de la saturation de la teinte au PSD
linktitle: Ajouter un calque de réglage de la saturation de la teinte au PSD
second_title: API Java Aspose.PSD
description: Découvrez comment ajouter des couches de réglage de saturation de teinte au PSD à l'aide d'Aspose.PSD pour Java dans ce didacticiel complet, étape par étape. Améliorez votre flux de travail de conception graphique.
weight: 14
url: /fr/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajouter un calque de réglage de la saturation de la teinte au PSD

## Introduction
En matière de conception graphique, la manipulation des couleurs joue un rôle central : en particulier, modifier la teinte, la saturation et la luminosité peut transformer radicalement l'ambiance et la qualité de n'importe quelle image. Un moyen efficace d’y parvenir consiste à utiliser des calques de réglage dans Photoshop (fichiers PSD). Si vous souhaitez améliorer vos fichiers PSD par programmation à l'aide de Java, la bibliothèque Aspose.PSD est là pour vous aider ! Ce didacticiel vous guidera à travers les étapes pour ajouter un calque de réglage de saturation de teinte à vos fichiers PSD, rendant ainsi vos flux de travail plus productifs et efficaces.
Dans ce guide, nous aborderons tout, de l'importation des packages nécessaires aux détails essentiels des exemples de code.
## Conditions préalables
Avant de passer au code, assurez-vous d'avoir les éléments suivants en place :
1.  Kit de développement Java (JDK) : assurez-vous que JDK 8 ou supérieur est installé sur votre ordinateur. Vous pouvez le télécharger depuis le[Téléchargements du kit de développement Java SE](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Bibliothèque Aspose.PSD pour Java : vous aurez besoin de la bibliothèque Aspose.PSD, que vous pouvez[télécharger ici](https://releases.aspose.com/psd/java/). 
3. IDE : un environnement de développement intégré (IDE) approprié comme IntelliJ IDEA ou Eclipse pour le développement Java.
4. Connaissances de base de Java : La connaissance de la programmation Java est un plus, mais ne vous inquiétez pas ; nous vous guiderons à travers le code étape par étape.
Maintenant que nous avons réglé nos prérequis, passons à la partie amusante : le codage !
## Importer des packages
Pour commencer à travailler avec la bibliothèque Aspose.PSD, la première étape consiste à importer les classes nécessaires. Voici comment procéder dans votre fichier Java :
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```
Assurez-vous que les bibliothèques appropriées sont ajoutées à votre projet afin que ces importations fonctionnent de manière transparente.
## Étape 1 : Configurez votre répertoire de documents
Chaque projet a besoin d'un point de départ, et le nôtre ne fait pas exception. Vous devez spécifier un répertoire dans lequel vos fichiers PSD sont stockés. Ceci est crucial pour charger et enregistrer correctement les images.
```java
String dataDir = "Your Document Directory"; // Mettez à jour ce chemin vers votre répertoire actuel
```
## Étape 2 : Charger un fichier PSD existant
Pour manipuler un fichier PSD existant, nous devons d'abord le charger dans notre programme. Voici comment procéder :
```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 Dans ce code, mettez à jour`"HueSaturationAdjustmentLayer.psd"` au nom de votre fichier PSD existant que vous souhaitez modifier.
## Étape 3 : modifier le calque de teinte/saturation
Ensuite, nous parcourrons les calques de notre image PSD chargée pour rechercher et modifier tous les calques de teinte/saturation existants. Cette étape consiste à modifier les valeurs de teinte, de saturation et de luminosité.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof HueSaturationLayer) {
        HueSaturationLayer hueLayer = (HueSaturationLayer) im.getLayers()[i];
        hueLayer.setHue((short) -25);
        hueLayer.setSaturation((short) -12);
        hueLayer.setLightness((short) 67);
        ColorRangeHsl colorRange = hueLayer.getRange(2);
        colorRange.setHue((short) -40);
        colorRange.setSaturation((short) 50);
        colorRange.setLightness((short) -20);
        colorRange.setMostLeftBorder((short) 300);
    }
}
```
Dans cet exemple :
- Nous ajustons la teinte à -25, la saturation à -12 et la luminosité à +67.
-  Le`getRange(2)` La méthode nous permet de modifier des gammes de couleurs spécifiques comme vous le souhaitez.
## Étape 4 : Enregistrez le fichier PSD modifié
Après avoir effectué les ajustements, l'étape suivante consiste à enregistrer le fichier. Il s'agit d'une partie essentielle de notre processus, garantissant que les changements que nous avons apportés ne seront pas perdus.
```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
## Étape 5 : ajouter un nouveau calque de teinte/saturation
Ensuite, vous souhaiterez peut-être ajouter un nouveau calque de réglage Teinte/Saturation à un autre fichier PSD. Suivez simplement la même approche que celle que vous avez utilisée précédemment, mais avec des fichiers PSD différents.
```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```
## Étape 6 : Définir de nouvelles valeurs de teinte/saturation pour le nouveau calque
Maintenant que vous avez créé ce nouveau calque, appliquez les paramètres de teinte, de saturation et de luminosité souhaités, comme avant.
```java
hueLayerNew.setHue((short) -25);
hueLayerNew.setSaturation((short) -12);
hueLayerNew.setLightness((short) 67);
ColorRangeHsl newColorRange = hueLayerNew.getRange(2);
newColorRange.setHue((short) -160);
newColorRange.setSaturation((short) 100);
newColorRange.setLightness((short) 20);
newColorRange.setMostLeftBorder((short) 300);
```
## Étape 7 : Enregistrez le fichier PSD mis à jour
Enfin, enregistrez le fichier PSD avec le calque Teinte/Saturation ajouté afin que vous puissiez voir vos modifications.
```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```
Félicitations! Vous avez manipulé avec succès des fichiers PSD à l'aide d'Aspose.PSD pour Java. Désormais, vous pouvez expérimenter différentes images et des modifications plus profondes, donnant ainsi vie à vos projets de conception graphique.
## Conclusion
Travailler avec des graphiques par programmation ouvre un monde de possibilités. L'utilisation d'Aspose.PSD pour Java pour ajouter et modifier des couches de réglage de saturation de teinte offre une flexibilité et une efficacité qui peuvent rationaliser votre flux de travail de conception. Que vous retouchiez des photos pour un projet ou créiez un contenu visuel époustouflant, la maîtrise de ces outils peut grandement améliorer votre résultat.
 N'hésitez pas à explorer plus de fonctionnalités d'Aspose.PSD en plongeant dans[documentation](https://reference.aspose.com/psd/java/) ou envisagez d'acquérir un[permis temporaire](https://purchase.aspose.com/temporary-license/) pour tester toute la puissance de la bibliothèque.
## FAQ
### Qu'est-ce qu'un calque de réglage de la saturation de la teinte ?
Un calque de réglage de la saturation de la teinte vous permet de modifier les propriétés de couleur d'une image sans altérer de manière permanente les pixels d'origine.
### Dois-je installer Photoshop pour utiliser Aspose.PSD ?
Non, Aspose.PSD est une bibliothèque autonome qui fonctionne indépendamment de Photoshop.
### Puis-je utiliser Aspose.PSD pour le traitement par lots ?
Oui, vous pouvez automatiser et traiter par lots plusieurs fichiers PSD avec Aspose.PSD.
### Aspose.PSD est-il gratuit ?
Aspose.PSD propose un essai gratuit, mais une licence est requise pour une utilisation à long terme. Vous pouvez consulter les prix[ici](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
