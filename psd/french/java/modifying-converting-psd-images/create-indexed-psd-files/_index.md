---
date: 2026-03-15
description: Apprenez à créer des fichiers PSD, à générer une palette de couleurs
  PSD et à définir le mode couleur PSD à l'aide d'Aspose.PSD pour Java dans ce guide
  étape par étape.
linktitle: Create Indexed PSD Files using Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Comment créer des fichiers PSD avec Aspose.PSD pour Java
url: /fr/java/modifying-converting-psd-images/create-indexed-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment créer des fichiers PSD avec Aspose.PSD pour Java

## Introduction
Si vous vous êtes déjà demandé **comment créer des PSD** de façon programmatique, vous êtes au bon endroit. Aspose.PSD pour Java vous donne un contrôle total sur les documents Photoshop, vous permettant de générer, modifier et enregistrer des fichiers PSD sans jamais ouvrir Photoshop. Dans ce tutoriel, nous allons parcourir la création d’un fichier **PSD indexé**, la définition du mode couleur du PSD et la génération d’une palette de couleurs personnalisée — le tout avec du code Java clair, étape par étape. Que vous construisiez une chaîne graphique, automatisiez la création d’actifs, ou que vous expérimentiez simplement, les concepts présentés vous aideront à concrétiser vos idées visuelles.

## Quick Answers
- **Quelle bibliothèque faut‑il ?** Aspose.PSD pour Java  
- **Puis‑je créer un PSD indexé ?** Oui, en définissant le mode couleur sur `Indexed`  
- **Dois‑je installer Photoshop ?** Non, Aspose.PSD fonctionne de manière indépendante  
- **Quelle version de Java est requise ?** JDK 8 ou ultérieure  
- **Quelle taille maximale pour le canevas ?** N’importe quelle taille ; cet exemple utilise 500 × 500 px  

## Qu’est‑ce qu’un fichier PSD indexé ?
Un PSD indexé stocke les couleurs dans une palette plutôt que des valeurs couleur complètes pour chaque pixel. Cela réduit la taille du fichier et est idéal pour les graphiques avec un nombre limité de couleurs, comme les icônes ou les éléments d’interface utilisateur. En générant une palette personnalisée, vous contrôlez exactement quelles couleurs apparaissent dans l’image finale.

## Pourquoi générer une palette de couleurs PSD ?
Créer une **palette de couleurs PSD** vous permet de :
- Garder les tailles de fichier petites pour le web ou le mobile  
- Garantir une cohérence de marque en limitant les couleurs à votre palette corporative  
- Accélérer le rendu dans les applications qui prennent en charge les images indexées  

## Prérequis
Avant de plonger dans le code, assurez‑vous de disposer de :

