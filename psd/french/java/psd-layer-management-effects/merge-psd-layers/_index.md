---
date: 2026-04-05
description: Apprenez à exporter un PSD en PNG et à fusionner les calques PSD à l’aide
  d’Aspose.PSD pour Java. Comprend la conversion de PSD en JPEG, le réglage de la
  qualité JPEG et des astuces de conversion de PSD en TIFF.
keywords:
- export psd to png
- convert psd to jpeg
- how to merge psd
- set jpeg quality
- psd to tiff conversion
linktitle: Exporter PSD en PNG et fusionner les calques avec Aspose.PSD pour Java
second_title: Aspose.PSD Java API
title: Exporter le PSD en PNG et fusionner les calques avec Aspose.PSD pour Java
url: /fr/java/psd-layer-management-effects/merge-psd-layers/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter PSD en PNG et fusionner les calques avec Aspose.PSD pour Java

## Introduction

Vous êtes-vous déjà demandé comment les graphistes créent ces images complexes et superposées dans Photoshop ? Le secret réside souvent dans **l'exportation de PSD en PNG** et la fusion intelligente des calques. Si vous travaillez avec des fichiers PSD en Java, maîtriser ces techniques peut vous aider à créer des images composites, réduire la taille des fichiers et préparer les ressources pour le web ou le mobile. Dans ce tutoriel, nous allons parcourir **comment fusionner les calques PSD** à l'aide d'Aspose.PSD pour Java, et nous vous montrerons également comment exporter le résultat en PNG (ou JPEG/TIFF si nécessaire). À la fin, vous pourrez automatiser la gestion des calques et les flux d'exportation directement depuis votre application Java.

## Réponses rapides
- **Quelle bibliothèque gère les fichiers PSD en Java ?** Aspose.PSD for Java.  
- **Puis-je exporter PSD en PNG ?** Oui – il suffit de définir les options d'image appropriées.  
- **Comment fusionner plusieurs calques ?** Chargez le PSD, manipulez la collection `Layer`, puis enregistrez.  
- **Et si j'ai besoin de contrôler la qualité JPEG ?** Utilisez `JpegOptions` et définissez la qualité (0‑100).  
- **Photoshop est-il requis ?** Non, Aspose.PSD fonctionne indépendamment du logiciel Adobe.

## Qu'est-ce que l'exportation de PSD en PNG ?
Exporter PSD en PNG signifie convertir un document Photoshop (PSD) en un fichier Portable Network Graphics (PNG) tout en aplatissant ou fusionnant éventuellement les calques. PNG préserve la transparence et est largement supporté sur le web, ce qui en fait un format populaire pour les ressources d'interface utilisateur.

## Pourquoi fusionner les calques PSD programmatiquement ?
- **Automatisation :** Traitez par lots des centaines de fichiers sans clics manuels.  
- **Performance :** Les calques fusionnés réduisent le temps de rendu dans les applications en aval.  
- **Taille du fichier :** Aplatir les calques inutiles peut réduire l'image finale.  
- **Cohérence :** Garantit le même ordre de calques et le même mode de fusion entre les builds.

## Prérequis

1. **Bibliothèque Aspose.PSD pour Java** – téléchargez depuis le [lien de téléchargement Aspose.PSD pour Java](https://releases.aspose.com/psd/java/).  
2. **Environnement de développement Java** – IntelliJ IDEA, Eclipse, ou tout IDE de votre choix.  
3. **Fichier PSD d'exemple** – un fichier avec plusieurs calques (par ex., `layers.psd`).  
4. **Connaissances de base en Java** – vous devez être à l'aise avec les classes et les méthodes.  
5. **Licence temporaire Aspose (facultatif)** – pour les fichiers volumineux ou pour supprimer les limitations d'essai, obtenez une [licence temporaire](https://purchase.aspose.com/temporary-license/).

## Importer les packages

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.JpegOptions;
```

## Guide étape par étape

### Étape 1 : Charger le fichier PSD

```java
String dataDir = "Your Document Directory";
PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
```

> Ce code charge `layers.psd` dans un objet `PsdImage`, vous donnant un accès complet à ses calques.

### Étape 2 : Inspecter les calques (comment fusionner le PSD)

```java
Layer[] layers = psdImage.getLayers();
System.out.println("Total layers: " + layers.length);

for (Layer layer : layers) {
    System.out.println("Layer name: " + layer.getName());
}
```

> Examiner les noms des calques vous aide à décider lesquels aplatir ou garder séparés.

### Étape 3 : Définir les options d'image (définir la qualité JPEG)

```java
JpegOptions jpgOptions = new JpegOptions();
jpgOptions.setQuality(80); // Set the quality of the JPEG image (0-100)
```

> Si vous préférez PNG ou TIFF, vous pouvez remplacer `JpegOptions` par `PngOptions` ou `TiffOptions` – c'est ici que la **conversion PSD en TIFF** serait configurée.

### Étape 4 : Enregistrer l'image fusionnée (exporter PSD en PNG)

```java
psdImage.save(dataDir + "MergePSDlayers_output.png", jpgOptions);
```

> La méthode `save` écrit le résultat fusionné dans `MergePSDlayers_output.png`.  
> *Conseil :* Pour exporter en PNG, remplacez `jpgOptions` par une instance de `PngOptions` ; le reste du code reste identique.

## Problèmes courants et solutions

- **Exception fichier non trouvé :** Vérifiez que `dataDir` se termine par un séparateur de chemin (`/` ou `\\`) et que `layers.psd` existe.  
- **Couleurs inattendues après fusion :** Assurez-vous que les modes de fusion des calques sont compatibles ; vous pouvez les ajuster via `layer.setBlendMode(...)`.  
- **Fichier de sortie volumineux :** Réduisez la qualité JPEG ou utilisez les niveaux de compression PNG pour diminuer la taille.

## Questions fréquemment posées

**Q : Est-il possible d'enregistrer l'image fusionnée dans des formats autres que JPEG ?**  
R : Absolument ! Aspose.PSD prend en charge PNG, BMP, TIFF, et plus encore. Utilisez simplement la classe d'options correspondante (`PngOptions`, `BmpOptions`, `TiffOptions`).

**Q : Comment puis-je ajuster la qualité de l'image pour différents formats de sortie ?**  
R : Chaque classe d'options expose ses propres paramètres de qualité/compression. Pour JPEG, utilisez `setQuality(int)`. Pour PNG, vous pouvez contrôler `CompressionLevel`.

**Q : Dois-je installer Photoshop pour utiliser Aspose.PSD pour Java ?**  
R : Non. Aspose.PSD fonctionne indépendamment d'Adobe Photoshop, vous pouvez donc l'exécuter sur n'importe quel serveur ou environnement CI.

**Q : Que se passe-t-il si je ne définis pas les options d'image avant d'enregistrer ?**  
R : La bibliothèque applique des paramètres par défaut (par ex., qualité JPEG 75). Spécifier les options vous donne le contrôle sur le résultat final.

**Q : Puis-je convertir un PSD directement en TIFF en une seule étape ?**  
R : Oui – instanciez `TiffOptions` et appelez `psdImage.save("output.tiff", tiffOptions);`.

---

**Dernière mise à jour :** 2026-04-05  
**Testé avec :** Aspose.PSD for Java 24.12 (dernière version au moment de la rédaction)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}