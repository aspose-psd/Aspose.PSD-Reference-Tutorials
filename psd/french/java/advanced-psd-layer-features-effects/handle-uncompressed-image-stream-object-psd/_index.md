---
date: 2026-08-01
description: Apprenez à exporter PSD en PNG et à gérer les flux d'images non compressés
  avec Aspose.PSD for Java.
keywords:
- export psd to png
- save psd as png
- java image manipulation
lastmod: 2026-08-01
linktitle: Gérer l'objet de flux d'image non compressé dans PSD - Java
og_description: exporter psd en png avec Aspose.PSD for Java. Apprenez à gérer les
  flux d'images non compressés, créer des objets graphiques et enregistrer des PNG
  de haute qualité.
og_image_alt: 'Developer guide: Export PSD to PNG with uncompressed stream using Aspose.PSD
  Java'
og_title: exporter psd en png – guide Java pour les flux PSD non compressés
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to export PSD to PNG and handle uncompressed image streams
    with Aspose.PSD for Java.
  headline: Export PSD to PNG – Create PSD Graphics Object – Uncompressed Stream in
    Java
  type: TechArticle
- questions:
  - answer: Yes. After loading the PSD, retrieve the desired layer via `psdImage.getLayers().get_Item(index)`
      and pass that layer to the `Graphics` constructor.
    question: Can I use the graphics object to edit only one specific layer?
  - answer: Raw stores pixel data without any compression, so the resulting file is
      larger than a compressed PSD, but it guarantees 100 % pixel fidelity.
    question: Does the Raw compression method affect file size?
  - answer: Absolutely. After editing, call `psdImage.save("output.png", new PngOptions())`—this
      is the standard way to **export PSD to PNG** with lossless quality.
    question: Is it possible to export the edited PSD to another format (e.g., PNG)?
  - answer: Aspose.PSD for Java supports JDK 8 and later, including all LTS releases
      up to JDK 21.
    question: What Java version is required?
  - answer: Invoke `psdImage.dispose()` and close any streams (e.g., `ms.close()`)
      to free native memory and avoid leaks.
    question: How do I release resources after processing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd
- Aspose.PSD
- Java image processing
- uncompressed stream
- PSD graphics
title: Exporter PSD en PNG – Créer un objet graphique PSD – Flux non compressé en
  Java
url: /fr/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter PSD en PNG – Créer un objet graphique PSD – Flux non compressé en Java

## Introduction
Dans ce guide étape par étape, vous allez **exporter PSD en PNG** tout en travaillant avec un flux d'image non compressé à l'aide d'Aspose.PSD pour Java. Que vous automatisiez un pipeline de conception ou créiez un éditeur personnalisé, la capacité de rendre un fichier Photoshop sans perte de qualité est essentielle. Nous commencerons par la configuration requise, parcourrons la création d'un objet `Graphics`, et terminerons par une exportation PNG sans perte. À la fin, vous comprendrez pourquoi Aspose.PSD gère efficacement les flux bruts et comment l'intégrer dans n'importe quel projet Java.

## Réponses rapides
- **Que signifie « create PSD graphics object » ?** Cela signifie instancier un contexte `Graphics` qui vous permet de dessiner ou de modifier une image PSD programmatiquement.  
- **Quelle bibliothèque gère les flux non compressés ?** Aspose.PSD pour Java offre une prise en charge complète des données d'image brutes (non compressées).  
- **Puis-je exporter PSD en PNG après modification ?** Oui — une fois que vous avez un objet `Graphics`, vous pouvez rendre le PSD et l'enregistrer en PNG en un seul appel.  
- **Ai-je besoin d'une licence pour le développement ?** Un essai gratuit fonctionne pour les tests ; une licence commerciale est requise pour les déploiements en production.  
- **L'exportation est‑elle sans perte ?** L'exportation en PNG préserve les données de pixels originales, offrant une qualité sans perte avec une taille de fichier inférieure à celle du PSD brut.

## Qu'est-ce que l'exportation de PSD en PNG ?
L'exportation de PSD en PNG convertit un document Photoshop à calques en une image raster à couche unique et sans perte qui peut être affichée par n'importe quel navigateur web ou visualiseur d'images. Le processus conserve la transparence, la profondeur de couleur et les effets de calque tout en supprimant les métadonnées spécifiques à Photoshop. Il préserve également le profil couleur original pour une reproduction précise des couleurs.

## Pourquoi utiliser Aspose.PSD pour Java pour la manipulation d'images ?
Aspose.PSD prend en charge **plus de 50** formats d'entrée et de sortie — notamment PSD, PNG, JPEG, BMP et TIFF — et peut traiter des fichiers contenant **plus de 200 couches** sans charger le document complet en mémoire. Son option de compression `Raw` stocke les données de pixels non compressées, garantissant une fidélité pixel‑par‑pixel pour les éditions ultérieures ou l'archivage.