1. **Connaissances de base en Java** – vous devez être à l’aise avec les classes, méthodes et la création d’objets.  
2. **Java Development Kit (JDK) 8+** – installé et configuré dans votre IDE.  
3. **IDE (IntelliJ IDEA, Eclipse, etc.)** – optionnel mais fortement recommandé pour faciliter le débogage.  
4. **Bibliothèque Aspose.PSD pour Java** – téléchargez‑la **[ici](https://releases.aspose.com/psd/java/)** et ajoutez le JAR à votre classpath.  
5. **Concepts fondamentaux de conception graphique** – la compréhension des modes couleur, des palettes et des formes de base vous aidera à suivre le tutoriel.  

## Import Packages
Avant de poursuivre avec le code, assurons‑nous que tous les packages nécessaires sont importés dans votre application Java. Voici ce dont vous avez besoin :

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdColorPalette;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

Ces importations vous permettront de travailler avec les options PSD, les couleurs et la manipulation graphique via Aspose.PSD.

Passons maintenant à l’analyse du code étape par étape pour **comment créer des PSD** avec un mode couleur indexé.

## Step 1: Set Up Your Document Directory
Tout d’abord, définissez l’endroit où le PSD généré sera enregistré.

```java
String dataDir = "Your Document Directory";
```

Remplacez `"Your Document Directory"` par un chemin absolu ou relatif, par exemple `"/Users/YourName/Documents/"`.

## Step 2: Create an Instance of PsdOptions
`PsdOptions` contient tous les paramètres du fichier que vous êtes sur le point de générer.

```java
PsdOptions createOptions = new PsdOptions();
```

## Step 3: Set Core Properties of PsdOptions
Ici nous spécifions l’emplacement de sortie, le **set psd color mode** à `Indexed`, et la version du PSD.

```java
createOptions.setSource(new FileCreateSource(dataDir + "Newsample_out.psd", false));
createOptions.setColorMode(ColorModes.Indexed);
createOptions.setVersion(5);
```

- **Source** – le chemin complet du nouveau fichier.  
- **Color Mode** – `Indexed` indique à Aspose.PSD d’utiliser une image basée sur une palette.  
- **Version** – version du format PSD (5 fonctionne pour la plupart des versions modernes de Photoshop).  

## Step 4: Create a Color Palette (Generate PSD Color Palette)
Définissez les couleurs qui seront disponibles dans l’image indexée.

```java
Color[] palette = { Color.getRed(), Color.getGreen(), Color.getBlue(), Color.getYellow() };
createOptions.setPalette(new PsdColorPalette(palette));
createOptions.setCompressionMethod(CompressionMethod.RLE);
```

- Le tableau `palette` peut contenir jusqu’à 256 objets `Color`.  
- `CompressionMethod.RLE` offre une compression sans perte efficace pour les images indexées.  

## Step 5: Create the PSD Image Canvas
Créons maintenant un PSD vierge avec les dimensions souhaitées.

```java
Image psd = Image.create(createOptions, 500, 500);
```

Cela crée un canevas de 500 × 500 pixels qui utilise la palette définie précédemment.

## Step 6: Draw Graphics on the PSD
Ajoutons du contenu visuel — ici nous dessinons une simple ellipse rouge sur un fond blanc.

```java
Graphics graphics = new Graphics(psd);
graphics.clear(Color.getWhite());
graphics.drawEllipse(new Pen(Color.getRed(), 6), new Rectangle(0, 0, 400, 400));
```

- `clear(Color.getWhite())` remplit le fond en blanc.  
- `drawEllipse` trace une ellipse rouge avec un contour de 6 pixels.  

## Step 7: Save the PSD File
Enfin, persistez l’image sur le disque.

```java
psd.save();
```

Le fichier `Newsample_out.psd` apparaîtra dans le répertoire que vous avez indiqué précédemment.

## Common Issues & Tips
- **Palette Size** – Si vous avez besoin de plus de 4 couleurs, ajoutez‑les simplement au tableau `palette` (jusqu’à 256).  
- **File Permissions** – Assurez‑vous que le processus Java possède les droits d’écriture sur `dataDir`.  
- **Incorrect Color Mode** – Oublier `createOptions.setColorMode(ColorModes.Indexed)` produira un PSD RGB au lieu d’un PSD indexé.  

## Frequently Asked Questions

**Q : Qu’est‑ce qu’Aspose.PSD pour Java ?**  
R : Aspose.PSD pour Java est une bibliothèque qui permet de manipuler des fichiers PSD (Photoshop) de façon programmatique avec Java.

**Q : Puis‑je utiliser Aspose.PSD gratuitement ?**  
R : Oui, vous pouvez accéder à une version d’essai gratuite d’Aspose.PSD **[ici](https://releases.aspose.com/)**.

**Q : Dois‑je installer Photoshop pour travailler avec Aspose.PSD ?**  
R : Non, vous pouvez créer et manipuler des fichiers PSD sans Photoshop, Aspose.PSD gère toutes les opérations de manière indépendante.

**Q : Comment obtenir une licence temporaire pour Aspose.PSD ?**  
R : Vous pouvez demander une licence temporaire **[ici](https://purchase.aspose.com/temporary-license/)**.

**Q : Où puis‑je obtenir du support pour Aspose.PSD ?**  
R : Vous pouvez obtenir du support sur le forum Aspose **[ici](https://forum.aspose.com/c/psd/34)**.

## Conclusion
Vous venez d’apprendre **comment créer des PSD** avec un mode couleur indexé, de générer une palette personnalisée et d’ajouter des graphiques simples — le tout en utilisant Aspose.PSD pour Java. Avec ces bases, vous pouvez passer à des dessins plus complexes, à la gestion de calques et au traitement par lots. Pour aller plus loin, consultez la référence officielle de l’API **[ici](https://reference.aspose.com/psd/java/)** et continuez à expérimenter avec différentes palettes et primitives de dessin.

---

**Last Updated:** 2026-03-15  
**Tested With:** Aspose.PSD for Java 24.12 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}