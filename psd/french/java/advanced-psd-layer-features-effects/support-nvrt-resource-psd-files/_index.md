---
date: 2026-09-23
description: Apprenez à charger des fichiers PSD, lire les calques et extraire la
  ressource Nvrt des calques de réglage d’inversion à l’aide d’Aspose.PSD pour Java,
  ainsi que le traitement par lots des fichiers PSD.
keywords:
- how to load psd
- batch process psd files
- invert adjustment layer java
- nvrt resource extraction
- Aspose.PSD
lastmod: 2026-09-23
linktitle: Prise en charge de la ressource Nvrt dans les fichiers PSD avec Java
og_description: Apprenez à charger des fichiers PSD, lire les calques et extraire
  la ressource Nvrt des calques de réglage d’inversion à l’aide d’Aspose.PSD pour
  Java. Découvrez également comment traiter efficacement les fichiers PSD par lots.
og_image_alt: 'Developer guide: Load PSD and extract Nvrt resource using Aspose.PSD
  for Java'
og_title: Comment charger un PSD et extraire la ressource Nvrt avec Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to load PSD files, read layers, and extract the Nvrt resource
    from invert adjustment layers using Aspose.PSD for Java, plus batch process PSD
    files.
  headline: How to load PSD and extract Nvrt resource with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Aspose.PSD for Java is a library that enables developers to create, edit,
      convert, and render PSD files directly from Java code.
    question: What is Aspose.PSD for Java?
  - answer: Yes, a commercial license is required for production use. You can explore
      purchasing options [purchase Aspose.PSD](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD in commercial products?
  - answer: 'The complete documentation is available here: [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).'
    question: Where can I find the documentation for Aspose.PSD?
  - answer: Absolutely! You can get a free trial of Aspose.PSD for Java [download
      free trial](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: 'You can ask questions and get support on the Aspose forum: [Aspose Support](https://forum.aspose.com/c/psd/34).'
    question: How can I get support for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- load PSD
- Aspose.PSD
- Java image processing
- invert adjustment layer
- Nvrt resource
title: Comment charger un PSD et extraire la ressource Nvrt avec Aspose.PSD
url: /fr/java/advanced-psd-layer-features-effects/support-nvrt-resource-psd-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment charger un PSD et extraire la ressource Nvrt des calques de réglage d'inversion à l'aide de Java

Lorsque vous devez **how to load PSD** des fichiers de manière programmatique et travailler avec un **calque de réglage d'inversion**, l'écosystème Java—en particulier la bibliothèque Aspose.PSD—vous offre un contrôle total. Que vous construisiez un éditeur graphique, automatisiez un pipeline de conception ou extrayiez des ressources de documents Photoshop, maîtriser la manipulation des PSD est essentiel pour les flux de travail modernes de traitement d'images.

## Réponses rapides
- **Quelle bibliothèque gère les fichiers PSD en Java ?** Aspose.PSD for Java  
- **Puis-je lire les calques PSD ?** Oui, l'API fournit un accès complet aux structures de calques  
- **Une licence est‑elle requise pour la production ?** Oui, une licence commerciale est nécessaire  
- **Quelle version du JDK est prise en charge ?** Java 8 et supérieur  
- **Où puis‑je télécharger la bibliothèque ?** Depuis la page officielle de téléchargement d'Aspose  

## Qu'est‑ce qu'un calque de réglage d'inversion ?
Un calque de réglage d'inversion inverse les valeurs de couleur de chaque pixel en dessous, créant un effet négatif photographique. Avec Aspose.PSD, vous pouvez détecter, lire et manipuler ce calque sans rasteriser l'image, ce qui est idéal pour les pipelines de traitement par lots nécessitant une correction colorimétrique cohérente sur de nombreux fichiers.

## Pourquoi utiliser le calque de réglage d'inversion avec Aspose.PSD ?
Aspose.PSD prend en charge **plus de 30 formats d'entrée et de sortie** et peut traiter des fichiers jusqu'à **2 Go** sans charger le document complet en mémoire, vous offrant un contrôle précis et efficace en mémoire sur l'inversion des couleurs. La bibliothèque expose également les données de réglage, vous permettant d'automatiser la suppression ou la modification de l'effet d'inversion sur de vastes bibliothèques de conception.

## Comment charger un fichier Photoshop et traiter des PSD en lot
Chargez un PSD une fois, inspectez ses calques, puis répétez la même logique dans une boucle pour **traiter des PSD en lot** efficacement. En instanciant un nouveau `PsdImage` pour chaque fichier et en le libérant rapidement, vous maintenez une faible utilisation de la mémoire et un débit élevé pour les opérations en masse.

## Prérequis
Avant de commencer à coder, assurez‑vous d'avoir les éléments suivants :

- **Java Development Kit (JDK)** installé (Java 8+ recommandé)  
- **Un IDE** tel qu'IntelliJ IDEA, Eclipse ou VS Code  
- **Bibliothèque Aspose.PSD for Java** – téléchargez‑la depuis le site officiel : [Download Aspose.PSD for Java](https://releases.aspose.com/psd/java/)  
- **Connaissances de base en Java** (classes, objets, gestion des exceptions)  

## Importer les packages
La classe `PsdImage` est l'objet de haut niveau d'Aspose.PSD qui représente un document Photoshop unique en mémoire, exposant les calques et les ressources pour la manipulation.  

```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.InvertAdjustmentLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.NvrtResource;
```

## Pourquoi lire les calques PSD ?
Lire les calques PSD vous donne un aperçu de la structure du document, vous permettant d'isoler des ressources individuelles, de comprendre quels réglages ont été appliqués et de réutiliser des composants dans d'autres projets ou formats. Cette visibilité est essentielle pour l'automatisation, l'extraction de ressources et le maintien de la cohérence du design à travers plusieurs fichiers.

- Extraire des ressources individuelles (p. ex., icônes, masques) pour réutilisation  
- Identifier les calques contenant un calque de réglage d'inversion afin de comprendre les modifications d'image  
- Automatiser le traitement par lots des fichiers de conception  

## Étape 1 : spécifiez votre répertoire source
Définissez le dossier qui contient le PSD avec lequel vous souhaitez travailler.

```java
String sourceDir = "Your Source Directory";
String inPsdFilePath = sourceDir + "InvertAdjustmentLayer.psd";
```

Remplacez `"Your Source Directory"` par le chemin réel sur votre machine.

## Étape 2 : charger le fichier PSD
`Image.load()` charge un fichier dans une instance `PsdImage`, analysant la structure du PSD afin que vous puissiez inspecter les calques, les ressources et les données de réglage.

```java
PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);
```

La méthode ouvre le fichier et le prépare à l'inspection.

## Étape 3 : initialiser la variable de ressource Nvrt
La classe `NvrtResource` représente les données de réglage d'inversion stockées dans un fichier Photoshop.  

```java
NvrtResource nvrtResource = null;
```

## Étape 4 : rechercher le calque de réglage d'inversion
`InvertAdjustmentLayer` est le type de calque spécifique qui applique l'effet de couleur négative. En parcourant la collection de calques, vous pouvez localiser ce calque puis récupérer son `NvrtResource` associé.

```java
try {
    for (Layer layer : psdImage.getLayers()) {
        if (layer instanceof InvertAdjustmentLayer) {
            for (LayerResource layerResource : layer.getResources()) {
                if (layerResource instanceof NvrtResource) {
                    // The NvrtResource is found
                    nvrtResource = (NvrtResource)layerResource;
                    break;
                }
            }
        }
    }
} finally {
    psdImage.dispose();
}
```

Le bloc `finally` garantit que l'image PSD est libérée, maintenant une utilisation de mémoire propre.

## Étape 5 : vérifier la ressource Nvrt
Confirmez que la ressource a été localisée avec succès en vérifiant la variable que vous avez remplie à l'étape précédente.

```java
Assert.isNotNull(nvrtResource);
```

Si l'assertion réussit, vous avez lu avec succès les calques PSD et extrait la ressource Nvrt.

## Pièges courants & conseils
- **Vérifications de null :** Vérifiez toujours que `psdImage` et les objets de calque ne sont pas null avant de les accéder.  
- **Libération des ressources :** Oublier `psdImage.dispose()` peut entraîner des fuites de mémoire dans les applications de longue durée.  
- **Problèmes de chemin de fichier :** Utilisez des chemins absolus ou assurez‑vous que votre répertoire de travail est correctement défini pour éviter `FileNotFoundException`.  
- **Note sur le traitement par lots :** Lors du bouclage sur de nombreux fichiers, réinstanciez le `PsdImage` à l'intérieur de la boucle et libérez‑le immédiatement après avoir terminé le traitement de chaque fichier.

## Conclusion
Vous savez maintenant **comment charger des PSD**, lire leurs calques et extraire la ressource Nvrt du **calque de réglage d'inversion** à l'aide de Java et Aspose.PSD. Cette base vous permet de créer des outils d'automatisation graphique puissants, de **traiter des PSD en lot** ou d'intégrer les données Photoshop dans des flux de travail plus vastes.

## Questions fréquemment posées

**Q : Qu'est‑ce qu'Aspose.PSD for Java ?**  
R : Aspose.PSD for Java est une bibliothèque qui permet aux développeurs de créer, modifier, convertir et rendre des fichiers PSD directement depuis du code Java.

**Q : Puis‑je utiliser Aspose.PSD dans des produits commerciaux ?**  
R : Oui, une licence commerciale est requise pour une utilisation en production. Vous pouvez explorer les options d'achat [purchase Aspose.PSD](https://purchase.aspose.com/buy).

**Q : Où puis‑je trouver la documentation d'Aspose.PSD ?**  
R : La documentation complète est disponible ici : [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).

**Q : Existe‑t‑il un essai gratuit ?**  
R : Absolument ! Vous pouvez obtenir un essai gratuit d'Aspose.PSD for Java [download free trial](https://releases.aspose.com/).

**Q : Comment puis‑je obtenir du support pour Aspose.PSD ?**  
R : Vous pouvez poser des questions et obtenir du support sur le forum Aspose : [Aspose Support](https://forum.aspose.com/c/psd/34).

---

**Last Updated:** 2026-09-23  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose

## Tutoriels associés

- [Bibliothèque de traitement d'images Java : calque d'inversion avec Aspose.PSD](/psd/java/advanced-image-manipulation/invert-adjustment-layer/)
- [Ajouter un calque de réglage de niveau aux fichiers PSD avec Aspose.PSD for Java](/psd/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/)
- [Lire les calques PSD avec Aspose.PSD for Java – Utiliser un chargeur de données brutes personnalisé](/psd/java/advanced-psd-layer-features-effects/use-custom-raw-data-loader-psd-files/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}