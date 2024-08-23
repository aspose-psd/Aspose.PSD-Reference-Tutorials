---
title: Ajouter un calque de réglage de niveau dans PSD
linktitle: Ajouter un calque de réglage de niveau dans PSD
second_title: API Java Aspose.PSD
description: Découvrez comment ajouter efficacement une couche de réglage de niveau dans vos fichiers PSD à l'aide d'Aspose.PSD pour Java. Élevez vos compétences en matière d'édition d'images.
type: docs
weight: 16
url: /fr/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
---
## Introduction
Lorsqu'il s'agit de retouche d'images, la gestion des niveaux peut faire toute la différence dans le dynamisme et la clarté de vos photos. Un outil pratique de l'arsenal Photoshop est le « Calque de réglage du niveau », qui vous permet de modifier la gamme de tons et la balance des couleurs de vos images. Dans ce guide, nous vous expliquerons comment implémenter une couche de réglage de niveau dans un fichier PSD à l'aide d'Aspose.PSD pour Java. Alors, prenez votre IDE Java.
## Conditions préalables
Avant de vous lancer dans le monde des réglages de niveau, vous devrez configurer quelques éléments pour garantir une conduite en douceur :
1.  Kit de développement Java (JDK) : assurez-vous que le JDK est installé sur votre ordinateur. Si vous ne l'avez pas, vous pouvez le récupérer sur[Site Web d'Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) ou utilisez OpenJDK.
2.  Bibliothèque Aspose.PSD pour Java : pour manipuler des fichiers PSD, vous devrez télécharger la bibliothèque Aspose.PSD. Vous pouvez obtenir la dernière version à partir de ceci[lien de téléchargement](https://releases.aspose.com/psd/java/) et assurez-vous d'avoir inclus le JAR dans la bibliothèque de votre projet.
3. Connaissance de base de Java : avoir une compréhension fondamentale de la programmation Java sera utile, car nous plongerons dans des extraits de code tout au long de ce didacticiel.
4. Configuration de l'IDE : vous pouvez utiliser n'importe quel IDE Java de votre choix, comme IntelliJ IDEA, Eclipse ou NetBeans, pour écrire et exécuter votre code. Assurez-vous simplement d'avoir configuré votre projet Java et ajouté la bibliothèque Aspose.PSD.

## Importer des packages
Avant de commencer à écrire notre code, nous devons importer les packages nécessaires depuis la bibliothèque Aspose.PSD. Voici comment procéder :
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
En important ces packages, nous aurons accès aux classes nécessaires au chargement, à la modification et à la sauvegarde de nos fichiers PSD.

Maintenant, décomposons le processus en étapes compréhensibles. Suivez-nous pendant le chargement d'un fichier PSD, l'ajustement des niveaux, puis l'enregistrement de vos modifications. 
## Étape 1 : Configurez vos chemins de fichiers
La première étape consiste à définir où se trouve notre fichier PSD et où nous souhaitons enregistrer la sortie modifiée. Vous pouvez personnaliser le chemin du répertoire en fonction de vos besoins.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
 Ici, remplacez`"Your Document Directory"`avec le chemin réel sur votre système où votre fichier PSD est stocké. Cela prépare le terrain pour tout ce que nous ferons ensuite.
## Étape 2 : Chargez le fichier PSD
 Maintenant, chargeons le fichier PSD en utilisant le`PsdImage` classe. Cette étape est essentielle car elle nous permet d'accéder et de manipuler les calques.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 Quand tu appelles`Image.load()` , il lira le fichier PSD et créera une instance de`PsdImage` avec lesquels vous pouvez travailler.
## Étape 3 : Parcourir les calques
Puisque nous souhaitons ajuster un calque de réglage de niveau, nous devrons parcourir chaque calque de notre fichier PSD. Cela nous aide à trouver le calque spécifique que nous souhaitons modifier.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // D'autres manipulations auront lieu ici...
    }
}
```
 Dans cette boucle,`instanceof LevelsLayer` vérifie si le calque actuel est un calque de réglage des niveaux. Si tel est le cas, nous pouvons procéder à la modification de ses propriétés.
## Étape 4 : Ajustez les paramètres du canal de niveau
Une fois que nous avons identifié la bonne couche, nous pouvons modifier ses niveaux d'entrée et de sortie. C'est ici que la magie opère ! Ajustez différents paramètres pour voir comment ils affectent l’image.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
Voici ce que fait chaque paramètre :
- Niveau des tons moyens d’entrée : Ajuste les tons moyens.
- Niveau d'ombre d'entrée : ajuste les zones les plus sombres de l'image.
- Niveau de surbrillance d’entrée : modifie les zones lumineuses de l’image.
- Niveau d'ombre de sortie : définit la façon dont les ombres sombres apparaîtront.
- Niveau de surbrillance de sortie : définit la manière dont les surbrillances lumineuses apparaîtront.
N'hésitez pas à expérimenter différentes valeurs !
## Étape 5 : Enregistrez le fichier PSD modifié
Maintenant que nous avons effectué nos ajustements, il est temps de sauvegarder le fichier PSD modifié. Cette étape est cruciale pour garantir que vos modifications sont appliquées et stockées.
```java
im.save(psdPathAfterChange);
```
 Vous pouvez maintenant trouver votre fichier PSD ajusté à l'adresse spécifiée`psdPathAfterChange`. 
## Conclusion
Vous venez d'apprendre comment ajouter un calque de réglage de niveau à un fichier PSD à l'aide d'Aspose.PSD pour Java ! En suivant ce guide, vous pouvez ajuster la qualité tonale de vos images sans effort, ouvrant ainsi la voie à une sortie plus dynamique et visuellement attrayante. N'oubliez pas que la pratique rend parfait, alors n'hésitez pas à peaufiner les ajustements et à explorer différents fichiers PSD pour voir les effets de vos modifications.
## FAQ
### Qu'est-ce qu'un calque de réglage de niveau ?
Un calque de réglage de niveau vous permet de corriger la plage tonale de vos images, en équilibrant les ombres, les tons moyens et les hautes lumières.
### Puis-je utiliser Aspose.PSD sans achat ?
Oui! Aspose propose un essai gratuit pour tester la bibliothèque avant de l'acheter.
### Où puis-je trouver de la documentation pour Aspose.PSD ?
 Vous pouvez trouver la documentation[ici](https://reference.aspose.com/psd/java/).
### Existe-t-il un support communautaire pour les produits Aspose ?
 Absolument! Vous pouvez poser des questions et obtenir de l'aide dans le[Forum Aspose](https://forum.aspose.com/c/psd/34).
### Comment puis-je obtenir une licence temporaire pour Aspose.PSD ?
 Vous pouvez demander une licence temporaire[ici](https://purchase.aspose.com/temporary-license/).