---
date: 2025-12-05
description: Apprenez à effectuer le remplacement de polices Aspose PSD en Java. Ce
  tutoriel pas à pas de manipulation d’images Java vous montre comment remplacer efficacement
  les polices dans les fichiers PSD.
language: fr
linktitle: Replace Fonts
second_title: Aspose.PSD Java API
title: Remplacement de polices PSD Aspose en Java – Remplacer les polices dans les
  fichiers PSD
url: /java/advanced-image-manipulation/replace-fonts/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Remplacement de polices Aspose PSD en Java

## Introduction

Si vous devez remplacer des polices manquantes ou indésirables dans un fichier Photoshop (PSD), le **remplacement de polices Aspose PSD** le rend simple. Dans les applications Java, vous pouvez charger un PSD, indiquer à Aspose la police de secours à utiliser, puis enregistrer le résultat dans le format de votre choix. Ce tutoriel vous guide à travers le flux complet de **remplacement de polices aspose psd**, depuis la configuration du projet jusqu’à l’exportation de l’image mise à jour.

## Quick Answers
- **Quelle bibliothèque gère le remplacement de polices ?** Aspose.PSD for Java  
- **Combien de temps prend l’implémentation ?** Environ 5‑10 minutes pour un scénario de base  
- **Quelle police est utilisée comme secours par défaut ?** Vous pouvez définir n’importe quelle police TrueType, par ex. « Arial »  
- **Puis‑je enregistrer dans d’autres formats que PNG ?** Oui – PSD, JPEG, BMP, etc., sont pris en charge  
- **Ai‑je besoin d’une licence pour la production ?** Une licence valide Aspose.PSD est requise pour un usage non‑essai  

## Qu’est‑ce que le remplacement de polices Aspose PSD ?

Le remplacement de polices Aspose PSD consiste à spécifier une police de substitution que la bibliothèque utilisera chaque fois qu’elle rencontrera une police manquante ou non prise en charge dans un fichier PSD. Cela garantit que les calques de texte sont rendus correctement sans édition manuelle dans Photoshop.

## Pourquoi utiliser Aspose.PSD pour Java ?

- **Gestion complète des PSD** – couches, masques, effets et texte sont tous accessibles via l’API.  
- **Multiplateforme** – fonctionne sur tout OS supportant Java.  
- **Aucune dépendance externe** – la bibliothèque gère la substitution de polices en interne, vous n’avez donc pas besoin d’inclure des polices supplémentaires avec votre application.  

## Prérequis

Avant de commencer, assurez‑vous d’avoir :

- **Java Development Kit (JDK)** – version 8 ou supérieure installée.  
- **Aspose.PSD for Java** – téléchargez le JAR le plus récent depuis la [page de publication](https://releases.aspose.com/psd/java/).  
- **Un IDE** – IntelliJ IDEA, Eclipse ou tout autre éditeur de votre choix.  

## Import Packages

Commencez par importer les classes dont vous aurez besoin. Cela vous donne accès au chargement d’image, aux options de chargement et aux fonctions d’enregistrement.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Étape 1 : Définir le répertoire du document

Définissez le dossier contenant le fichier PSD source. Remplacez le texte de substitution par le chemin réel sur votre machine.

```java
String dataDir = "Your Document Directory";
```

## Étape 2 : Charger l’image avec une police de remplacement

Créez une instance `PsdLoadOptions`, spécifiez la police de remplacement par défaut (par ex. **Arial**) et chargez le PSD. Aspose appliquera automatiquement la police de secours chaque fois qu’une police manquante est rencontrée.

```java
PsdLoadOptions psdLoadOptions = new PsdLoadOptions(); 
psdLoadOptions.setDefaultReplacementFont("Arial");

PsdImage psdImage = (PsdImage)Image.load(dataDir + "Cloud_AzPlat_Banner3A_SB_EN_US_160x600_chinese_font.psd", psdLoadOptions);
```

## Étape 3 : Enregistrer l’image remplacée

Après la substitution de police, vous pouvez exporter l’image dans n’importe quel format pris en charge. Ici nous l’enregistrons en PNG, mais vous pouvez également choisir JPEG, BMP ou même réécrire le fichier en PSD.

```java
PngOptions pngOptions = new PngOptions();
psdImage.save(dataDir + "replaced_font.png", pngOptions);
```

## Problèmes courants et solutions

| Problème | Cause | Solution |
|----------|-------|----------|
| Le texte apparaît illisible après le remplacement | La police de secours ne contient pas les glyphes requis | Choisissez une police qui prend en charge la plage Unicode nécessaire (par ex. « Arial Unicode MS »). |
| `OutOfMemoryError` sur de gros PSD | Chargement d’un fichier très haute résolution sans assez de mémoire heap | Augmentez la taille du heap JVM (`-Xmx2g`) ou chargez l’image en mode streaming si disponible. |
| Exception de licence | Utilisation de la version d’essai en production | Appliquez une licence permanente ou temporaire valide avant de charger l’image. |

## Foire aux questions

**Q : Puis‑je remplacer les polices dans d’autres formats d’image que le PSD ?**  
R : Oui. Bien que le cas d’usage principal soit le PSD, Aspose.PSD prend également en charge PNG, JPEG, BMP et TIFF, permettant le remplacement de police lorsque des calques de texte existent.

**Q : La police de remplacement par défaut est‑elle obligatoire ?**  
R : Non. Vous pouvez définir n’importe quelle police TrueType de votre choix, ou omettre ce paramètre pour laisser Aspose utiliser son défaut interne.

**Q : Existe‑t‑il des exigences de licence pour l’utilisation d’Aspose.PSD ?**  
R : Une licence commerciale est requise pour les déploiements en production. Consultez la [page d’achat](https://purchase.aspose.com/buy) pour plus de détails.

**Q : Puis‑je obtenir une licence temporaire pour les tests ?**  
R : Absolument. Aspose propose des licences temporaires gratuites pour l’évaluation – rendez‑vous sur la [page de licence temporaire](https://purchase.aspose.com/temporary-license/).

**Q : Où puis‑je trouver un support supplémentaire ou discuter des problèmes liés à Aspose.PSD ?**  
R : Le forum communautaire est un excellent endroit pour poser des questions : [forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

**Q : Comment gérer les fichiers PSD contenant plusieurs polices manquantes ?**  
R : Définissez la police de remplacement par défaut une fois (comme montré) – elle sera appliquée à *toutes* les polices manquantes lors du chargement.

**Q : Est‑il possible de remplacer les polices après que l’image a été enregistrée ?**  
R : La substitution de police doit se faire pendant la phase de chargement. Pour changer les polices ultérieurement, rechargez le PSD avec une police de remplacement différente et réenregistrez.

## Conclusion

Vous avez maintenant découvert un flux complet de **remplacement de polices aspose psd** en Java — de l’importation des bonnes classes, à la configuration d’une police de secours, le chargement du PSD, jusqu’à l’exportation de l’image corrigée. Intégrez ce modèle dans vos pipelines de traitement d’image pour garantir une typographie cohérente sur tous vos actifs PSD.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Dernière mise à jour :** 2025-12-05  
**Testé avec :** Aspose.PSD for Java 24.12 (dernière version au moment de la rédaction)  
**Auteur :** Aspose  

---