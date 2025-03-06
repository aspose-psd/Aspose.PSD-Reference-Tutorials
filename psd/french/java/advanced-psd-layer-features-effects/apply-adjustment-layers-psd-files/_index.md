---
title: Appliquer des calques de réglage dans des fichiers PSD à l'aide de Java
linktitle: Appliquer des calques de réglage dans des fichiers PSD à l'aide de Java
second_title: API Java Aspose.PSD
description: Apprenez à appliquer des calques de réglage dans les fichiers PSD à l'aide d'Aspose.PSD pour Java dans ce guide complet étape par étape pour les développeurs.
weight: 15
url: /fr/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Appliquer des calques de réglage dans des fichiers PSD à l'aide de Java

## Introduction
Êtes-vous un développeur Java cherchant à améliorer les images stockées dans des fichiers PSD ? Si c'est le cas, vous êtes au bon endroit ! Dans cet article, nous verrons comment appliquer des calques de réglage dans les fichiers PSD à l'aide de la bibliothèque Aspose.PSD pour Java. Que vous travailliez sur un projet personnel ou sur une application professionnelle, comprendre comment manipuler les fichiers PSD peut augmenter considérablement les capacités de votre logiciel. 

## Conditions préalables
Avant de passer au code et de commencer à appliquer ces calques de réglage, vous aurez besoin de quelques prérequis :
1. Kit de développement Java (JDK) : assurez-vous que JDK est installé sur votre ordinateur. Vous pouvez le télécharger depuis[Le site d'Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Bibliothèque Aspose.PSD : si vous ne l'avez pas déjà fait, vous devrez télécharger la bibliothèque Aspose.PSD pour Java. Vous pouvez le trouver[ici](https://releases.aspose.com/psd/java/).
3. Environnement de développement : configurez un environnement de développement intégré (IDE) Java tel qu'IntelliJ IDEA ou Eclipse dans lequel vous écrirez et exécuterez votre code.
4. Familiarité de base avec Java : Une compréhension générale de la programmation Java vous aidera à suivre le cours en douceur.
5. Fichiers PSD : ayez quelques fichiers PSD à portée de main à des fins de test. Vous pouvez en créer à l'aide d'Adobe Photoshop ou télécharger des exemples de fichiers sur Internet.
## Importer des packages
Avant de commencer le codage, clarifions les packages que nous devons importer. Aspose.PSD nous permet de travailler avec des fichiers Photoshop de différentes manières, alors prenons les classes nécessaires pour gérer les images PSD et les calques de réglage.
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.AdjustmentLayer;
```
Maintenant que nos packages sont en place, décomposons les exemples étape par étape !
## Étape 1 : Chargez le fichier PSD
La première étape de notre voyage consiste à charger le fichier PSD. C'est le fichier avec lequel nous allons travailler pour appliquer nos calques de réglage.
```java
String dataDir = "Your Document Directory";
String sourceFileName1 = dataDir + "ChannelMixerAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName1);
```
 Dans cet extrait, nous définissons le répertoire où se trouvent nos fichiers PSD et chargeons le fichier spécifique que nous souhaitons manipuler. Assurez-vous de remplacer`"Your Document Directory"` avec le chemin réel de vos fichiers PSD sur votre machine.
## Étape 2 : Itérer sur les calques
Maintenant que nous avons chargé le fichier PSD, nous allons parcourir ses calques pour trouver nos calques de réglage.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof AdjustmentLayer) {
        AdjustmentLayer adjustmentLayer = (AdjustmentLayer) im.getLayers()[i];
        
        if (adjustmentLayer != null) {
            adjustmentLayer.mergeLayerTo(im.getLayers()[0]);
        }
    }
}
```
 Au cours de cette étape, nous parcourons chaque couche du fichier PSD pour identifier celles qui appartiennent au`AdjustmentLayer` taper. Si nous en trouvons un, nous le fusionnons avec le calque de base, qui est généralement le premier calque (`im.getLayers()[0]`). Ce processus de fusion applique efficacement les ajustements à notre image. 
## Étape 3 : Enregistrez le fichier PSD modifié
Après avoir modifié les calques, il est crucial de sauvegarder les modifications que nous avons apportées. Faisons cela à l'étape suivante.
```java
String exportPath1 = dataDir + "ChannelMixerAdjustmentLayerChanged.psd";
im.save(exportPath1);
```
 Ici, nous spécifions le chemin d'exportation de notre fichier PSD modifié et appelons le`save()` méthode pour écrire nos modifications sur le disque.
## Étape 4 : Couche de réglage des niveaux
Répétons le processus pour un autre type de calque de réglage : le calque de réglage Niveaux. 
### Charger le calque de réglage des niveaux PSD
```java
String sourceFileName2 = dataDir + "LevelsAdjustmentLayerRgb.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName2);
```
Comme précédemment, nous chargeons le fichier PSD contenant notre calque de réglage des niveaux. 
### Parcourir les couches de niveaux
Ensuite, nous allons parcourir à nouveau les calques, comme nous l'avons fait précédemment, mais nous travaillons maintenant avec un autre fichier PSD.
```java
for (int i = 0; i < img.getLayers().length; i++) {
    if (img.getLayers()[i] instanceof AdjustmentLayer) {
        AdjustmentLayer adjustmentLayer = (AdjustmentLayer) img.getLayers()[i];
        
        if (adjustmentLayer != null) {
            adjustmentLayer.mergeLayerTo(img.getLayers()[0]);
        }
    }
}
```
Ce code agit de la même manière que l'itération précédente ; il recherche les calques de réglage dans le fichier PSD actuel, nous permettant d'appliquer tous les réglages disponibles.
## Enregistrer le calque de réglage des niveaux PSD
Enfin, nous enregistrerons ce nouveau fichier après avoir appliqué les ajustements.
```java
String exportPath2 = dataDir + "LevelsAdjustmentLayerRgbChanged.psd";
img.save(exportPath2);
```
Maintenant, nous avons traité avec succès le calque de réglage des niveaux !
## Conclusion
Félicitations! Vous venez d'apprendre à appliquer des calques de réglage dans des fichiers PSD à l'aide de Java et de la bibliothèque Aspose.PSD. Que vous ajustiez les couleurs ou les niveaux, vous disposez désormais des compétences de base nécessaires pour manipuler les fichiers PSD par programmation.
L'utilisation d'Aspose.PSD peut rationaliser considérablement les flux de travail dans l'édition d'images, permettant une automatisation et une personnalisation d'une manière que les outils traditionnels ne pourraient pas faire. N'hésitez pas à explorer davantage la bibliothèque et à expérimenter différents types de calques pour voir quelles possibilités créatives existent.
## FAQ
### Qu'est-ce que la bibliothèque Aspose.PSD ?
Aspose.PSD est une bibliothèque qui permet aux développeurs de charger, manipuler et enregistrer des fichiers Photoshop PSD dans des applications Java.
### Puis-je utiliser Aspose.PSD gratuitement ?
 Oui! Aspose propose un essai gratuit pour vous permettre d'explorer leur bibliothèque. Vous pouvez vous inscrire[ici](https://releases.aspose.com/).
### Dois-je installer Photoshop pour utiliser Aspose.PSD ?
Non, vous n'avez pas besoin de Photoshop. Aspose.PSD fonctionne indépendamment pour manipuler les fichiers PSD par programme.
### Où puis-je trouver de la documentation pour Aspose.PSD ?
Vous pouvez visiter la page de documentation[ici](https://reference.aspose.com/psd/java/) pour explorer les fonctionnalités, les classes et les méthodes.
### Comment puis-je obtenir de l'aide pour les produits Aspose ?
 Vous pouvez accéder à l'assistance via le[Forum Aspose](https://forum.aspose.com/c/psd/34) où vous pouvez poser des questions et trouver des solutions.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
