---
title: Contrôler la réallocation du cache dans les fichiers PSD
linktitle: Contrôler la réallocation du cache dans les fichiers PSD
second_title: API Java Aspose.PSD
description: Gérez la réallocation du cache dans les fichiers PSD à l'aide d'Aspose.PSD pour Java. Découvrez comment optimiser efficacement la mémoire et la gestion des fichiers, idéal pour les développeurs.
type: docs
weight: 22
url: /fr/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
---
## Introduction
Lorsque vous travaillez avec des images et des fichiers Photoshop par programmation, l'efficacité est un facteur clé. Aspose.PSD pour Java offre des fonctionnalités robustes pour gérer et manipuler les fichiers PSD de manière transparente. L'un des aspects fondamentaux de l'optimisation des performances consiste à contrôler la réallocation du cache. La gestion du cache aide à maintenir l'équilibre entre l'utilisation de la mémoire et du disque, garantissant ainsi le bon fonctionnement de votre application, sans pannes ni ralentissements inattendus. 
## Conditions préalables
Avant de passer à la partie codage, vous devez vous assurer de quelques points pour que tout se passe bien :
1. Kit de développement Java (JDK) : assurez-vous que JDK est installé sur votre ordinateur. Vous pouvez le télécharger depuis[Le site d'Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD pour Java : vous devez télécharger la bibliothèque Aspose.PSD. Vous pouvez trouver la dernière version[ici](https://releases.aspose.com/psd/java/).
3. Configuration de l'IDE : un environnement de développement intégré (IDE) comme IntelliJ IDEA ou Eclipse vous facilitera la gestion de votre code.
4. Compréhension de base de Java : la familiarité avec la programmation Java vous aidera à mieux comprendre les concepts et les extraits de code.
5.  Licence Aspose (facultatif) : si vous souhaitez supprimer les filigranes et bénéficier de toutes les fonctionnalités, envisagez d'acheter une licence[ici](https://purchase.aspose.com/buy) ou essayer l'essai gratuit[ici](https://releases.aspose.com/).
## Importer des packages
Avant de commencer à écrire le code, assurons-nous que les packages nécessaires sont importés. Vous trouverez ci-dessous une brève liste de ce qu'il faut inclure au début de votre fichier Java :
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
## Étape 1 : configuration de votre répertoire de données
Tout d’abord, vous devrez configurer un répertoire dans lequel vous souhaitez que vos fichiers de cache soient stockés. Ceci est essentiel pour gérer efficacement le cache.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- String dataDir : définissez le répertoire de votre cache de documents.
- Cache.setCacheFolder(dataDir) : cette méthode définit le dossier de cache sur le répertoire spécifié. Tout cache créé par Aspose sera désormais stocké ici au lieu du répertoire temporaire par défaut.
## Étape 2 : configuration du cache sur le disque
Ensuite, nous préciserons que nous souhaitons que notre cache soit stocké uniquement sur disque. Ceci est particulièrement utile si votre application utilise des fichiers volumineux et que vous souhaitez vous assurer que la mémoire reste libre.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- Cache.setCacheType(CacheType.CacheOnDiskOnly) : cette option garantit que le cache n'est pas conservé en mémoire, ce qui est avantageux pour gérer des fichiers PSD volumineux sans consommer trop de RAM.
## Étape 3 : Définition de la taille maximale du disque et du cache mémoire
Maintenant, limitons la taille de notre cache. Ceci est crucial car un cache illimité peut entraîner des problèmes de performances.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigaoctet
Cache.setMaxMemoryForCache(1073741824); // 1 gigaoctet
```

- Cache.setMaxDiskSpaceForCache(1073741824) : cela définit une limite de 1 Go pour le cache sur le disque. Vous pouvez ajuster cette taille en fonction de vos besoins.
- Cache.setMaxMemoryForCache(1073741824) : de même, cela limite le cache en mémoire, garantissant que votre application n'utilise pas de mémoire excessive.
## Étape 4 : Gérer la stratégie de réallocation du cache
La gestion de la façon dont le cache est réaffecté est essentielle pour maintenir les performances. Voici comment vous pouvez le configurer.
```java
Cache.setExactReallocateOnly(false);
```

- Cache.setExactReallocateOnly(false) : lorsqu'il est défini sur false, cela permet à Aspose de gérer la réallocation du cache de manière plus flexible, ce qui peut conduire à de meilleures performances.
## Étape 5 : Vérifiez la taille du cache allouée
Cette étape consiste à surveiller le nombre d'octets actuellement alloués au cache en mémoire ou sur le disque. Implémentons cela :
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- long l1 : stocke le nombre d’octets alloués sur le disque.
- long l2 : stocke le nombre d’octets alloués en mémoire. 
Vous pouvez vérifier ces valeurs à tout moment pour vous assurer que votre application gère l'utilisation de la mémoire et du disque comme prévu.
## Étape 6 : Création d'une image PSD
Maintenant que nos configurations de cache sont configurées, créons une simple image PSD.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- Options PsdOptions : Cet objet vous permet de spécifier des options lors de la création d'une image Photoshop.
- Couleur[] color : Un tableau contenant les couleurs qui seront utilisées dans la palette d'images.
## Étape 7 : Enregistrement des données de pixels sur l'image
Maintenant, remplissons notre image avec des données de pixels et sauvegardons-la.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- Couleur[] pixels : il s'agit d'un tableau d'objets de couleur. Ici, nous le remplissons de pixels blancs.
- image.savePixels(image.getBounds(), pixels) : Cette méthode enregistre les données de pixels dans l'image. Il met à jour l'image avec les couleurs que nous avons définies.
## Étape 8 : Surveillance du cache alloué après la création de l'image
Après avoir créé l’image, il est conseillé de vérifier à nouveau combien d’octets sont alloués au cache.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- long diskBytes : capture l'allocation actuelle sur le disque après la création de l'image.
- long memoryBytes : capture l’allocation actuelle en mémoire. 
Cette étape vous aidera à déterminer la quantité de cache consommée après vos opérations.
## Étape 9 : Vérifier l'élimination appropriée
Enfin, il est crucial de s'assurer que tous les objets Aspose.PSD ont été correctement éliminés pour éviter les fuites de mémoire.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- l1 et l2 : Ces variables vous aideront à vérifier l'allocation finale. S'ils ne sont pas nuls, cela indique que certains objets n'ont pas été éliminés correctement.
## Conclusion
Le contrôle de la réallocation du cache dans Aspose.PSD pour Java peut faire une différence significative dans les performances de votre application. En suivant les étapes décrites ci-dessus, vous pouvez gérer efficacement le cache, minimiser l'utilisation de la mémoire et créer efficacement de superbes fichiers PSD. Adoptez ces techniques et regardez vos applications prospérer avec des performances optimales !
## FAQ
### Qu’est-ce qu’Aspose.PSD ?
Aspose.PSD est une bibliothèque permettant aux développeurs .NET et Java de créer, manipuler et convertir des fichiers Photoshop (PSD) par programme.
### Comment vérifier la taille du cache allouée ?
 Utilisez des méthodes comme`Cache.getAllocatedDiskBytesCount()` et`Cache.getAllocatedMemoryBytesCount()` pour surveiller l'utilisation actuelle du cache.
### Puis-je définir un répertoire personnalisé pour le cache ?
 Oui, vous pouvez spécifier un répertoire différent en utilisant`Cache.setCacheFolder("Your Directory Path")`.
### L’utilisation d’Aspose.PSD est-elle gratuite ?
Aspose.PSD est une bibliothèque payante, mais vous pouvez commencer avec un essai gratuit disponible sur leur[site web](https://releases.aspose.com/).
### Que se passe-t-il si je ne me débarrasse pas d'objets ?
Ne pas supprimer des objets peut entraîner des fuites de mémoire, obligeant votre application à utiliser plus de ressources que nécessaire.