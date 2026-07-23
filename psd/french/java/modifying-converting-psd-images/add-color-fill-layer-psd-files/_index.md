---
date: 2026-03-02
description: Apprenez comment ajouter un remplissage en créant un calque de remplissage
  de couleur dans les fichiers PSD à l’aide de Java et d’Aspose.PSD. Suivez notre
  guide étape par étape pour définir rapidement la couleur du calque de remplissage.
linktitle: Add Color Fill Layer to PSD Files using Java
second_title: Aspose.PSD Java API
title: 'Comment ajouter un remplissage : ajouter un calque de remplissage de couleur
  aux fichiers PSD avec Java'
url: /fr/java/modifying-converting-psd-images/add-color-fill-layer-psd-files/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajouter un calque de remplissage de couleur aux fichiers PSD avec Java

## Introduction
Vous êtes déjà tombé sur le besoin de manipuler des fichiers Photoshop de façon programmatique, peut‑être pour ajouter une touche de couleur à un design ? Si vous demandez **how to add fill** à un PSD, vous êtes au bon endroit. Dans ce tutoriel, nous allons parcourir les étapes pour ajouter un calque de remplissage de couleur à des fichiers PSD (Photoshop Document) en utilisant Java et la bibliothèque Aspose.PSD. Considérez votre PSD comme une toile numérique—à la fin, vous saurez créer un calque de remplissage de couleur, définir la couleur du calque de remplissage et enregistrer le fichier mis à jour en quelques lignes de code seulement.

## Réponses rapides
- **Quelle bibliothèque est nécessaire ?** Aspose.PSD pour Java
- **Cas d'utilisation principal ?** Ajouter ou modifier par programmation les couleurs de remplissage PSD
- **Combien de temps prend la mise en œuvre ?** Environ 10 à 15 minutes pour un scénario de base
- **Ai-je besoin d'une licence ?** Un essai gratuit fonctionne pour l'évaluation ; une licence commerciale est requise pour la production
- **Version Java prise en charge ?** Java8 et supérieur

## Qu'est-ce qu'un calque de remplissage de couleur ?
Un calque de remplissage de couleur est une superposition de couleur unie qui se situe au-dessus des autres calques dans un document Photoshop. Il est souvent utilisé pour ajouter une couleur d’arrière-plan, créer des masques, ou changer rapidement le thème visuel d’un design sans modifier les pixels individuellement.

## Pourquoi ajouter un calque de remplissage de couleur avec du code ?
- **Automation :** Générer des actifs de marque cohérents à travers de nombreux fichiers.
- **Traitement par lots :** Mettre à jour des dizaines de PSD en quelques secondes au lieu de le faire manuellement.
- **Conceptions dynamiques :** Modifiez les couleurs à la volée en fonction des entrées utilisateur ou de sources de données.

## Prérequis
Avant de Sous-marin dans le code, contrôlez‑nous que vous avez tout le nécessaire :

