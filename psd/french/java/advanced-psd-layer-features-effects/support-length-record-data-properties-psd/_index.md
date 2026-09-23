---
date: 2026-09-23
description: Apprenez comment modifier les formes vectorielles PSD et traiter par
  lots les fichiers PSD en utilisant Aspose.PSD for Java. Étapes détaillées, conseils
  et espaces réservés de code pour une solution complète.
keywords:
- modify psd vector shapes
- batch process psd files
- Aspose.PSD Java
- vector shape editing
lastmod: 2026-09-23
linktitle: Prise en charge de Length Record Data Properties dans PSD - Java
og_description: Apprenez comment modifier les formes vectorielles PSD et traiter par
  lots les fichiers PSD en utilisant Aspose.PSD for Java. Guide étape par étape avec
  espaces réservés de code et conseils d'experts.
og_image_alt: Guide showing how to edit vector shapes in PSD files using Aspose.PSD
  for Java
og_title: Modifier les formes vectorielles PSD avec Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  headline: Modify PSD vector shapes with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  name: Modify PSD vector shapes with Aspose.PSD for Java
  steps:
  - name: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
    text: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
  - name: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
  - name: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
    text: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
  type: HowTo
- questions:
  - answer: The `VsmsResource` will be absent, so `resource` stays `null`. Add a check
      and skip the modification step or inform the user.
    question: How do I handle a PSD that contains no vector shape layers?
  - answer: Yes, `LengthRecord` provides setters for fill, stroke, and opacity. See
      the API docs for the full list.
    question: Can I change other properties like fill color or stroke width?
  - answer: Absolutely. Wrap the code inside a loop that iterates over a directory
      of PSD files, adjusting the input and output paths each time.
    question: Is it possible to batch‑process multiple PSD files?
  - answer: '`Image.load` handles file streams automatically, but if you load from
      an `InputStream`, remember to close it after use.'
    question: Do I need to close streams manually when loading from a file path?
  - answer: The `LengthRecord` and `PathOperations` classes have been available since
      Aspose.PSD 20.10. Using the latest version (24.11 at time of writing) is recommended.
    question: What version of Aspose.PSD is required for these APIs?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- modify psd vector shapes
- Aspose.PSD
- Java image processing
- batch PSD processing
title: Modifier les formes vectorielles PSD avec Aspose.PSD for Java
url: /fr/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Modifier les formes vectorielles PSD avec Aspose.PSD pour Java

## Introduction
If you need to **modify PSD vector shapes** programmatically, Aspose.PSD for Java gives you full control over Photoshop files directly from your Java code. This tutorial walks you through supporting length record properties—an essential step when editing vector shape layers. By the end you’ll be able to open a PSD, adjust its vector shape data, and save the updated file without ever launching Photoshop.

## Réponses rapides
- **Que signifie « modifier les formes vectorielles PSD » ?** Ajuster la géométrie, les opérations de chemin ou d'autres attributs des calques basés sur des vecteurs à l'intérieur d'un fichier PSD.  
- **Quelle bibliothèque gère cela ?** Aspose.PSD for Java.  
- **Ai-je besoin d'une licence ?** Un essai gratuit fonctionne pour l'évaluation ; une licence commerciale est requise pour la production.  
- **Combien de temps prend l'implémentation ?** Environ 10‑15 minutes pour un script de modification de forme basique.  
- **Quels sont les prérequis principaux ?** Java JDK, Aspose.PSD for Java et un fichier PSD d'exemple.

## Qu’est-ce que « prendre en charge les propriétés d’enregistrement de longueur » ?
Prendre en charge les propriétés d'enregistrement de longueur signifie accéder et mettre à jour les objets `LengthRecord` qui décrivent chaque tracé vectoriel à l'intérieur d'un PSD. Ces enregistrements stockent des informations telles que la longueur du tracé, son type et la façon dont il se joint à d'autres tracés. Les modifier vous permet de contrôler comment les formes se combinent, s'intersectent ou se soustraient les unes des autres, permettant une édition vectorielle précise.

## Pourquoi utiliser Aspose.PSD pour Java pour prendre en charge les propriétés d’enregistrement de longueur ?
Chargez votre PSD, modifiez les données vectorielles et enregistrez—tout cela sans Photoshop. Aspose.PSD traite des PSD de plusieurs centaines de pages en moins de 2 secondes sur un serveur typique, propose plus de 150 classes (dont plus de 30 types liés aux vecteurs) et fonctionne sous Windows, Linux ou macOS avec n'importe quel JDK 11+. Cette bibliothèque axée sur la performance élimine le besoin de logiciels de bureau coûteux.

