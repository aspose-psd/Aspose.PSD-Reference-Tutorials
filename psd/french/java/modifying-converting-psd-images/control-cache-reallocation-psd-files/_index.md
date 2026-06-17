---
date: 2026-03-13
description: Apprenez à créer des projets Java d'images PSD tout en gérant la réallocation
  du cache avec Aspose.PSD pour Java. Optimisez efficacement l’utilisation de la mémoire
  et du disque.
linktitle: Create PSD Image Java – Control Cache Reallocation
second_title: Aspose.PSD Java API
title: Créer une image PSD Java – Contrôler la réallocation du cache
url: /fr/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
weight: 22
---

 -> "Étape 1 : Configuration du répertoire de données". Keep "Step 1:" maybe "Étape 1 :".

Make sure to preserve colon and formatting.

Translate bullet points accordingly.

Now produce final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Contrôler la réallocation du cache dans les fichiers PSD

## Introduction
Si vous devez **create PSD image java** des projets efficacement, contrôler la réallocation du cache est essentiel. Lorsqu’on travaille avec des images et des fichiers Photoshop de manière programmatique, l’efficacité est un facteur clé. Aspose.PSD for Java offre des fonctionnalités robustes pour gérer et manipuler les fichiers PSD de façon transparente. L’un des aspects fondamentaux de l’optimisation des performances est le contrôle de la réallocation du cache. La gestion du cache aide à maintenir l’équilibre entre l’utilisation de la mémoire et du disque, garantissant que votre application fonctionne sans plantages inattendus ni ralentissements.

## Réponses rapides
- **Que fait la réallocation du cache ?** Elle équilibre l’utilisation de la mémoire et du disque lors du traitement de gros fichiers PSD.  
- **Quel type de cache est le meilleur pour les grandes images ?** `CacheOnDiskOnly` libère la mémoire en stockant le cache sur le disque.  
- **Quelle quantité d’espace disque puis‑je allouer ?** Jusqu’à 1 GB (ou toute taille que vous définissez avec `setMaxDiskSpaceForCache`).  
- **Ai‑je besoin d’une licence pour utiliser ces fonctionnalités ?** Une licence supprime les limitations de la version d’essai ; voir la page d’achat d’Aspose.  
- **Puis‑je surveiller l’utilisation du cache à l’exécution ?** Oui, utilisez `Cache.getAllocatedDiskBytesCount()` et `Cache.getAllocatedMemoryBytesCount()`.

## Pourquoi contrôler la réallocation du cache ?
La gestion du cache est cruciale lorsque vous **create PSD image java** des applications qui manipulent des fichiers haute résolution ou multi‑couches. Des paramètres de cache appropriés préviennent les erreurs de dépassement de mémoire, réduisent les pauses du GC et offrent des performances prévisibles sur les serveurs ou les applications de bureau.