1. **Java Development Kit (JDK)** – JDK8 ou version plus récente installée.
2. **Aspose.PSD Library** – Téléchargez le JAR le plus récent depuis la [Aspose Releases page](https://releases.aspose.com/psd/java/).
3. **IDE** – IntelliJ IDEA, Eclipse, NetBeans, ou tout éditeur de votre choix.
4. **Connaissances de base de Java** – Familiarité avec les objets, les boucles et la gestion des exceptions.

## Importer des packages
Maintenant que les bases sont couvertes, importons les classes nécessaires. Ces imports nous donnent accès à la manipulation des PSD et des calques de remplissage.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IColorFillSettings;
```

## Comment ajouter un remplissage – Guide étape par étape

### Étape 1 : Configurer votre environnement
Définissez où se trouve votre PSD source et où le fichier modifié sera enregistré, puis chargez le document.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ColorFillLayer.psd";
String exportPath     = dataDir + "ColorFillLayer_output.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- `dataDir` pointe vers le dossier contenant votre PSD.  
- `sourceFileName` est le fichier original que vous allez modifier.  
- `exportPath` est l’endroit où le nouveau fichier avec le **add color fill layer** sera écrit.  

### Étape 2 : Parcourir les calques
Nous devons localiser les éventuels calques de remplissage existants afin de les modifier ou d’en créer un nouveau.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof FillLayer) {
        FillLayer fillLayer = (FillLayer) im.getLayers()[i];
```

- La boucle `for` parcourt chaque calque du PSD.  
- La vérification `instanceof FillLayer` garantit que nous ne travaillons qu’avec des calques de remplissage.

### Étape 3 : Vérifier le type de remplissage
Assurez‑vous que le calque trouvé est un **color fill layer** avant d’essayer de changer sa couleur.

```java
if (fillLayer.getFillSettings().getFillType() != FillType.Color) {
    throw new Exception("Wrong Fill Layer");
}
```

Si le type de remplissage n’est pas `FillType.Color`, nous interrompons l’opération afin d’éviter de modifier accidentellement des remplissages en dégradé ou en motif.

### Étape 4 : Définir la couleur de remplissage
C’est ici que nous **set fill layer color**. L’exemple change le calque en rouge, mais vous pouvez remplacer `Color.getRed()` par n’importe quel autre `Color` dont vous avez besoin (par ex., `Color.getBlue()`, `new Color(255, 165, 0)` pour l’orange).

```java
IColorFillSettings settings = (IColorFillSettings) fillLayer.getFillSettings();
settings.setColor(Color.getRed());
fillLayer.update();
```

- `settings.setColor(...)` modifie réellement la couleur du remplissage.  
- `fillLayer.update()` rafraîchit le calque afin que la nouvelle couleur soit appliquée.  

### Étape 5 : Enregistrer les modifications
Enfin, écrivez le PSD modifié sur le disque.

```java
im.save(exportPath);
break;
```

- Le `break` arrête la boucle après la première mise à jour du calque de remplissage correspondant, ce qui est généralement ce que vous voulez lorsque vous devez **change PSD fill color** une seule fois.

## Problèmes courants et conseils
- **No FillLayer found:** Si votre PSD ne contient pas de calque de remplissage, vous devrez en créer un avec `new FillLayer(im)` et l'ajouter à `im.getLayers()`.
- **Color not update:** Assurez-vous d'appeler `fillLayer.update()` après avoir défini la couleur.
- **Fichier non enregistré :** Vérifiez que `exportPath` pointe vers un répertoire accessible en écriture et que vous avez les autorisations nécessaires.

## Questions fréquemment posées

**Q : Qu'est-ce qu'Aspose.PSD ?**
A: Aspose.PSD est une bibliothèque Java robuste qui vous permet de créer, modifier et convertir des fichiers Photoshop PSD sans avoir besoin d'Adobe Photoshop.

**Q : Puis-je utiliser Aspose.PSD gratuitement ?**
R : Oui, un essai gratuit est disponible sur la [page Aspose Releases](https://releases.aspose.com/).

**Q : Quels formats de fichiers puis-je utiliser en plus de PSD ?**
R : Aspose.PSD prend en charge les formats PSD, PSB, BMP, JPEG, PNG, GIF, TIFF et bien d’autres.

**Q : Comment obtenir de l’aide en cas de problème ?**
R : Vous pouvez poser vos questions sur le [forum d’assistance Aspose](https://forum.aspose.com/c/psd/34).

**Q : Où puis-je acheter une licence complète ?**
R : Les licences sont vendues sur la [page d’achat Aspose](https://purchase.aspose.com/buy).

## Conclusion
Vous savez maintenant **how to add fill** à un document Photoshop de façon programmatique avec Java. En créant ou en localisant un calque de remplissage de couleur, en définissant sa couleur et en enregistrant le résultat, vous pouvez automatiser des tâches de design répétitives, générer des actifs dynamiques, ou intégrer la manipulation de PSD dans des applications Java plus larges. Essayez‑vous — expérimentez avec différentes couleurs, ajoutez plusieurs calques de remplissage, ou combinez cette technique avec d’autres fonctionnalités d’Aspose.PSD pour des pipelines de traitement d’image puissants.

---

**Last Updated:** 2026-03-02  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
