---
date: 2026-06-28
description: Apprenez à modifier les fichiers PSD avec Aspose.PSD for Java – récupérez
  et ajustez une zone de délimitation de texte dans un PSD. Guide étape par étape
  pour modifier un PSD de manière programmatique.
keywords:
- how to edit psd
- change photoshop text layer
- adjust text bound box
- retrieve text bound box
- update text bound box
linktitle: Ajuster la zone de délimitation du calque texte dans un PSD avec Java
schemas:
- author: Aspose
  dateModified: '2026-06-28'
  description: Learn how to edit PSD files with Aspose.PSD for Java – retrieve and
    adjust a text bound box in a PSD. Step‑by‑step guide for how to edit psd programmatically.
  headline: 'how to edit psd: Adjust Text Layer Bound Box in Java'
  type: TechArticle
- description: Learn how to edit PSD files with Aspose.PSD for Java – retrieve and
    adjust a text bound box in a PSD. Step‑by‑step guide for how to edit psd programmatically.
  name: 'how to edit psd: Adjust Text Layer Bound Box in Java'
  steps:
  - name: '**Java Development Kit (JDK)** – download from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – download from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Integrated Development Environment (IDE)** – Eclipse, IntelliJ IDEA,
      or NetBeans.'
    text: '**Integrated Development Environment (IDE)** – Eclipse, IntelliJ IDEA,
      or NetBeans.'
  - name: '**Aspose.PSD for Java Library** – obtain the latest version from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java Library** – obtain the latest version from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and arrays.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and arrays.'
  type: HowTo
