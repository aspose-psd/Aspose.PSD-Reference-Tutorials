---
date: 2026-03-18
description: Apprenez à modifier la résolution PNG en Java et à définir la résolution
  d’image en Java avec Aspose.PSD pour Java. Suivez ce guide étape par étape pour
  optimiser rapidement vos images.
linktitle: Change PNG resolution java using Aspose.PSD
second_title: Aspose.PSD Java API
title: Modifier la résolution PNG en Java avec Aspose.PSD
url: /fr/java/optimizing-png-files/set-png-file-resolution/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Modifier la résolution PNG java avec Aspose.PSD

## Introduction
Si vous devez **modifier la résolution PNG java** rapidement et de manière fiable, vous êtes au bon endroit. Dans ce tutoriel, nous passerons en revue les étapes exactes nécessaires pour ajuster la résolution d’un fichier PNG avec Aspose.PSD pour Java. Que vous construisiez un outil de traitement par lots, un service web ou que vous peaufiniez simplement quelques ressources, la même approche fonctionne partout. Ouvrez votre IDE préféré, et c’est parti !

## Réponses rapides
- **Quelle bibliothèque gère la résolution PNG ?** Aspose.PSD pour Java  
- **Méthode principale ?** `PngOptions.setResolutionSettings`  
- **Valeurs DPI typiques ?** 72 × 96 pour les images prêtes pour le web  
- **Ai‑je besoin d’une licence ?** Une version d’essai suffit pour les tests ; une licence est requise en production  
- **JDK supporté ?** Java 8 ou supérieur  

## Qu’est‑ce que « change PNG resolution java » ?
Modifier la résolution PNG en Java signifie changer les métadonnées DPI (points par pouce) qui indiquent aux navigateurs et aux imprimantes la taille d’affichage de l’image. Les données pixel restent identiques, mais le tag de résolution est mis à jour, ce qui peut influencer la taille d’impression et la qualité.

## Pourquoi utiliser Aspose.PSD pour cette tâche ?
Aspose.PSD fournit une API de haut niveau qui abstrait la gestion bas‑niveau du PNG, vous permettant de vous concentrer sur la logique métier plutôt que sur les particularités du format de fichier. Elle prend en charge des centaines de fonctionnalités PSD, fonctionne sur n’importe quelle plateforme exécutant Java et ne nécessite aucune bibliothèque native.

## Pré‑requis
Avant de commencer, assurez‑vous d’avoir :

