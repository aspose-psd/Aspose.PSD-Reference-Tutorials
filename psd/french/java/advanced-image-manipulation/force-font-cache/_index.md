---
date: 2025-12-01
description: Apprenez comment enregistrer un fichier PSD, forcer le cache des polices
  et améliorer les performances d’image en utilisant Aspose.PSD pour Java. Guide étape
  par étape pour l’optimisation du traitement d’image.
linktitle: Force Font Cache
second_title: Aspose.PSD Java API
title: Comment enregistrer un fichier PSD et forcer le cache des polices avec Aspose.PSD
  pour Java
url: /fr/java/advanced-image-manipulation/force-font-cache/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment enregistrer un fichier PSD et forcer le cache des polices avec Aspose.PSD pour Java

## Introduction

Si vous avez besoin d'**enregistrer des fichiers PSD** rapidement tout en vous assurant que les bonnes polices sont disponibles, vous êtes au bon endroit. Le cache des polices peut améliorer considérablement les **performances d'image**, surtout lorsque vous traitez de gros documents Photoshop de façon répétée. Dans ce tutoriel, nous passerons en revue les étapes exactes pour forcer le cache des polices, charger une image PSD, et enfin **enregistrer le fichier PSD** avec les nouvelles polices installées en utilisant Aspose.PSD pour Java.

## Quick Answers
- **Que fait le forçage du cache des polices ?** Il force Aspose.PSD à re‑scanner les polices du système afin que les nouvelles polices installées soient reconnues instantanément.  
- **Combien de temps dois‑je attendre pour qu’une police s’installe ?** Le code d’exemple fait une pause de **2 minutes**, ce qui est généralement suffisant pour une installation manuelle.  
- **Puis‑je l’utiliser avec n’importe quel fichier PSD ?** Oui – tant que le fichier est accessible et que les polices requises sont installées sur le système.  
- **Ai‑je besoin d’une licence pour exécuter ce code ?** Une licence temporaire ou complète est requise pour une utilisation en production ; un essai gratuit suffit pour l’évaluation.  
- **Quelles versions de Java sont prises en charge ?** Aspose.PSD pour Java fonctionne avec JDK 8 et versions ultérieures.

## What is “save PSD file” and why does it matter?

Enregistrer un fichier PSD après avoir manipulé ses calques, son texte ou ses polices est l’étape finale qui persiste vos modifications. Lorsque le cache des polices n’est pas à jour, le fichier enregistré peut revenir aux polices par défaut, entraînant des incohérences visuelles. En forçant d’abord le cache, vous garantissez que l’opération **enregistrer le fichier PSD** intègre les bonnes polices.

## Why force the font cache with Aspose.PSD?

- **Gain de performance** – Réduit le besoin de recherches de polices répétées.  
- **Fiabilité** – Garantit que les fichiers PSD enregistrés s’affichent exactement comme prévu sur n’importe quelle machine.  
- **Simplicité** – Un seul appel de méthode (`OpenTypeFontsCache.updateCache()`) gère le travail lourd.

## Prerequisites

Avant de commencer, assurez-vous d’avoir :