## Pré‑requis
Avant de plonger dans la partie codage, assurez‑vous que les points suivants sont en place pour que tout fonctionne correctement :
1. Java Development Kit (JDK) : Assurez‑vous d’avoir le JDK installé sur votre machine. Vous pouvez le télécharger depuis [le site d’Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD for Java : Vous devez télécharger la bibliothèque Aspose.PSD. Vous pouvez trouver la dernière version [ici](https://releases.aspose.com/psd/java/).
3. Configuration de l’IDE : Un environnement de développement intégré (IDE) comme IntelliJ IDEA ou Eclipse facilitera la gestion de votre code.
4. Connaissances de base en Java : Une familiarité avec la programmation Java vous aidera à comprendre les concepts et les extraits de code.
5. Licence Aspose (Optionnel) : Si vous souhaitez supprimer les filigranes et obtenir toutes les fonctionnalités, envisagez d’acheter une licence [ici](https://purchase.aspose.com/buy) ou d’essayer la version d’évaluation gratuite [ici](https://releases.aspose.com/).

## Importer les packages
Avant de commencer à écrire le code, assurons‑nous que les packages nécessaires sont importés. Voici une brève liste de ce qu’il faut inclure au début de votre fichier Java :
```java
import com.aspose.psd.Cache;
import com.aspose.psd.CacheType;
import com.aspose.psd.Color;
import com.aspose.psd.ColorPalette;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.imageoptions.GifOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.MemoryStream;
```

## Comment créer une image PSD Java avec contrôle du cache
Voici un guide étape par étape qui lie la configuration du cache directement au processus de création d’une image PSD en Java.

### Étape 1 : Configuration du répertoire de données
Tout d’abord, vous devez configurer un répertoire où vous souhaitez que vos fichiers de cache soient stockés. C’est essentiel pour gérer le cache efficacement.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- `String dataDir` : Définit le répertoire pour le cache de votre document.  
- `Cache.setCacheFolder(dataDir)` : Cette méthode définit le dossier de cache sur le répertoire spécifié. Tout cache créé par Aspose sera désormais stocké ici au lieu du répertoire temporaire par défaut.

### Étape 2 : Configuration du cache sur disque
Ensuite, nous préciserons que nous voulons que notre cache soit stocké uniquement sur le disque. Cela est particulièrement utile si votre application utilise de gros fichiers et que vous souhaitez libérer la mémoire.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- `Cache.setCacheType(CacheType.CacheOnDiskOnly)` : Cette option garantit que le cache n’est pas conservé en mémoire, ce qui est bénéfique pour le traitement de gros fichiers PSD sans consommer trop de RAM.

### Étape 3 : Définition de la taille maximale du cache disque et mémoire
Maintenant, limitons la taille de nos caches. C’est crucial car un cache illimité peut entraîner des problèmes de performance.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabyte
Cache.setMaxMemoryForCache(1073741824); // 1 gigabyte
```

- `Cache.setMaxDiskSpaceForCache(1073741824)` : Définit une limite de 1 GB pour le cache sur le disque. Vous pouvez ajuster cette taille selon vos besoins.  
- `Cache.setMaxMemoryForCache(1073741824)` : De même, cela limite le cache en mémoire, assurant que votre application n’utilise pas une mémoire excessive.

### Étape 4 : Gestion de la stratégie de réallocation du cache
Gérer la façon dont le cache est réalloué est essentiel pour maintenir les performances. Voici comment le configurer.
```java
Cache.setExactReallocateOnly(false);
```

- `Cache.setExactReallocateOnly(false)` : Lorsqu’il est réglé sur `false`, cela permet à Aspose de gérer la réallocation du cache de façon plus flexible, ce qui peut améliorer les performances.

### Étape 5 : Vérification de la taille du cache allouée
Cette étape consiste à surveiller le nombre d’octets actuellement alloués pour le cache en mémoire ou sur le disque. Implémentons cela :
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- `long l1` : Stocke le nombre d’octets alloués sur le disque.  
- `long l2` : Stocke le nombre d’octets alloués en mémoire.  
Vous pouvez vérifier ces valeurs à tout moment pour vous assurer que votre application gère correctement l’utilisation de la mémoire et du disque.

### Étape 6 : Création d’une image PSD
Maintenant que nos configurations de cache sont en place, créons une image PSD simple.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- `PsdOptions options` : Cet objet vous permet de spécifier des options lors de la création d’une image Photoshop.  
- `Color[] color` : Un tableau contenant les couleurs qui seront utilisées dans la palette de l’image.

### Étape 7 : Enregistrement des données de pixels dans l’image
Maintenant, remplissons notre image avec des données de pixels et enregistrons‑la.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- `Color[] pixels` : Il s’agit d’un tableau d’objets couleur. Ici, nous le remplissons de pixels blancs.  
- `image.savePixels(image.getBounds(), pixels)` : Cette méthode enregistre les données de pixels dans l’image. Elle met à jour l’image avec les couleurs que nous avons définies.

### Étape 8 : Surveillance du cache alloué après la création de l’image
Après la création de l’image, il est judicieux de vérifier à nouveau le nombre d’octets alloués pour le cache.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- `long diskBytes` : Capture l’allocation actuelle sur le disque après la création de l’image.  
- `long memoryBytes` : Capture l’allocation actuelle en mémoire.  
Cette étape vous aidera à déterminer la quantité de cache consommée après vos opérations.

### Étape 9 : Vérification de la libération correcte des ressources
Enfin, il est crucial de s’assurer que tous les objets Aspose.PSD ont été correctement libérés afin d’éviter les fuites de mémoire.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- `l1` et `l2` : Ces variables vous aideront à vérifier l’allocation finale. Si elles ne sont pas à zéro, cela indique que certains objets n’ont pas été correctement libérés.

## Problèmes courants et solutions
- **Dossier de cache non créé** – Vérifiez que l’application possède les droits d’écriture pour le chemin que vous avez passé à `Cache.setCacheFolder`.  
- **Erreurs de dépassement de mémoire** – Assurez‑vous que `Cache.setCacheType(CacheType.CacheOnDiskOnly)` est appliqué avant de charger de gros fichiers PSD.  
- **Taille de cache inattendue** – Utilisez les méthodes `Cache.getAllocated*BytesCount()` après chaque opération majeure pour suivre la croissance.

## FAQ

**Q : Qu’est‑ce qu’Aspose.PSD ?**  
R : Aspose.PSD est une bibliothèque pour les développeurs .NET et Java permettant de créer, manipuler et convertir des fichiers Photoshop (PSD) de façon programmatique.

**Q : Comment vérifier la taille du cache allouée ?**  
R : Utilisez des méthodes comme `Cache.getAllocatedDiskBytesCount()` et `Cache.getAllocatedMemoryBytesCount()` pour surveiller l’utilisation actuelle du cache.

**Q : Puis‑je définir un répertoire personnalisé pour le cache ?**  
R : Oui, vous pouvez spécifier un autre répertoire en utilisant `Cache.setCacheFolder("Your Directory Path")`.

**Q : Aspose.PSD est‑il gratuit ?**  
R : Aspose.PSD est une bibliothèque payante, mais vous pouvez commencer avec une version d’essai gratuite disponible sur leur [site web](https://releases.aspose.com/).

**Q : Que se passe‑t‑il si je ne libère pas les objets ?**  
R : Ne pas libérer les objets peut entraîner des fuites de mémoire, faisant que votre application utilise plus de ressources que nécessaire.

## Conclusion
Contrôler la réallocation du cache pendant que vous **create PSD image java** des applications peut faire une différence significative en termes de performances. En suivant les étapes ci‑dessus, vous gérerez le cache efficacement, réduirez la consommation de mémoire et générerez des fichiers PSD de haute qualité avec Aspose.PSD for Java. Appliquez ces techniques, et vos projets seront plus fluides et plus évolutifs.

---

**Dernière mise à jour :** 2026-03-13  
**Testé avec :** Aspose.PSD for Java (dernière version)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}