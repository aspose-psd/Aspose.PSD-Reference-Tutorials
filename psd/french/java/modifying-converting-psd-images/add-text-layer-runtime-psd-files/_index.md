---
date: 2026-03-07
description: Apprenez comment ajouter du texte aux fichiers PSD à l'exécution en utilisant
  Java et Aspose.PSD. Suivez ce guide étape par étape pour créer rapidement un calque
  de texte dans un PSD.
linktitle: Add Text Layer on Runtime in PSD Files using Java
second_title: Aspose.PSD Java API
title: Ajouter du texte aux fichiers PSD à l'exécution avec Java
url: /fr/java/modifying-converting-psd-images/add-text-layer-runtime-psd-files/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajouter du texte aux fichiers PSD à l'exécution avec Java

## Introduction
Si vous avez déjà modifié manuellement un document Photoshop, vous savez à quel point les calques peuvent être puissants. Et si vous pouviez **ajouter du texte à des PSD** automatiquement depuis votre application Java ? Avec la bibliothèque Aspose.PSD for Java, vous pouvez créer un calque de texte dans un PSD à l'exécution, ouvrant la voie au traitement par lots, à la génération dynamique de graphiques et aux flux de travail de marque automatisés. Dans ce tutoriel, nous parcourrons l’ensemble du processus, de la configuration du projet à l’enregistrement du fichier mis à jour.

## Réponses rapides
- **Quelle bibliothèque faut‑il ?** Aspose.PSD for Java.  
- **Puis‑je ajouter du texte à un PSD existant ?** Oui – chargez simplement le fichier, ajoutez un `TextLayer`, puis enregistrez.  
- **Ai‑je besoin d’une licence pour la production ?** Une licence commerciale est requise pour un usage autre que l’évaluation.  
- **Quelle version de Java est prise en charge ?** JDK 8 ou supérieur (nous recommandons la dernière LTS).  
- **Cette solution convient‑elle aux back‑ends web ?** Absolument – l’API fonctionne dans tout environnement serveur Java.

## Qu’est‑ce que « ajouter du texte à un PSD » ?
Ajouter du texte à un PSD signifie créer programmétiquement un nouveau calque de texte à l’intérieur d’un document Photoshop. Le calque se comporte comme n’importe quel autre calque de texte Photoshop : vous pouvez le déplacer, modifier son contenu et appliquer du style — le tout sans ouvrir Photoshop.

## Pourquoi créer un calque de texte dans un PSD avec Java ?
- **Automatisation** – Générer des actifs marketing, des filigranes ou des étiquettes produit en masse.  
- **Cohérence** – Garantir la même police, taille et positionnement sur des milliers de fichiers.  
- **Intégration** – Combiner avec d’autres services Java (e‑commerce, reporting, pipelines CI) pour fournir des graphiques à la volée.

## Prérequis
Avant d’écrire du code, assurez‑vous d’avoir :

