---
date: 2026-01-09
description: Apprenez à convertir un PSD en PNG en utilisant le seuillage de Bradley
  dans Aspose.PSD pour Java. Ce guide montre comment choisir le seuil optimal et binariser
  efficacement une image PSD.
linktitle: Bradley Thresholding
second_title: Aspose.PSD Java API
title: Convertir PSD en PNG avec le seuillage Bradley (Aspose.PSD Java)
url: /fr/java/image-processing/bradley-thresholding/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir PSD en PNG avec le seuillage de Bradley (Aspose.PSD Java)

Bienvenue dans ce guide complet sur **convertir PSD en PNG** en utilisant le seuillage de Bradley dans Aspose.PSD pour Java. Dans les prochaines minutes, vous verrez pourquoi cette technique est idéale pour créer des fichiers PNG binarisés à fort contraste à partir de documents Photoshop, et vous bénéficierez d’une démonstration pratique, étape par étape.

## Réponses rapides
- **Puis-je convertir PSD en PNG avec Aspose.PSD ?** Oui – chargez le PSD, appliquez `binarizeBradley`, puis enregistrez en PNG.  
- **Que signifie « choisir le seuil optimal » ?** C’est la valeur de sensibilité (0‑1) qui détermine comment les pixels sombres/clairs sont classés.  
- **Ai-je besoin d’une licence pour une utilisation en production ?** Une licence commerciale est requise ; un essai gratuit suffit pour l’évaluation.  
- **Quels formats d’image sont pris en charge pour l’enregistrement ?** PNG, JPEG, BMP, et bien d’autres via les classes `ImageOptions`.  
- **Le code est‑il compatible avec Java 8 et versions ultérieures ?** Absolument – l’API Aspose.PSD Java prend en charge Java 8+.

## Qu’est‑ce que le seuillage de Bradley ?
Le seuillage de Bradley est un algorithme de binarisation adaptatif qui calcule une moyenne locale pour chaque pixel et compare l’intensité du pixel à cette moyenne multipliée par un seuil défini par l’utilisateur. Le résultat est une image noir‑et‑blanc nette qui conserve les détails importants.

## Pourquoi convertir PSD en PNG avec le seuillage de Bradley ?
- **Préserver les bords nets** – Idéal pour l’OCR, la détection de codes‑barres ou tout flux de travail nécessitant une séparation claire entre le premier plan et l’arrière‑plan.  
- **Réduire la taille du fichier** – Le PNG est sans perte mais souvent plus petit après binarisation.  
- **Compatibilité multiplateforme** – Le PNG fonctionne partout, alors que le PSD est spécifique à Photoshop.  

## Prérequis
Avant de plonger, assurez‑vous d’avoir :

1. **Environnement de développement Java** – JDK 8 ou version plus récente installé.  
2. **Bibliothèque Aspose.PSD** – Téléchargez le JAR le plus récent depuis [here](https://releases.aspose.com/psd/java/).  
3. **Image PSD d’exemple** – Tout fichier PSD que vous souhaitez convertir ; vous pouvez également utiliser l’exemple fourni dans les exemples Aspose.

## Importer les packages
Commencez par importer les classes nécessaires dans votre projet Java :

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## Comment convertir PSD en PNG en utilisant le seuillage de Bradley
Voici le flux complet découpé en étapes numérotées claires. Chaque étape comprend une courte explication suivie du code exact à copier‑coller.

### Étape 1 : Charger l’image PSD
Tout d’abord, indiquez le fichier source et chargez‑le avec Aspose.PSD.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "binarized_out.png";

// Load an image
PsdImage image = (PsdImage)Image.load(sourceFile);
```

### Étape 2 : Choisir le seuil optimal
La valeur du seuil (plage 0 – 1) contrôle l’agressivité de la binarisation. Un point de départ typique est **0.15**, mais vous pouvez l’ajuster selon votre image.

```java
// Define threshold value
double threshold = 0.15;
```

### Étape 3 : Binariser l’image PSD
Appliquez maintenant l’algorithme Bradley. Cette étape **binarize PSD image** en fonction du seuil que vous avez sélectionné.

```java
// Call BinarizeBradley method and pass the threshold value as a parameter
image.binarizeBradley(threshold);
```

### Étape 4 : Enregistrer la sortie au format PNG
Enfin, écrivez l’image traitée sur le disque au format PNG.

```java
// Save the output image
image.save(destName, new PngOptions());
```

Répétez ces étapes pour le nombre de fichiers PSD que vous devez traiter, en ajustant le seuil au besoin pour obtenir le meilleur résultat visuel.

## Problèmes courants et astuces
- **Seuil trop bas/élevé :** Si la sortie semble trop bruitée ou délavée, ajustez la valeur `threshold` de façon incrémentale (p. ex., 0.10 – 0.20).  
- **Consommation de mémoire :** Les gros fichiers PSD peuvent être gourmands en mémoire. Envisagez de les traiter un par un ou d’augmenter la taille du tas JVM (`-Xmx`).  
- **Aperçu avant l’enregistrement :** Utilisez `image.save("preview.bmp", new BmpOptions());` pour inspecter le résultat binarisé avant l’exportation finale en PNG.

## Questions fréquentes

**Q : Quelle est la différence entre `binarizeBradley` et les autres méthodes de seuillage ?**  
**R :** `binarizeBradley` calcule une moyenne locale pour chaque pixel, ce qui le rend plus robuste pour les images avec un éclairage inégal comparé au seuillage global.

**Q : Puis‑je appliquer le seuillage de Bradley aux fichiers JPEG ou BMP ?**  
**R :** Oui. Chargez n’importe quel format pris en charge avec `Image.load(...)`, puis appelez `binarizeBradley` avant d’enregistrer.

**Q : Existe‑t‑il un moyen d’apercevoir l’image binarisée avant de l’enregistrer ?**  
**R :** Absolument. Utilisez l’une des options d’enregistrement d’image d’Aspose.PSD (p. ex., BMP) pour créer un fichier d’aperçu temporaire.

**Q : Où puis‑je trouver davantage d’assistance et de ressources ?**  
**R :** Consultez le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour l’aide de la communauté et explorez la [documentation](https://reference.aspose.com/psd/java/) complète pour des scénarios avancés.

## Conclusion
Vous avez maintenant appris comment **convertir PSD en PNG** efficacement en **choisissant un seuil optimal** et en **binarisant l’image PSD** avec le seuillage de Bradley. Cette approche est idéale pour les flux de travail qui exigent des sorties PNG nettes et à fort contraste à partir de fichiers Photoshop complexes.

---

**Last Updated:** 2026-01-09  
**Tested With:** Aspose.PSD Java 23.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}