1. **Java Development Kit (JDK) 8+** – le code s’exécute sur tout JDK récent.  
2. **Aspose.PSD pour Java** – téléchargez‑le depuis le [lien de téléchargement](https://releases.aspose.com/psd/java/).  
3. **Un IDE** – IntelliJ IDEA, Eclipse ou VS Code avec le support Java.  
4. **Un fichier PSD d’exemple** – nous le convertirons en PNG et modifierons sa résolution.  
5. **Connaissances de base en Java** – vous comprendrez les extraits sans explication supplémentaire.

## Importer les packages
Maintenant que tout est prêt, importez les classes dont vous aurez besoin. Ces imports vous donnent accès au chargement d’image, aux paramètres de résolution et aux options d’export PNG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResolutionSetting;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## Étape 1 : Configurer votre projet Java
Créez un nouveau projet Java (ou un module Maven/Gradle) et ajoutez le JAR Aspose.PSD au chemin de construction. Si vous utilisez Maven, ajoutez la dépendance appropriée depuis le dépôt Aspose.

## Étape 2 : Définir le répertoire de vos documents
Indiquez au programme où se trouve le fichier PSD source et où écrire le PNG de sortie.

```java
String dataDir = "Your Document Directory"; // Update with your folder path
```

Remplacez `"Your Document Directory"` par le chemin absolu ou relatif contenant `sample.psd`.

## Étape 3 : Charger l’image PSD
Utilisez la classe `PsdImage` pour lire le fichier PSD depuis le disque.

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "sample.psd");
```

Assurez‑vous que le nom du fichier correspond bien au PSD que vous souhaitez traiter.

## Étape 4 : Créer et configurer les options PNG
C’est ici que nous **modifions réellement la résolution PNG java**. Nous instancions `PngOptions` et définissons les valeurs DPI horizontale et verticale via `ResolutionSetting`.

```java
PngOptions options = new PngOptions();
options.setResolutionSettings(new ResolutionSetting(72, 96)); // 72 DPI horizontal, 96 DPI vertical
```

N’hésitez pas à remplacer `72` et `96` par les valeurs qui conviennent à votre dispositif cible. C’est le cœur de l’opération **set image resolution java**.

## Étape 5 : Enregistrer le PNG résultant
Enfin, exportez le PSD en PNG avec les nouvelles métadonnées de résolution.

```java
psdImage.save(dataDir + "SettingResolution_output.png", options);
```

Le fichier `SettingResolution_output.png` apparaîtra dans le même dossier, maintenant doté des valeurs DPI que vous avez spécifiées.

## Pièges courants et conseils
- **Chemin incorrect** – Vérifiez que `dataDir` se termine par un séparateur de fichier (`/` ou `\`).  
- **DPI non supporté** – La plupart des navigateurs ignorent les DPI supérieurs à 300 ; gardez‑les raisonnables.  
- **Utilisation de la mémoire** – Les PSD volumineux peuvent consommer beaucoup de RAM ; pensez à libérer `psdImage` après l’enregistrement (`psdImage.dispose()`).  

## Conclusion
Vous venez d’apprendre comment **modifier la résolution PNG java** à l’aide d’Aspose.PSD. En ajustant `ResolutionSetting`, vous contrôlez la façon dont vos PNG sont interprétés par les imprimantes et les outils de conception sans altérer les données pixel. Explorez d’autres options comme le niveau de compression, la profondeur de couleur ou le traitement par lots pour automatiser davantage votre flux de travail.

Pour aller plus loin, consultez la documentation officielle [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).

## FAQ
### Quels formats puis‑je convertir depuis des fichiers PSD avec Aspose.PSD pour Java ?
Vous pouvez convertir les fichiers PSD en PNG, JPEG, BMP et TIFF.  
### Dois‑je disposer d’une licence pour utiliser Aspose.PSD pour Java ?
Oui, bien qu’une version d’essai gratuite soit disponible, une licence valide est requise pour une utilisation continue après l’évaluation.  
### Puis‑je changer la résolution plusieurs fois dans un même programme ?
Absolument ! Vous pouvez créer différentes instances de `PngOptions` pour divers paramètres d’exportation au sein de la même application.  
### Que faire si mon fichier PSD est corrompu ?
Aspose.PSD gère de nombreux problèmes courants, mais si un fichier est gravement corrompu, il se peut qu’il ne se charge pas. Conservez toujours une sauvegarde.  
### Aspose.PSD convient‑il aux applications haute performance ?
Oui, il est conçu pour gérer de gros fichiers efficacement et convient aux tâches de traitement d’image intensives.

## Questions fréquentes
**Q : Comment définir programmatique un DPI différent pour les axes horizontal et vertical ?**  
R : Utilisez `new ResolutionSetting(horizontalDpi, verticalDpi)` comme illustré dans l’exemple d’options PNG.  

**Q : Puis‑je traiter plusieurs fichiers PSD en lot lors d’une même exécution ?**  
R : Oui — encapsulez les étapes de chargement, de configuration des options et d’enregistrement dans une boucle qui parcourt votre collection de fichiers.  

**Q : Le changement de DPI affecte‑t‑il la taille du fichier ?**  
R : Généralement non ; le DPI est une métadonnée. La taille du fichier ne change que si vous modifiez la compression ou les dimensions pixel.  

**Q : Existe‑t‑il un moyen de lire le DPI actuel d’un PNG existant ?**  
R : Chargez le PNG avec `Image.load()` et inspectez `image.getResolutionSettings()` (disponible pour les fichiers PNG).  

**Q : Quelles versions de JDK sont officiellement prises en charge ?**  
R : Aspose.PSD pour Java prend en charge JDK 8 à JDK 21.

---

**Dernière mise à jour :** 2026-03-18  
**Testé avec :** Aspose.PSD pour Java 24.10  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}