1. **Java Development Kit (JDK)** – Installez JDK 8 ou plus récent. Vous pouvez [le télécharger ici](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java** – Récupérez le dernier JAR depuis la [page des releases Aspose](https://releases.aspose.com/psd/java/).  
3. **IDE (optionnel mais utile)** – IntelliJ IDEA, Eclipse ou tout éditeur de votre choix.  
4. **Connaissances de base en Java** – Vous devez être à l’aise avec les classes, objets et I/O de fichiers.  
5. **Un PSD d’exemple** – Pour ce guide, nous utiliserons `OneLayer.psd` placé dans le dossier de votre choix.

## Importer les packages
Tout d’abord, importez les classes nécessaires pour travailler avec les fichiers PSD et les calques de texte.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
```

Ces importations vous donnent accès aux fonctionnalités principales d’Aspose.PSD.

## Guide étape par étape

### Étape 1 : Configurer le répertoire de vos documents
Définissez le dossier qui contient votre PSD source et où le résultat sera enregistré.

```java
String dataDir = "Your Document Directory"; 
```

Remplacez `"Your Document Directory"` par le chemin absolu ou relatif vers vos fichiers.

### Étape 2 : Charger votre fichier PSD source
Chargez le PSD existant en mémoire avec `Image.load()`.

```java
String sourceFileName = dataDir + "OneLayer.psd"; 
Image img = Image.load(sourceFileName);
```

Si le chemin est correct, `img` représente maintenant le document Photoshop chargé.

### Étape 3 : Convertir en `PsdImage`
Comme nous utilisons des fonctionnalités spécifiques à Photoshop, convertissez l’`Image` générique en `PsdImage`.

```java
PsdImage im = (PsdImage)img;
```

Cette conversion débloque des méthodes telles que `addTextLayer()`.

### Étape 4 : Définir le rectangle pour le calque de texte
Spécifiez l’endroit où le nouveau texte doit apparaître. Le rectangle définit la position (x, y) et la taille (largeur, hauteur).

```java
Rectangle rect = new Rectangle(
    (int)(im.getWidth() * 0.25),
    (int)(im.getHeight() * 0.25),
    (int)(im.getWidth() * 0.5),
    (int)(im.getHeight() * 0.5)
);
```

N’hésitez pas à ajuster les calculs selon les besoins de votre mise en page.

### Étape 5 : Ajouter le calque de texte
Créez le calque de texte réel à l’intérieur du rectangle défini.

```java
TextLayer layer = im.addTextLayer("Added text", rect);
```

Remplacez `"Added text"` par la chaîne que vous souhaitez voir apparaître dans le PSD. C’est ici que nous **créons un calque de texte PSD** de façon programmatique.

### Étape 6 : Enregistrer votre fichier PSD mis à jour
Écrivez le document modifié dans un nouveau fichier afin de ne pas écraser l’original.

```java
String psdPath = dataDir + "ImageWithTextLayer.psd";
im.save(psdPath);
```

Après exécution, vous trouverez `ImageWithTextLayer.psd` dans le dossier cible, contenant désormais le nouveau calque de texte.

## Problèmes courants et solutions
| Problème | Raison | Solution |
|----------|--------|----------|
| **`NullPointerException` on `im.addTextLayer`** | PSD non chargé correctement (chemin incorrect). | Vérifiez que `sourceFileName` pointe vers un PSD existant. |
| **Text not visible** | Rectangle placé en dehors du canevas ou calque masqué. | Ajustez les coordonnées du rectangle ou vérifiez la visibilité du calque avec `layer.setVisible(true)`. |
| **LicenseException** | Utilisation de la bibliothèque sans licence valide en production. | Obtenez une licence commerciale et configurez‑la via `License license = new License(); license.setLicense("Aspose.PSD.lic");`. |

## Foire aux questions

**Q : Puis‑je ajouter plusieurs calques de texte ?**  
**R :** Oui – répétez simplement les Étapes 4 et 5 pour chaque texte que vous souhaitez insérer.

**Q : Comment styliser le texte (police, taille, couleur) ?**  
**R :** La classe `TextLayer` expose une méthode `getTextData()` où vous pouvez modifier `Font`, `FontSize`, `Color` et d’autres propriétés de style. Consultez la documentation de l’API Aspose.PSD pour plus de détails.

**Q : Et si mon PSD possède déjà de nombreux calques ?**  
**R :** Aspose.PSD fonctionne avec des structures de calques complexes. Vous pouvez cibler des groupes spécifiques ou insérer le nouveau calque de texte à l’indice souhaité en utilisant les surcharges de `addTextLayer`.

**Q : Cette approche convient‑elle aux applications web ?**  
**R :** Absolument. Tant que votre serveur exécute Java, vous pouvez générer ou modifier des PSD à la volée et les servir aux clients.

**Q : Où puis‑je obtenir de l’aide en cas de problème ?**  
**R :** Visitez les [forums de support Aspose](https://forum.aspose.com/c/psd/34) où la communauté et les ingénieurs Aspose peuvent vous assister.

## Conclusion
Vous avez maintenant vu à quel point il est simple **d’ajouter du texte à des PSD** à l’exécution avec Java et Aspose.PSD. Cette technique vous permet d’automatiser la création graphique, de personnaliser des actifs et d’intégrer l’édition de niveau Photoshop dans toute solution Java. Explorez le reste de l’API Aspose.PSD pour ajouter des formes, des calques raster ou même appliquer des filtres pour une automatisation encore plus riche.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Dernière mise à jour :** 2026-03-07  
**Testé avec :** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Auteur :** Aspose  

---