## Prérequis
1. **Java Development Kit (JDK)** – téléchargez depuis [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) ou utilisez votre gestionnaire de paquets préféré.  
2. **Aspose.PSD for Java** – obtenez le dernier JAR depuis la [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse ou tout éditeur compatible Java.  
4. **Un fichier PSD** – créez‑en un dans Photoshop ou récupérez un PSD d'exemple pour expérimenter.  
5. **Connaissances de base en Java** – familiarité avec les classes, les objets et la gestion des exceptions.

## Importer les packages
Les instructions d'importation apportent les classes principales d'Aspose.PSD dans le scope, telles que `PsdImage`, `VsmsResource` et `LengthRecord`.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Étape 1 : Configurer vos répertoires source et de sortie
Définissez où se trouve le PSD original et où le fichier modifié sera écrit.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Étape 2 : Charger le fichier PSD
Utilisez `Image.load` pour ouvrir le fichier et le convertir en `PsdImage` afin d'accéder aux fonctionnalités spécifiques aux PSD.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Étape 3 : Localiser la ressource Vsms dans le calque
`VsmsResource` est le conteneur qui stocke les données de forme vectorielle d'un calque. Parcourez les ressources du deuxième calque pour le trouver.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Étape 4 : Accéder aux enregistrements de longueur
`LengthRecord` représente un tracé vectoriel distinct. Récupérez les enregistrements que vous souhaitez modifier.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Étape 5 : Modifier les propriétés d'opération de chemin
`PathOperations` définit comment les formes individuelles interagissent (par ex., exclusion, intersection, soustraction). Modifier ces valeurs met à jour la composition visuelle du calque vectoriel.

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Étape 6 : Enregistrer le fichier PSD modifié
Enregistrez vos modifications dans un nouveau fichier.

```java
psdImage.save(outPsdFilePath);
```

## Étape 7 : Nettoyer les ressources
Libérez l'instance `PsdImage` pour libérer la mémoire et éviter les fuites de ressources.

```java
psdImage.dispose();
```

## Comment traiter par lots les fichiers PSD avec prise en charge des propriétés d'enregistrement de longueur
Enveloppez le flux de travail d'un seul fichier dans une boucle qui parcourt un répertoire de PSD, en mettant à jour `inPsdFilePath` et `outPsdFilePath` pour chaque fichier. Cette approche vous permet d'appliquer des ajustements de forme vectorielle identiques à des dizaines ou des centaines de fichiers en quelques minutes, idéal pour les pipelines d'actifs automatisés.

## Pièges courants et astuces
- **Vérifications de null** – vérifiez toujours que `resource` n'est pas `null` avant d'accéder à ses membres.  
- **Limites d'index de chemin** – assurez‑vous que les indices que vous utilisez (par ex., `[2]`, `[7]`, `[11]`) existent pour le PSD spécifique que vous éditez.  
- **Licence** – exécuter sans licence valide ajoute un filigrane au PSD enregistré.  

## Conclusion
Vous disposez maintenant d'un exemple complet, de bout en bout, sur la façon de **modifier les formes vectorielles PSD** en prenant en charge les propriétés d'enregistrement de longueur avec Aspose.PSD pour Java. Que vous automatisiez un pipeline d'actifs ou que vous construisiez un outil de conception personnalisé, ces API vous offrent la flexibilité de manipuler les calques vectoriels sans travail manuel dans Photoshop. Expérimentez avec d'autres valeurs de `PathOperations` ou combinez plusieurs modifications de `LengthRecord` pour créer des formes complexes.

## Questions fréquemment posées

**Q : Comment gérer un PSD qui ne contient aucune couche de forme vectorielle ?**  
R : Le `VsmsResource` sera absent, donc `resource` reste `null`. Ajoutez une vérification et sautez l'étape de modification ou informez l'utilisateur.

**Q : Puis‑je modifier d'autres propriétés comme la couleur de remplissage ou la largeur du trait ?**  
R : Oui, `LengthRecord` fournit des setters pour le remplissage, le trait et l'opacité. Consultez la documentation de l'API pour la liste complète.

**Q : Est‑il possible de traiter par lots plusieurs fichiers PSD ?**  
R : Absolument. Enveloppez le code dans une boucle qui parcourt un répertoire de fichiers PSD, en ajustant les chemins d'entrée et de sortie à chaque fois.

**Q : Dois‑je fermer les flux manuellement lors du chargement depuis un chemin de fichier ?**  
R : `Image.load` gère les flux de fichiers automatiquement, mais si vous chargez depuis un `InputStream`, pensez à le fermer après utilisation.

**Q : Quelle version d'Aspose.PSD est requise pour ces API ?**  
R : Les classes `LengthRecord` et `PathOperations` sont disponibles depuis Aspose.PSD 20.10. Il est recommandé d'utiliser la dernière version (24.11 au moment de la rédaction).

---

**Dernière mise à jour :** 2026-09-23  
**Testé avec :** Aspose.PSD for Java 24.11  
**Auteur :** Aspose

## Tutoriels associés

- [Convertir PSD en PNG et créer un masque vectoriel Java – Ressource Vmsk dans les fichiers PSD](/psd/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/)
- [Convertir PSD en PNG avec prise en charge du masque de calque en utilisant Aspose.PSD pour Java](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [Ajouter la prise en charge des calques aux fichiers PSD](/psd/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}