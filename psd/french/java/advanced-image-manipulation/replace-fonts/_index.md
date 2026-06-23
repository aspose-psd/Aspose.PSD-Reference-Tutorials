---
date: 2026-06-23
description: Découvrez comment enregistrer un PSD au format PNG, remplacer les polices
  manquantes et exporter des images avec Aspose.PSD pour Java – gérez rapidement les
  fichiers PSD contenant des polices manquantes.
keywords:
- save psd as png
- how to replace fonts
- convert psd to bmp
- export psd to jpeg
- handle missing fonts psd
linktitle: Remplacer les polices
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to save PSD as PNG, replace missing fonts, and export images
    using Aspose.PSD for Java – handle missing fonts PSD files quickly.
  headline: How to Save PSD as PNG and Replace Missing Fonts in Java with Aspose
  type: TechArticle
- questions:
  - answer: Yes. While the primary use‑case is PSD, Aspose.PSD also supports PNG,
      JPEG, BMP, and TIFF, allowing font replacement wherever text layers exist.
    question: Can I replace fonts in other image formats besides PSD?
  - answer: No. You can set any TrueType font you prefer, or omit the setting to let
      Aspose use its internal default.
    question: Is the default replacement font mandatory?
  - answer: A commercial license is required for production deployments. See the [purchase
      page](https://purchase.aspose.com/buy) for details.
    question: Are there licensing requirements for using Aspose.PSD?
  - answer: Absolutely. Aspose offers free temporary licenses for evaluation – visit
      the [temporary license page](https://purchase.aspose.com/temporary-license/).
    question: Can I obtain a temporary license for testing?
  - answer: 'The community forum is a great place to ask questions: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).'
    question: Where can I find additional support or discuss Aspose.PSD‑related issues?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Comment enregistrer un PSD au format PNG et remplacer les polices manquantes
  en Java avec Aspose
url: /fr/java/advanced-image-manipulation/replace-fonts/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# enregistrer psd en png – Remplacer les polices manquantes en Java

## Introduction

Si vous devez **enregistrer PSD en PNG** tout en remplaçant les polices manquantes ou indésirables à l'intérieur d'un fichier Photoshop (PSD), la substitution de polices Aspose PSD rend cela simple. Dans les applications Java, vous pouvez charger un PSD, indiquer à Aspose la police de secours à utiliser, puis exporter l'image corrigée dans le format de votre choix. Ce tutoriel vous guide à travers le flux de travail complet — de la configuration du projet à l'exportation du PNG mis à jour — afin que vous puissiez gérer de manière fiable les scénarios **handle missing fonts PSD** sans jamais ouvrir Photoshop.

## Réponses rapides

- **Quelle bibliothèque gère la substitution de polices ?** Aspose.PSD for Java  
- **Combien de temps prend l'implémentation ?** Environ 5‑10 minutes pour un scénario de base  
- **Quelle police est utilisée comme police de secours par défaut ?** Vous pouvez définir n'importe quelle police TrueType, par ex., “Arial”  
- **Puis-je enregistrer dans d'autres formats que PNG ?** Oui – PSD, JPEG, BMP et plus sont pris en charge  
- **Ai‑je besoin d'une licence pour la production ?** Une licence valide Aspose.PSD est requise pour une utilisation non‑trial  

## Qu'est‑ce que la substitution de polices Aspose PSD ?

La substitution de polices Aspose PSD est le processus de spécification d'une police de remplacement que la bibliothèque utilisera chaque fois qu'elle rencontrera une police manquante ou non prise en charge dans un fichier PSD. Cela garantit que les calques de texte sont rendus correctement sans édition manuelle dans Photoshop et vous permet de **handle missing fonts PSD** automatiquement.

## Pourquoi utiliser Aspose.PSD pour Java ?

Aspose.PSD for Java fournit une solution complète et haute performance pour travailler avec les fichiers Photoshop directement depuis le code Java, éliminant ainsi le besoin de Photoshop lui‑même. Il prend en charge un large éventail de types de calques, d'effets et de tailles de fichiers importantes tout en offrant des API simples pour des tâches telles que la substitution de polices, la conversion d'images et la gestion des métadonnées.

- **Gestion complète des PSD** – Aspose.PSD prend en charge **plus de 30 types de calques**, **plus de 20 effets**, et peut traiter des fichiers jusqu'à **2 GB** sans charger l'intégralité du document en mémoire.  
- **Multiplateforme** – fonctionne sur tout OS supportant Java 8+.  
- **Aucune dépendance externe** – la bibliothèque gère la substitution de polices en interne, vous n'avez donc pas besoin d'inclure des polices supplémentaires avec votre application.  

## Comment remplacer les polices manquantes dans un PSD avec Aspose PSD

Pour remplacer les polices manquantes, vous chargez d'abord le PSD avec une police de secours définie dans les options de chargement, puis vous rendez ou enregistrez l'image. La bibliothèque substitue automatiquement les polices manquantes par celle que vous avez spécifiée, garantissant que le rendu visuel correspond à vos attentes sans édition manuelle.

## Prérequis

- **Java Development Kit (JDK)** – version 8 ou supérieure installée.  
- **Aspose.PSD for Java** – téléchargez le dernier JAR depuis la [release page](https://releases.aspose.com/psd/java/).  
- **Un IDE** – IntelliJ IDEA, Eclipse ou tout éditeur de votre choix.  

## Importer les packages

La classe `PsdImage` représente un document Photoshop en mémoire, offrant l'accès aux calques, au texte et aux capacités de rendu. `PsdLoadOptions` contrôle la façon dont le fichier est lu, y compris la police de secours, tandis que `SaveOptions` (ou les sous‑classes spécifiques au format) définissent comment l'image est écrite.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Étape 1 : Définir le répertoire de votre document

Spécifiez le dossier contenant le fichier PSD source. Remplacez le texte de substitution par le chemin réel sur votre machine.

L'objet `File` pointe simplement vers le PSD que vous souhaitez traiter ; aucune configuration supplémentaire n'est requise ici.  

```java
String dataDir = "Your Document Directory";
```

## Étape 2 : Charger l'image avec une police de remplacement

Créez une instance de `PsdLoadOptions`, définissez la police de remplacement par défaut (par ex., **Arial**), et chargez le PSD. Aspose appliquera automatiquement la police de secours chaque fois qu'une police manquante sera rencontrée.

`PsdLoadOptions` vous permet de définir le comportement de chargement, y compris la police de secours qui remplace toute police manquante pendant la phase d'importation.  

```java
PsdLoadOptions psdLoadOptions = new PsdLoadOptions(); 
psdLoadOptions.setDefaultReplacementFont("Arial");

PsdImage psdImage = (PsdImage)Image.load(dataDir + "Cloud_AzPlat_Banner3A_SB_EN_US_160x600_chinese_font.psd", psdLoadOptions);
```

## Étape 3 : Enregistrer l'image remplacée en PNG

Après la substitution de police, vous pouvez exporter l'image dans n'importe quel format pris en charge. Ici nous l'enregistrons en PNG, mais vous pourriez également choisir JPEG, BMP ou même le réécrire en PSD.

La méthode `save` de `PsdImage` accepte un objet `SaveOptions` ; en utilisant `PngOptions`, vous obtenez un PNG sans perte adapté au web ou à un traitement ultérieur.  

```java
PngOptions pngOptions = new PngOptions();
psdImage.save(dataDir + "replaced_font.png", pngOptions);
```

## Comment enregistrer un PSD en PNG après avoir remplacé les polices ?

Chargez le PSD avec une police de secours, puis appelez `psdImage.save("output.png", new PngOptions())`. Cette opération d'enregistrement en une seule ligne crée un PNG entièrement rendu reflétant la police substituée, vous permettant d'intégrer l'image où vous le souhaitez sans vous soucier des polices manquantes. Assurez‑vous d'avoir appliqué la police de remplacement avant l'enregistrement, et ajustez éventuellement les paramètres de compression PNG via l'objet `PngOptions` pour une taille de fichier optimale.

## Problèmes courants et solutions

| Problème | Cause | Solution |
|----------|-------|----------|
| Le texte apparaît illisible après le remplacement | La police de secours ne contient pas les glyphes requis | Choisissez une police qui prend en charge la plage Unicode nécessaire (par ex., “Arial Unicode MS”). |
| `OutOfMemoryError` sur de gros PSD | Chargement d'un fichier très haute résolution sans assez de mémoire heap | Augmentez la taille du heap JVM (`-Xmx2g`) ou chargez l'image en mode streaming si disponible. |
| Exception de licence | Utilisation de la version d'essai en production | Appliquez une licence permanente ou temporaire valide avant de charger l'image. |

## Questions fréquentes

**Q : Puis‑je remplacer les polices dans d'autres formats d'image que le PSD ?**  
R : Oui. Bien que le cas d'utilisation principal soit le PSD, Aspose.PSD prend également en charge PNG, JPEG, BMP et TIFF, permettant le remplacement de police partout où des calques de texte existent.

**Q : La police de remplacement par défaut est‑elle obligatoire ?**  
R : Non. Vous pouvez définir n'importe quelle police TrueType que vous préférez, ou omettre ce paramètre pour laisser Aspose utiliser son défaut interne.

**Q : Existe‑t‑il des exigences de licence pour l'utilisation d'Aspose.PSD ?**  
R : Une licence commerciale est requise pour les déploiements en production. Consultez la [purchase page](https://purchase.aspose.com/buy) pour plus de détails.

**Q : Puis‑je obtenir une licence temporaire pour les tests ?**  
R : Absolument. Aspose propose des licences temporaires gratuites pour l'évaluation – rendez‑vous sur la [temporary license page](https://purchase.aspose.com/temporary-license/).

**Q : Où puis‑je trouver un support supplémentaire ou discuter des problèmes liés à Aspose.PSD ?**  
R : Le forum communautaire est un excellent endroit pour poser des questions : [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

**Q : Comment gérer les fichiers PSD contenant plusieurs polices manquantes ?**  
R : Définissez la police de remplacement par défaut une seule fois (comme indiqué) – elle sera appliquée à *toutes* les polices manquantes lors de l'opération de chargement.

**Q : Est‑il possible de remplacer les polices après que l'image a été enregistrée ?**  
R : La substitution de police doit se faire pendant la phase de chargement. Pour changer les polices plus tard, rechargez le PSD avec une police de remplacement différente et réenregistrez.

## Conclusion

Vous avez maintenant découvert un flux complet **enregistrer psd en png** en Java — de l'importation des bonnes classes, à la configuration d'une police de secours, le chargement du PSD, jusqu'à l'exportation du PNG corrigé. Intégrez ce modèle dans vos pipelines de traitement d'images pour garantir une typographie cohérente sur tous vos actifs PSD et pour **handle missing fonts PSD** automatiquement.

---

**Dernière mise à jour :** 2026-06-23  
**Testé avec :** Aspose.PSD for Java 24.12 (dernière version au moment de la rédaction)  
**Auteur :** Aspose

## Tutoriels associés

- [Paramètres pour remplacer les polices manquantes dans Aspose.PSD pour Java](/psd/java/advanced-techniques/settings-replacing-missing-fonts/)
- [Enregistrer PSD en PNG et appliquer une ombre portée lors du rendu dans Aspose.PSD pour Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Comment convertir PSD en PNG et redimensionner proportionnellement avec Aspose.PSD pour Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}