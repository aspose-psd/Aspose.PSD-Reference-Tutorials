---
date: 2026-02-09
description: Apprenez à utiliser la substitution de polices Aspose PSD en Java pour
  gérer les fichiers PSD avec des polices manquantes, remplacer rapidement les polices
  manquantes dans les PSD et exporter des images.
linktitle: Replace Fonts
second_title: Aspose.PSD Java API
title: Substitution de polices PSD Aspose en Java – Remplacer les polices manquantes
url: /fr/java/advanced-image-manipulation/replace-fonts/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Substitution de polices Aspose PSD en Java

## Introduction

Si vous devez remplacer des polices manquantes ou indésirables dans un fichier Photoshop (PSD), **Aspose PSD font substitution** le rend simple. Dans les applications Java, vous pouvez charger un PSD, indiquer à Aspose la police de secours à utiliser, puis enregistrer le résultat dans le format de votre choix. Ce tutoriel vous guide à travers le flux complet de **aspose psd font substitution**, depuis la configuration de votre projet jusqu'à l'exportation de l'image mise à jour, afin que vous puissiez gérer de manière fiable les scénarios de polices manquantes PSD sans ouvrir Photoshop.

## Réponses rapides
- **Quelle bibliothèque gère la substitution de polices ?** Aspose.PSD for Java  
- **Combien de temps prend l'implémentation ?** Environ 5‑10 minutes pour un scénario de base  
- **Quelle police est utilisée comme secours par défaut ?** Vous pouvez définir n'importe quelle police TrueType, par ex., « Arial »  
- **Puis-je enregistrer dans d'autres formats que PNG ?** Oui – PSD, JPEG, BMP, etc., sont pris en charge  
- **Ai-je besoin d'une licence pour la production ?** Une licence valide Aspose.PSD est requise pour une utilisation non‑essai  

## Qu'est-ce que la substitution de polices Aspose PSD ?

La substitution de polices Aspose PSD est le processus de spécification d'une police de substitution que la bibliothèque utilisera chaque fois qu'elle rencontrera une police manquante ou non prise en charge dans un fichier PSD. Cela garantit que les calques de texte sont rendus correctement sans édition manuelle dans Photoshop et vous permet de **handle missing fonts PSD** automatiquement.

## Pourquoi utiliser Aspose.PSD pour Java ?

- **Gestion complète des PSD** – les calques, masques, effets et texte sont tous accessibles via l'API.  
- **Cross‑platform** – fonctionne sur tout OS supportant Java.  
- **Aucune dépendance externe** – la bibliothèque gère la substitution de polices en interne, vous n'avez donc pas besoin d'inclure des polices supplémentaires avec votre application.  

## Comment remplacer les polices manquantes dans un PSD avec Aspose PSD

Voici un guide étape par étape qui montre **how to replace missing fonts PSD** fichiers avec une police de secours personnalisée.

## Pré-requis

Avant de commencer, assurez-vous d'avoir :

- **Java Development Kit (JDK)** – version 8 ou supérieure installée.  
- **Aspose.PSD for Java** – téléchargez le dernier JAR depuis la [release page](https://releases.aspose.com/psd/java/).  
- **Un IDE** – IntelliJ IDEA, Eclipse, ou tout éditeur de votre choix.  

## Importer les packages

Commencez par importer les classes dont vous avez besoin. Cela vous donne accès au chargement d'images, aux options de chargement et aux fonctionnalités d'enregistrement.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Étape 1 : Définir le répertoire du document

Définissez le dossier contenant le fichier PSD source. Remplacez le texte de remplacement par le chemin réel sur votre machine.

```java
String dataDir = "Your Document Directory";
```

## Étape 2 : Charger l'image avec une police de remplacement

Créez une instance de `PsdLoadOptions`, spécifiez la police de remplacement par défaut (par ex., **Arial**), puis chargez le PSD. Aspose appliquera automatiquement la police de secours chaque fois qu'il rencontrera une police manquante.

```java
PsdLoadOptions psdLoadOptions = new PsdLoadOptions(); 
psdLoadOptions.setDefaultReplacementFont("Arial");

PsdImage psdImage = (PsdImage)Image.load(dataDir + "Cloud_AzPlat_Banner3A_SB_EN_US_160x600_chinese_font.psd", psdLoadOptions);
```

## Étape 3 : Enregistrer l'image remplacée

Après la substitution de police, vous pouvez exporter l'image dans n'importe quel format pris en charge. Ici nous l'enregistrons en PNG, mais vous pouvez également choisir JPEG, BMP, ou même le réécrire en PSD.

```java
PngOptions pngOptions = new PngOptions();
psdImage.save(dataDir + "replaced_font.png", pngOptions);
```

## Problèmes courants et solutions

| Problème | Cause | Solution |
|----------|-------|----------|
| Le texte apparaît illisible après le remplacement | La police de secours ne contient pas les glyphes requis | Choisissez une police qui prend en charge la plage Unicode nécessaire (par ex., « Arial Unicode MS »). |
| `OutOfMemoryError` sur de gros PSD | Chargement d'un fichier très haute résolution sans assez de mémoire heap | Augmentez la taille du heap JVM (`-Xmx2g`) ou chargez l'image en mode streaming si disponible. |
| Exception de licence | Utilisation de la version d'essai en production | Appliquez une licence permanente ou temporaire valide avant de charger l'image. |

## Questions fréquentes

**Q : Puis-je remplacer les polices dans d'autres formats d'image que le PSD ?**  
R : Oui. Bien que le cas d'utilisation principal soit le PSD, Aspose.PSD prend également en charge PNG, JPEG, BMP et TIFF, permettant le remplacement de polices lorsque des calques de texte existent.

**Q : La police de remplacement par défaut est‑elle obligatoire ?**  
R : Non. Vous pouvez définir n'importe quelle police TrueType que vous préférez, ou omettre ce paramètre pour laisser Aspose utiliser son défaut interne.

**Q : Y a‑t‑il des exigences de licence pour utiliser Aspose.PSD ?**  
R : Une licence commerciale est requise pour les déploiements en production. Consultez la [purchase page](https://purchase.aspose.com/buy) pour plus de détails.

**Q : Puis‑je obtenir une licence temporaire pour les tests ?**  
R : Absolument. Aspose propose des licences temporaires gratuites pour l'évaluation – consultez la [temporary license page](https://purchase.aspose.com/temporary-license/).

**Q : Où puis‑je trouver un support supplémentaire ou discuter des problèmes liés à Aspose.PSD ?**  
R : Le forum communautaire est un excellent endroit pour poser des questions : [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

**Q : Comment gérer les fichiers PSD contenant plusieurs polices manquantes ?**  
R : Définissez la police de remplacement par défaut une fois (comme indiqué) – elle sera appliquée à *toutes* les polices manquantes lors de l'opération de chargement.

**Q : Est‑il possible de remplacer les polices après que l'image a été enregistrée ?**  
R : La substitution de police doit se faire pendant la phase de chargement. Pour changer les polices plus tard, rechargez le PSD avec une police de remplacement différente et réenregistrez‑le.

## Conclusion

Vous avez maintenant vu un flux complet de **aspose psd font substitution** en Java — de l'importation des bonnes classes, la configuration d'une police de secours, le chargement du PSD, à l'exportation de l'image corrigée. Intégrez ce modèle dans vos pipelines de traitement d'images pour garantir une typographie cohérente sur tous vos actifs PSD et pour **handle missing fonts PSD** automatiquement.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Dernière mise à jour :** 2026-02-09  
**Testé avec :** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Auteur :** Aspose  

---