- questions:
  - answer: Aspose.PSD is a robust library that lets developers create, edit, and
      convert Adobe Photoshop PSD files without needing Photoshop installed.
    question: What is Aspose.PSD?
  - answer: No, Aspose.PSD operates completely independently of Adobe Photoshop, making
      it ideal for server‑side automation.
    question: Do I need Photoshop installed to use Aspose.PSD?
  - answer: Yes, Aspose.PSD is available for .NET, Java, and Python, providing a consistent
      API across platforms.
    question: Can I use Aspose.PSD with other programming languages?
  - answer: You can get help on the official [Aspose Forum](https://forum.aspose.com/c/psd/34)
      where both staff and community members answer questions.
    question: Where can I find support for Aspose.PSD?
  - answer: Yes! Download a free trial from the [Aspose website](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
title: 'comment modifier un PSD : ajuster la zone de délimitation du calque texte
  en Java'
url: /fr/java/advanced-psd-layer-features-effects/adjust-text-layer-bound-box-psd/
weight: 25
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment modifier un PSD : ajuster la boîte englobante du calque texte en Java

## Introduction
Si vous vous demandez **comment modifier des fichiers PSD** de manière programmatique—en particulier lorsque vous devez **modifier les propriétés d'un calque texte Photoshop**—la bibliothèque Aspose.PSD pour Java brille de mille feux. Ce tutoriel vous guide à travers les étapes exactes pour **ajuster la boîte englobante du texte** et **récupérer les informations de la boîte englobante du texte** en utilisant **aspose psd java**. Que vous soyez un développeur chevronné ou que vous débutiez avec Java, vous trouverez des explications claires et conversationnelles qui rendent la manipulation de PSD simple et accessible. Plongeons‑y !

## Quick Answers
- **Quelle bibliothèque permet de modifier des fichiers PSD en Java ?** Aspose.PSD for Java.  
- **Puis‑je ajuster la boîte englobante d’un calque texte ?** Oui—utilisez `getTextBoundBox()` et `setSize()` pour la modifier.  
- **Dois‑je installer Photoshop ?** Non, Aspose.PSD fonctionne indépendamment d’Adobe Photoshop.  
- **Quels sont les prérequis principaux ?** JDK, un IDE et la bibliothèque Aspose.PSD for Java.  
- **Combien de temps prend l’implémentation de base ?** Environ 10‑15 minutes pour exécuter le code d’exemple.

## Qu’est‑ce que « how to edit psd » avec Aspose.PSD ?
Modifier un PSD de manière programmatique signifie ouvrir le fichier, accéder à ses calques et modifier des propriétés telles que la taille, la position ou le contenu texte—le tout sans lancer Photoshop. Aspose.PSD fournit une API riche qui abstrait le format PSD complexe, vous permettant de vous concentrer sur la logique dont vous avez besoin.

## Pourquoi utiliser Aspose.PSD pour Java ?
Aspose.PSD pour Java propose un ensemble complet de fonctionnalités qui rendent la manipulation de PSD simple et efficace. Il élimine le besoin de Photoshop, prend en charge tous les principaux types de calques, offre un traitement rapide même pour les gros fichiers, et fonctionne de manière cohérente sous Windows, Linux et macOS.

- **Pas besoin de Photoshop** – fonctionne sur n’importe quel serveur ou poste de travail.  
- **Prise en charge complète des calques** – les calques raster, vectoriels et texte peuvent être lus ou modifiés.  
- **Moteur haute performance** – traite des fichiers jusqu’à 500 Mo en moins de 2 secondes et gère des traitements par lots de 1 000 fichiers avec moins de 200 Mo de mémoire maximale.  
- **Multi‑plateforme** – fonctionne sous Windows, Linux ou macOS avec le même code.

## Prérequis
1. **Java Development Kit (JDK)** – téléchargez depuis le [site Web d'Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Environnement de développement intégré (IDE)** – Eclipse, IntelliJ IDEA ou NetBeans.  
3. **Bibliothèque Aspose.PSD pour Java** – obtenez la dernière version depuis la [page des versions d'Aspose](https://releases.aspose.com/psd/java/).  
4. **Connaissances de base en Java** – familiarité avec les classes, les objets et les tableaux.

Parfait ! Avec tout cela en place, commençons à coder.

## Importer les packages
La première étape consiste à importer les classes dont vous aurez besoin. Considérez cela comme la collecte de tous les outils avant de commencer un projet bricolage.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Size;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
```

Ces importations vous donnent accès à la gestion d’images, à la manipulation des tailles et à la classe `TextLayer` avec laquelle nous travaillerons.

## Étape 1 : Configurer vos chemins de fichiers
Spécifiez l’emplacement de votre fichier PSD. C’est comme préparer la scène avant le début du spectacle.

`File` objets permettent à Java de localiser les ressources sur le disque.  
`String` variables stockent le chemin absolu ou relatif vers le PSD source et le dossier de sortie.

```java
String dataDir = "Your Document Directory"; 
String sourceFileName = dataDir + "LayerWithText.psd";
```

Remplacez `"Your Document Directory"` par le chemin réel du dossier sur votre machine.

## Étape 2 : Charger le fichier PSD
Nous ouvrons maintenant le PSD afin de pouvoir interagir avec ses calques.

`Image.load` lit le fichier et renvoie un objet `PsdImage` prêt à être manipulé.  
`PsdImage` fournit des méthodes pour énumérer les calques, accéder aux métadonnées et enregistrer les modifications.

```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

La méthode `Image.load` lit le fichier et renvoie un objet `PsdImage` prêt à être manipulé.

## Étape 3 : Récupérer le calque texte
Identifiez le calque texte spécifique que vous souhaitez ajuster. Les calques sont indexés à partir de zéro, donc `[1]` fait référence au deuxième calque.

`TextLayer` est la classe concrète pour les calques de type texte ; elle expose des propriétés spécifiques au texte telles que la police, la couleur et la boîte englobante.

```java
TextLayer textLayer = (TextLayer) im.getLayers()[1];
```

Assurez‑vous de cibler le bon calque ; sinon vous pourriez modifier le mauvais contenu.

## Étape 4 : Vérifier la taille du calque
Avant de modifier quoi que ce soit, il est judicieux de vérifier la taille actuelle. Cela sert de contrôle de cohérence.

Les objets `Size` contiennent la largeur et la hauteur en pixels.  
`Assert` (ou un simple `if`) vous permet de valider les attentes pendant le développement.

```java
Size correctOpticalSize = new Size(127, 45);
Size opticalSize = textLayer.getSize();
Assert.areEqual(correctOpticalSize, opticalSize);
```

Si les tailles ne correspondent pas, l’`Assert` déclenchera une alerte, vous indiquant qu’il y a un problème.

## Étape 5 : Obtenir la taille de la boîte englobante
Nous récupérons maintenant la **boîte englobante du texte** — le rectangle qui entoure le texte rendu.

`getTextBoundBox()` renvoie une instance `Size` décrivant le rectangle exact que le texte occupe après le rendu, en tenant compte des métriques de police et de l’interligne.

```java
Size correctBoundBox = new Size(172, 62);
Size boundBox = textLayer.getTextBoundBox();
Assert.areEqual(correctBoundBox, boundBox);
```

Vous pouvez comparer cette taille à vos dimensions attendues ou l’utiliser pour calculer d’autres ajustements.

## Comment récupérer la boîte englobante du texte avec Aspose.PSD Java ?
Pour récupérer la boîte englobante du texte, chargez d’abord le fichier PSD avec `Image.load` et obtenez l’instance `PsdImage`. Ensuite, localisez le `TextLayer` cible en parcourant `psdImage.getLayers()` ou par indice. Appelez la méthode `getTextBoundBox()` sur ce calque ; elle renvoie un objet `Size` avec la largeur et la hauteur exactes en pixels, que vous pouvez enregistrer ou utiliser pour d’autres calculs.

## Comment ajuster la boîte englobante du texte avec Aspose.PSD Java ?
Une fois que vous avez la boîte englobante actuelle, vous pouvez la modifier en appelant `setSize(new Size(width, height))` directement sur le `TextLayer`, en fournissant les valeurs de largeur et de hauteur souhaitées. Vous pouvez également appliquer une matrice de transformation avec la méthode `transform()` pour mettre à l’échelle ou repositionner le texte avant de rasteriser le calque. Les deux approches mettent à jour la disposition visuelle pour répondre à vos exigences de conception.

## Cas d’utilisation courants
- **Génération dynamique de miniatures** – ajustez les limites du texte avant de rasteriser un aperçu.  
- **Branding automatisé** – remplacez programmétiquement le texte du logo et assurez‑vous qu’il s’adapte aux contraintes de conception.  
- **Traitement par lots** – parcourez de nombreux fichiers PSD pour standardiser les tailles des calques texte sur une gamme de produits.

## Dépannage et astuces
- **Indice de calque incorrect** – vérifiez l’ordre des calques dans Photoshop ; l’indice peut différer de ce que vous attendez.  
- **Problèmes de licence** – une version d’essai peut limiter certaines opérations ; assurez‑vous de disposer d’une licence valide pour la production.  
- **Tailles inattendues** – les réglages DPI peuvent affecter les calculs de taille ; vérifiez la résolution du PSD si les valeurs semblent erronées.  
- **Astuce de performance** – réutilisez la même instance `PsdImage` lors du traitement de plusieurs calques afin de minimiser les allocations de mémoire.

## Conclusion
Vous avez maintenant appris **comment modifier des fichiers PSD** en récupérant et en ajustant la boîte englobante d’un calque texte à l’aide de **aspose psd java**. En quelques lignes de code, vous pouvez charger un PSD, cibler un calque spécifique, vérifier ses dimensions et garantir que le texte s’ajuste parfaitement. Pour aller plus loin—comme modifier le contenu du texte, appliquer des effets ou exporter vers d’autres formats—consultez la documentation complète d’Aspose.PSD [ici](https://reference.aspose.com/psd/java/).

## Questions fréquentes
**Q : Qu’est‑ce qu’Aspose.PSD ?**  
R : Aspose.PSD est une bibliothèque robuste qui permet aux développeurs de créer, modifier et convertir des fichiers Adobe Photoshop PSD sans nécessiter l’installation de Photoshop.

**Q : Dois‑je installer Photoshop pour utiliser Aspose.PSD ?**  
R : Non, Aspose.PSD fonctionne complètement indépendamment d’Adobe Photoshop, ce qui le rend idéal pour l’automatisation côté serveur.

**Q : Puis‑je utiliser Aspose.PSD avec d’autres langages de programmation ?**  
R : Oui, Aspose.PSD est disponible pour .NET, Java et Python, offrant une API cohérente sur toutes les plateformes.

**Q : Où puis‑je obtenir du support pour Aspose.PSD ?**  
R : Vous pouvez obtenir de l’aide sur le [Forum Aspose](https://forum.aspose.com/c/psd/34) officiel où le personnel et les membres de la communauté répondent aux questions.

**Q : Existe‑t‑il une version d’essai disponible pour Aspose.PSD ?**  
R : Oui ! Téléchargez une version d’essai gratuite depuis le [site Web d'Aspose](https://releases.aspose.com/).

**Dernière mise à jour** : 2026-06-28  
**Testé avec** : Aspose.PSD for Java (latest)  
**Auteur** : Aspose

## Tutoriels associés
- [Comment modifier les calques texte PSD avec Aspose.PSD pour Java](/psd/java/advanced-psd-layer-features-effects/update-text-layer-psd-files/)
- [Ajouter un calque texte à l’exécution dans les fichiers PSD avec Java](/psd/java/modifying-converting-psd-images/add-text-layer-runtime-psd-files/)
- [Rendu d’un calque texte pivoté dans les fichiers PSD avec Java](/psd/java/psd-layer-management-effects/render-rotated-text-layer-psd/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}