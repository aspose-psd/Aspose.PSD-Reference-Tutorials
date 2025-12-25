---
date: 2025-12-25
description: Apprenez à remplacer les polices dans les fichiers PSD avec Aspose.PSD
  pour Java – un guide étape par étape qui montre également comment enregistrer un
  PSD au format PNG et gérer les polices manquantes.
linktitle: Settings for Replacing Missing Fonts
second_title: Aspose.PSD Java API
title: Comment remplacer les polices dans Aspose.PSD pour Java
url: /fr/java/advanced-techniques/settings-replacing-missing-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment remplacer les polices dans Aspose.PSD pour Java

## Introduction

Si vous travaillez avec des fichiers Photoshop (PSD) dans une application Java, l'absence de polices peut rompre la mise en page visuelle et provoquer des erreurs de rendu. **Comment remplacer les polices** rapidement et de manière fiable est essentiel pour maintenir la fidélité du design. Dans ce tutoriel, vous apprendrez à utiliser Aspose.PSD pour Java afin de remplacer les polices manquantes, convertir le résultat en PNG, et garder votre flux de conversion d'images fluide. À la fin, vous serez capable de remplacer les polices dans les images, d’enregistrer le PSD en PNG, et d’éviter les pièges courants rencontrés par les développeurs.

## Réponses rapides
- **Que signifie « remplacer les polices » dans le traitement PSD ?** Cela substitue les polices manquantes ou indisponibles par une police de secours que vous spécifiez.  
- **Quelle bibliothèque gère cela automatiquement ?** Aspose.PSD pour Java fournit `PsdLoadOptions.setDefaultReplacementFont`.  
- **Puis‑je également convertir le PSD en PNG après le remplacement ?** Oui – utilisez `PngOptions` et appelez `psdImage.save`.  
- **Ai‑je besoin d’une licence pour une utilisation en production ?** Une licence valide Aspose.PSD est requise pour les builds non‑évaluation.  
- **Quelle version de Java est prise en charge ?** Tout runtime Java 8+ fonctionne avec la version actuelle d’Aspose.PSD.

## Qu’est‑ce que le remplacement de police dans les fichiers PSD ?

Lorsqu’un PSD référence une police qui n’est pas installée sur la machine hôte, le moteur de rendu revient à une police générique, entraînant souvent un texte mal aligné. Le remplacement de police vous permet de définir une police par défaut (par ex. Arial) que la bibliothèque utilisera chaque fois qu’elle rencontrera une police manquante, garantissant ainsi une sortie visuelle cohérente.

## Pourquoi remplacer les polices manquantes avec Aspose.PSD ?

- **Solution sans dépendance** – Aucun besoin de Photoshop natif ou d’outils externes.  
- **Prêt pour le traitement par lots** – Traitez des dizaines de fichiers dans une boucle avec les mêmes paramètres.  
- **Conversion d’image prête** – Après le remplacement, vous pouvez directement **enregistrer le PSD en PNG** ou **convertir le PSD en PNG** sans étapes supplémentaires.  
- **Multiplateforme** – Fonctionne sur les runtimes Java Windows, Linux et macOS.

## Prérequis

1. **Bibliothèque Aspose.PSD** – Téléchargez et installez la bibliothèque Aspose.PSD pour Java depuis la [page des releases](https://releases.aspose.com/psd/java/).  
2. **Environnement de développement Java** – JDK 8 ou version ultérieure installé et configuré.  

Maintenant que nous avons les éléments essentiels, plongeons dans le code.

## Importer les packages

Commencez par importer les classes Aspose.PSD nécessaires. Cela vous donne accès au chargement d’image, aux options de remplacement de police et aux capacités d’export PNG.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Étape 1 : Configurer le répertoire de votre document

Définissez le dossier qui contient le PSD source et où le PNG résultant sera enregistré.

```java
String dataDir = "Your Document Directory";
```

## Étape 2 : Spécifier les fichiers source et destination

Fournissez les chemins complets pour le PSD d’entrée et le PNG de sortie. Cela rend le flux de travail clair et facilite la maintenance du code.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "result.png";
```

## Étape 3 : Configurer les paramètres de remplacement de police

Créez une instance de `PsdLoadOptions` et indiquez à Aspose.PSD quelle police utiliser lorsqu’une police manquante est rencontrée. Dans cet exemple nous utilisons **Arial**, mais vous pouvez le remplacer par n’importe quelle police installée sur votre système.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setDefaultReplacementFont("Arial");
```

## Étape 4 : Charger l’image PSD et remplacer les polices

Chargez le PSD en utilisant les options définies ci‑dessus. La bibliothèque échange automatiquement les polices manquantes avec la police par défaut que vous avez spécifiée.

```java
Image image = Image.load(sourceFile, loadOptions);
PsdImage psdImage = (PsdImage) image;
```

## Étape 5 : Enregistrer l’image modifiée

Configurez les options d’export PNG – couleur vraie avec canal alpha – pour préserver la transparence. Cette étape montre également la **conversion d’image PSD en PNG** après le remplacement de police.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
psdImage.save(destName, options);
```

### Que s’est‑il passé ?

- Le PSD a été ouvert avec une police de secours (Arial).  
- Tous les calques de texte qui référençaient initialement des polices manquantes sont maintenant rendus avec Arial.  
- L’image finale a été enregistrée en PNG, réalisant ainsi **l’enregistrement du PSD en PNG** tout en préservant la fidélité visuelle.

## Problèmes courants & Dépannage

| Problème | Cause | Solution |
|----------|-------|----------|
| Le texte apparaît toujours incorrect | Les métriques de la police diffèrent (taille, graisse) | Ajustez la taille de la police de remplacement par programme ou choisissez une police aux métriques similaires. |
| Le PNG est plus volumineux que prévu | Les options PNG par défaut utilisent la couleur 32 bits | Passez `PngColorType` à `Truecolor` si l’alpha n’est pas nécessaire. |
| Exception de licence | Exécution sans licence valide | Appliquez une licence Aspose.PSD temporaire ou permanente avant de charger l’image. |

## Questions fréquentes

**Q : Aspose.PSD est‑il compatible avec toutes les versions de fichiers PSD ?**  
R : Aspose.PSD prend en charge un large éventail de versions PSD, des premières versions de Photoshop aux dernières fonctionnalités.

**Q : Puis‑je utiliser des polices personnalisées pour le remplacement dans Aspose.PSD ?**  
R : Oui, il suffit de transmettre le nom de la police personnalisée à `setDefaultReplacementFont`. Assurez‑vous que la police soit accessible à la JVM.

**Q : Existe‑t‑il des options de licence pour Aspose.PSD ?**  
R : Explorez les options de licence [ici](https://purchase.aspose.com/buy) pour choisir le plan qui convient le mieux à vos besoins.

**Q : Y a‑t‑il un forum communautaire pour le support d’Aspose.PSD ?**  
R : Oui, visitez le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour le support communautaire et les discussions.

**Q : Comment obtenir une licence temporaire pour Aspose.PSD ?**  
R : Obtenez une licence temporaire [ici](https://purchase.aspose.com/temporary-license/) pour les tests et l’évaluation.

---

**Dernière mise à jour :** 2025-12-25  
**Testé avec :** Aspose.PSD 24.11 pour Java (dernière version au moment de la rédaction)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}