- Java Development Kit (JDK) 8 ou version ultérieure installé.  
- Bibliothèque Aspose.PSD pour Java (téléchargez depuis le [lien de téléchargement](https://releases.aspose.com/psd/java/)).  
- Un fichier PSD d’exemple (`sample.psd`) placé dans un dossier que vous pouvez référencer depuis votre code.  

Maintenant que tout est prêt, plongeons dans l’implémentation.

## Import Packages

Tout d’abord, importez les classes nécessaires pour travailler avec les images PSD et le cache des polices. Placez ces déclarations en haut de votre classe Java :

```java
import com.aspose.psd.Image;
import com.aspose.psd.OpenTypeFontsCache;

import com.aspose.psd.fileformats.psd.PsdImage;
import java.io.Console;
import java.util.concurrent.TimeUnit;
```

### Step 1: Load the PSD Image (How to load PSD)

Nous commençons par charger le fichier PSD original. Cela nous fournit un objet image de base que nous pourrons ensuite ré‑enregistrer après la mise à jour du cache des polices.

```java
String dataDir = "Your Document Directory";

PsdImage image = (PsdImage)Image.load(dataDir + "sample.psd");
image.save(dataDir + "NoFont.psd");
```

- **Explanation:**  
  - `Image.load` lit le fichier en mémoire.  
  - `image.save` crée une copie nommée **NoFont.psd** qui reflète l’état **avant** que de nouvelles polices soient disponibles.  
  - Cette étape est utile pour la comparaison et garantit que la mise à jour du cache suivante modifie réellement le résultat.

### Step 2: Wait for Font Installation (Improve image performance)

Nous donnons maintenant à l’utilisateur le temps d’installer manuellement la police requise. Dans un scénario réel, vous pourriez automatiser cette étape, mais la pause montre le mécanisme de rafraîchissement du cache.

```java
System.out.println("You have 2 minutes to install the font");
Thread.sleep(2 * 60 * 1000);
OpenTypeFontsCache.updateCache();
```

- **Explanation:**  
  - `Thread.sleep` suspend l’exécution pendant **2 minutes** (2 × 60 × 1000 ms).  
  - `OpenTypeFontsCache.updateCache()` force Aspose.PSD à re‑scanner les polices OpenType du système, rendant immédiatement disponibles les nouvelles polices installées pour le rendu.

### Step 3: Load the Updated PSD Image (Load PSD image) and **save PSD file**

Après le rafraîchissement du cache, nous chargeons à nouveau le PSD original. Cette fois les informations de police sont à jour, et nous pouvons **enregistrer le fichier PSD** avec la bonne police.

```java
PsdImage image1 = (PsdImage)Image.load(dataDir + "sample.psd");
image1.save(dataDir + "HasFont.psd");
```

- **Explanation:**  
  - Le deuxième chargement prend en compte la police nouvellement installée.  
  - En enregistrant sous **HasFont.psd**, on obtient un fichier contenant maintenant le rendu correct de la police, confirmant que la mise à jour du cache a fonctionné.

## Common Issues and Solutions

| Problème | Raison | Solution |
|----------|--------|----------|
| Le PSD enregistré affiche toujours la police par défaut | Police non installée dans un emplacement scanné par le système d’exploitation | Installez la police dans le dossier des polices du système (par ex., `C:\Windows\Fonts` sous Windows) et relancez `updateCache()`. |
| `Thread.sleep` lève `InterruptedException` | La signature de la méthode ne gère pas les exceptions vérifiées | Ajoutez `throws InterruptedException` à votre méthode `main` ou encapsulez l’appel dans un bloc try‑catch. |
| `OpenTypeFontsCache.updateCache()` ne fait rien | Exécution sur un serveur sans affichage (headless) sans configuration de polices | Assurez‑vous que le serveur a les polices requises installées et que le processus Java a la permission de les lire. |

## Frequently Asked Questions

**Q : Aspose.PSD est‑il compatible avec toutes les versions de Java ?**  
R : Aspose.PSD pour Java prend en charge JDK 8 et versions ultérieures, couvrant la majorité des applications Java modernes.

**Q : Puis‑je utiliser Aspose.PSD pour des projets commerciaux ?**  
R : Oui. Une licence commerciale est requise pour une utilisation en production. Vous pouvez en obtenir une sur la [page d’achat](https://purchase.aspose.com/buy).

**Q : Une version d’essai gratuite est‑elle disponible ?**  
R : Absolument ! Téléchargez une version d’essai depuis la [page des releases](https://releases.aspose.com/).

**Q : Où puis‑je trouver du support communautaire ?**  
R : Rejoignez la discussion sur le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour des astuces et du dépannage.

**Q : Comment obtenir une licence temporaire pour les tests ?**  
R : Consultez la [page de licence temporaire](https://purchase.aspose.com/temporary-license/) pour demander une licence à court terme.

## Conclusion

Vous avez maintenant appris comment **enregistrer le fichier PSD** après avoir forcé le cache des polices, garantissant que vos sorties PSD s’affichent avec les bonnes polices à chaque fois. Cette technique est simple mais puissante pour l’**optimisation du traitement d’image** et peut être intégrée à des flux de travail plus grands nécessitant une manipulation fiable et haute performance des PSD.

---

**Dernière mise à jour :** 2025-12-01  
**Testé avec :** Aspose.PSD for Java 24.12 (dernière version au moment de la rédaction)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}