## Prérequis
Avant de plonger dans le code, vérifiez que vous disposez de ce qui suit :
- **Java Development Kit (JDK)** – JDK 8 ou version ultérieure installé.  
- **Aspose.PSD for Java** – Téléchargez le JAR le plus récent depuis la page officielle de publication : [Téléchargement Aspose.PSD Java](https://releases.aspose.com/psd/java/). Vous pouvez également y accéder via [ce lien](https://releases.aspose.com/psd/java/) ou la [page de publication](https://releases.aspose.com/psd/java/). Pour d'autres produits Aspose, cliquez [ici](https://releases.aspose.com/).  
- **IDE** – IntelliJ IDEA, Eclipse ou tout éditeur compatible Java.  
- **Connaissances de base en Java** – Familiarité avec les classes, les méthodes et la gestion des exceptions.

Avec tout cela en place, vous êtes prêt à commencer à coder.

## Importer les packages
La classe `Graphics` est la surface de dessin d'Aspose.PSD qui vous permet de rendre ou de modifier les données de pixels directement. La classe `PsdImage` représente un fichier PSD en mémoire, tandis que `PsdOptions` contrôle la façon dont l'image est enregistrée.

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

Maintenant, décomposons le code en étapes digestes afin que vous puissiez suivre facilement. Nous configurerons l'environnement, chargerons un fichier PSD, le manipulerons, puis enregistrerons le résultat.

## Étape 1 : Définir le répertoire de vos documents
Avant toute opération de fichier, vous devez indiquer au programme où chercher vos ressources PSD. Ce chemin de répertoire est utilisé tout au long du tutoriel.

```java
String dataDir = "Your Document Directory";
```

Remplacez `"Your Document Directory"` par le chemin absolu contenant `layers.psd`. Garder le chemin configurable rend le code réutilisable dans différents projets.

## Étape 2 : Créer un flux de sortie ByteArray
Un `ByteArrayOutputStream` est un flux Java qui conserve les données en mémoire sous forme de tableau d'octets. Il agit comme un tampon en mémoire pour l'image modifiée, vous permettant de capturer les octets bruts avant de les écrire sur le disque ou de les envoyer sur un réseau.

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

La variable `ms` contiendra les données d'image non compressées après l'opération `save`.

## Étape 3 : Charger le fichier PSD
La classe `PsdImage` charge un fichier PSD en mémoire pour la manipulation. Charger le fichier convertit le PSD présent sur le disque en un objet `PsdImage` que vous pouvez manipuler. Cette étape est celle où Aspose.PSD lit l'en-tête du fichier, les calques et les ressources.

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Si le chemin est incorrect, Aspose.PSD lève une `FileNotFoundException`, que vous devriez intercepter dans le code de production.

## Étape 4 : Configurer les PsdOptions pour l'enregistrement
`PsdOptions` spécifie les paramètres d'enregistrement pour les fichiers PSD. Définir la méthode de compression sur `Raw` indique que les données de pixels doivent être stockées sans compression, préservant chaque pixel exactement tel qu'il apparaît en mémoire.

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

L'option `CompressionMethod.Raw` stocke les données de pixels sans aucune compression, ce qui est idéal lorsque vous prévoyez d'effectuer d'autres modifications ultérieurement.

## Étape 5 : Enregistrer l'image dans le flux de sortie
Vous persistez maintenant le PSD (avec toutes les modifications) dans le `ByteArrayOutputStream` créé précédemment. La méthode `save` respecte les `PsdOptions` que vous avez configurées.

```java
psdImage.save(ms, saveOptions);
```

À ce stade, `ms` contient la représentation binaire complète du PSD non compressé.

## Étape 6 : Réinitialiser le flux de sortie
Après l'écriture, le pointeur interne du flux se trouve à la fin. Le réinitialiser revient au début du flux afin que vous puissiez lire depuis le commencement.

```java
ms.reset();
```

Considérez cela comme le déplacement de la tête de bande vers le début avant la lecture.

## Étape 7 : Charger l'image nouvellement créée
Vous pouvez maintenant créer une nouvelle instance `PsdImage` directement à partir du tableau d'octets. Cette étape vérifie que les données enregistrées peuvent être rechargées sans corruption.

```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

Si l'image se charge avec succès, vous savez que le flux non compressé a été écrit correctement.

## Étape 8 : Créer un objet Graphics
La classe `Graphics` est le canevas de dessin d'Aspose.PSD. Elle fournit des méthodes pour dessiner des formes, du texte et appliquer des filtres directement sur la matrice de pixels d'un `PsdImage`.

```java
Graphics graphics = new Graphics(psdImage);
```

Avec cette instance `Graphics`, vous pouvez peindre du nouveau contenu, effacer des parties ou composer des calques supplémentaires.

## Comment exporter PSD en PNG avec Aspose.PSD pour Java ?
Chargez le PSD avec `new PsdImage(dataDir + "layers.psd")`, créez un objet `Graphics`, effectuez les dessins nécessaires, puis appelez `psdImage.save("output.png", new PngOptions())`. Cette séquence rend le PSD modifié et écrit un PNG sans perte en une seule étape, en exploitant le moteur de conversion intégré d'Aspose.PSD.

## Manipuler les calques PSD avec l'objet Graphics
Disposer d'une instance `Graphics` vous donne un contrôle au niveau du pixel sur chaque calque. Vous pouvez dessiner des formes géométriques, rendre du texte ou appliquer des filtres personnalisés. Comme le contexte graphique travaille sur la vue rasterisée du calque, les modifications sont immédiatement visibles lors de l'enregistrement de l'image.

## Problèmes courants et solutions
- **NullPointerException lors du chargement du fichier** – vérifiez à nouveau le chemin `dataDir` et assurez‑vous que le nom du fichier correspond exactement, y compris la sensibilité à la casse.  
- **Sortie compressée malgré l'utilisation de Raw** – vérifiez que `saveOptions.setCompressionMethod(CompressionMethod.Raw);` est appelé **avant** d'invoquer `save`.  
- **L'objet Graphics apparaît vide** – assurez‑vous de dessiner sur la bonne instance `PsdImage` (celle que vous avez chargée, pas une nouvelle image vide).  
- **OutOfMemoryError sur de gros fichiers** – utilisez `PsdImage.load(dataDir, LoadOptions)` avec `loadOptions.setLoadMode(LoadMode.Memory)` pour diffuser de gros fichiers sans charger le document complet en RAM.

## FAQ

### Qu'est-ce qu'Aspose.PSD ?
Aspose.PSD est une bibliothèque Java qui permet aux développeurs de créer, modifier et convertir des fichiers Photoshop PSD de manière programmatique sans nécessiter Adobe Photoshop. Elle prend en charge la lecture et l'écriture de fichiers PSD, la gestion des calques, masques, canaux et diverses ressources d'image, et fournit des API pour les opérations raster et vectorielles, ce qui la rend adaptée au traitement d'images côté serveur et aux tâches d'automatisation.

### Comment télécharger Aspose.PSD pour Java ?
Vous pouvez le télécharger depuis la page officielle de publication : [Téléchargement Aspose.PSD Java](https://releases.aspose.com/psd/java/).

### Existe‑t‑il un essai gratuit pour Aspose.PSD ?
Oui, un essai pleinement fonctionnel est disponible sur la même page de téléchargement. Il fonctionne pour le développement et l'évaluation.

### Puis‑je obtenir du support pour Aspose.PSD ?
Absolument ! Le forum de support Aspose fournit des réponses de l'équipe produit et de la communauté : [Forum de support Aspose](https://forum.aspose.com/c/psd/34).

### Comment obtenir une licence temporaire pour Aspose.PSD ?
Vous pouvez demander une licence temporaire directement depuis le portail de licences d'Aspose, qui fournit une clé limitée dans le temps valable 30 jours. Cela vous permet d'évaluer la pleine fonctionnalité d'Aspose.PSD sans acheter de licence commerciale. Après la période d'essai, vous devez remplacer la clé temporaire par une licence permanente pour continuer à utiliser la bibliothèque en production. Visitez la [page de licence temporaire](https://purchase.aspose.com/temporary-license/) pour générer une clé limitée dans le temps.

## Questions fréquemment posées
**Q : Puis‑je utiliser l'objet graphics pour modifier uniquement un calque spécifique ?**  
R : Oui. Après avoir chargé le PSD, récupérez le calque souhaité via `psdImage.getLayers().get_Item(index)` et passez ce calque au constructeur `Graphics`.

**Q : La méthode de compression Raw affecte‑t‑elle la taille du fichier ?**  
R : Raw stocke les données de pixels sans aucune compression, ainsi le fichier résultant est plus volumineux qu'un PSD compressé, mais il garantit une fidélité pixel à 100 %.

**Q : Est‑il possible d'exporter le PSD modifié vers un autre format (par ex., PNG) ?**  
R : Absolument. Après modification, appelez `psdImage.save("output.png", new PngOptions())` — c'est la méthode standard pour **exporter PSD en PNG** avec une qualité sans perte.

**Q : Quelle version de Java est requise ?**  
R : Aspose.PSD pour Java prend en charge JDK 8 et versions ultérieures, y compris toutes les versions LTS jusqu'à JDK 21.

**Q : Comment libérer les ressources après le traitement ?**  
R : Appelez `psdImage.dispose()` et fermez tous les flux (par ex., `ms.close()`) pour libérer la mémoire native et éviter les fuites.

---

**Dernière mise à jour :** 2026-08-01  
**Testé avec :** Aspose.PSD for Java (latest release)  
**Auteur :** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriels associés

- [Enregistrer les images dans un flux avec Aspose.PSD pour Java](/psd/java/advanced-techniques/save-images-to-stream/)
- [Exporter le groupe de calques PSD en image avec Java](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)
- [Créer une image à l'aide d'un flux dans Aspose.PSD pour Java](/psd/java/image-editing/create-image-using-stream/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}