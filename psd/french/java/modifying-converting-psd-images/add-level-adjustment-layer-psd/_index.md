---
date: 2026-03-07
description: Apprenez à ajuster les niveaux en ajoutant un calque d’ajustement de
  niveaux dans les fichiers PSD à l’aide d’Aspose.PSD pour Java. Maîtrisez rapidement
  les réglages tonaux.
linktitle: Add Level Adjustment Layer in PSD
second_title: Aspose.PSD Java API
title: Comment ajuster les niveaux – Ajouter un calque de réglage des niveaux dans
  PSD
url: /fr/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajouter un calque de réglage des niveaux dans PSD

## Introduction
Si vous cherchez **comment ajuster les niveaux** dans vos documents Photoshop, le calque de réglage des niveaux est l'outil idéal. Il vous permet d'ajuster finement les ombres, les tons moyens et les hautes lumières sans modifier de façon permanente les pixels d'origine. Dans ce tutoriel, nous allons vous montrer comment ajouter un calque de réglage des niveaux à un fichier PSD en utilisant Aspose.PSD pour Java, afin d'obtenir un contrôle tonal de niveau professionnel en quelques étapes seulement.

## Réponses rapides
- **Que fait un calque de réglage des niveaux ?** Il modifie la plage tonale d'une image de manière non destructive.  
- **Quelle bibliothèque est utilisée ?** Aspose.PSD pour Java.  
- **Ai‑je besoin d'une licence ?** Un essai gratuit suffit pour le développement ; une licence est requise pour la production.  
- **Combien de temps prend l'implémentation ?** Environ 10‑15 minutes pour un réglage de base.  
- **Puis‑je ajuster plusieurs canaux ?** Oui, vous pouvez définir les niveaux d'entrée/sortie pour chaque canal de couleur individuellement.

## Qu'est‑ce qu'un calque de réglage des niveaux ?
Un calque de réglage des niveaux vous permet de corriger l'équilibre tonal d'une image en ajustant les ombres d'entrée, les tons moyens et les hautes lumières ainsi que les niveaux de sortie. Parce qu'il vit sur son propre calque, vous pouvez basculer sa visibilité ou le supprimer sans affecter le contenu sous‑jacent.

## Pourquoi ajouter un calque de réglage des niveaux avec Aspose.PSD ?
- **Automatisation :** Intégrer les ajustements de niveaux dans les pipelines de traitement par lots.  
- **Multiplateforme :** Fonctionne sur tout système d'exploitation supportant Java.  
- **Précision :** Accéder aux paramètres de chaque canal par programme pour des résultats exactes.  

## Prérequis
1. Java Development Kit (JDK). Si vous ne l'avez pas, téléchargez-le depuis le [site d'Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) ou utilisez OpenJDK.  
2. Bibliothèque Aspose.PSD pour Java – obtenez le dernier JAR via ce [lien de téléchargement](https://releases.aspose.com/psd/java/).  
3. Connaissances de base en programmation Java.  
4. Un IDE tel qu'IntelliJ IDEA, Eclipse ou NetBeans avec le JAR Aspose.PSD ajouté au classpath du projet.

## Importer les packages
Avant de commencer à écrire notre code, nous devons importer les packages nécessaires de la bibliothèque Aspose.PSD. Voici comment procéder :
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
Ces imports nous donnent accès aux classes pour charger les fichiers PSD, travailler avec les calques de réglage des niveaux et manipuler les paramètres de chaque canal.

## Comment ajuster les niveaux dans un fichier PSD
Ci‑dessous se trouve un guide étape par étape qui vous montre exactement **comment ajuster les niveaux** de façon programmatique.

### Étape 1 : Configurer vos chemins de fichiers
Définissez où se trouve le PSD source et où le fichier modifié sera enregistré.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
Remplacez `"Your Document Directory"` par le dossier réel sur votre machine.

### Étape 2 : Charger le fichier PSD
Créez une instance `PsdImage` à partir du fichier source.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
Vous avez maintenant un accès complet à tous les calques du PSD.

### Étape 3 : Parcourir les calques
Trouvez le calque de réglage des niveaux que vous souhaitez modifier.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Further manipulation will go here...
    }
}
```
La vérification `instanceof LevelsLayer` garantit que nous ne travaillons qu'avec des calques de réglage des niveaux.

### Étape 4 : Ajuster les paramètres du canal de niveau
Modifiez les valeurs d'entrée et de sortie pour le canal sélectionné.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
- **Niveau moyen d'entrée :** Décale la gamme des tons moyens.  
- **Niveau d'ombre d'entrée :** Assombrit ou éclaircit les ombres.  
- **Niveau de surbrillance d'entrée :** Contrôle les parties les plus claires.  
- **Niveaux de sortie ombre/surbrillance :** Définissent la plage de sortie finale.

N'hésitez pas à expérimenter avec différentes valeurs pour voir comment elles affectent l'image.

### Étape 5 : Enregistrer le fichier PSD modifié
Enregistrez vos modifications dans un nouveau fichier.
```java
im.save(psdPathAfterChange);
```
Vous trouverez le PSD mis à jour à l'emplacement que vous avez spécifié dans `psdPathAfterChange`.

## Problèmes courants et solutions
- **Fichier non trouvé :** Vérifiez que `dataDir` pointe vers le bon dossier et que le PSD source existe.  
- **ClassCastException :** Assurez‑vous que le fichier chargé est bien un PSD ; d'autres formats nécessitent des classes différentes.  
- **Erreurs de licence :** Utilisez une licence Aspose.PSD valide pour les builds de production ; l'essai fonctionne pour le développement.

## Conclusion
Vous savez maintenant **comment ajuster les niveaux** en ajoutant et en configurant un calque de réglage des niveaux dans un fichier PSD avec Aspose.PSD pour Java. Cette technique vous offre un contrôle précis sur l'équilibre tonal tout en gardant votre flux de travail entièrement automatisé. Continuez à expérimenter avec différentes valeurs de canal et explorez le traitement par lots pour appliquer les mêmes ajustements à plusieurs images.

## Questions fréquentes

**Q : Qu'est‑ce qu'un calque de réglage des niveaux ?**  
R : C’est un calque non destructif qui vous permet de modifier la plage tonale (ombres, tons moyens, hautes lumières) d’une image.

**Q : Puis‑je utiliser Aspose.PSD sans acheter de licence ?**  
R : Oui, vous pouvez évaluer la bibliothèque avec un essai gratuit, mais une licence est requise pour le déploiement commercial.

**Q : Où puis‑je trouver la documentation d'Aspose.PSD ?**  
R : Vous pouvez trouver la documentation [ici](https://reference.aspose.com/psd/java/).

**Q : Existe‑t‑il un support communautaire pour les produits Aspose ?**  
R : Absolument ! Vous pouvez poser des questions et obtenir de l'aide sur le [forum Aspose](https://forum.aspose.com/c/psd/34).

**Q : Comment obtenir une licence temporaire pour Aspose.PSD ?**  
R : Vous pouvez demander une licence temporaire [ici](https://purchase.aspose.com/temporary-license/).

---

**Dernière mise à jour :** 2026-03-07  
**Testé avec :** Aspose.PSD dernière version (Java)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}