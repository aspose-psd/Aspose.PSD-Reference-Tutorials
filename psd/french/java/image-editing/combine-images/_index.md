---
date: 2025-12-30
description: Apprenez à créer un fichier PSD en Java en combinant deux images avec
  Aspose.PSD. Suivez notre guide étape par étape pour fusionner rapidement les images
  dans un fichier PSD.
linktitle: Combine Images
second_title: Aspose.PSD Java API
title: Comment créer un fichier PSD en Java – Combiner des images avec Aspose.PSD
url: /fr/java/image-editing/combine-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Créer un fichier PSD Java – Combiner des images avec Aspose.PSD

## Introduction

Si vous devez **créer un fichier PSD en Java** en fusionnant plusieurs images, Aspose.PSD rend la tâche simple. Dans ce tutoriel, nous allons parcourir la combinaison de deux images en un seul canevas PSD, expliquer pourquoi cette approche est utile, et vous fournir du code prêt à l’emploi. À la fin, vous serez capable de **combiner deux images en Java** et de générer un fichier à calques d’aspect professionnel.

## Réponses rapides
- **Quelle bibliothèque est la meilleure pour fusionner des images en PSD ?** Aspose.PSD pour Java.  
- **Combien de temps prend l’implémentation ?** Environ 10‑15 minutes pour une combinaison de base.  
- **Ai‑je besoin d’une licence ?** Un essai gratuit suffit pour les tests ; une licence commerciale est requise pour la production.  
- **Puis‑je ajouter plus de deux images ?** Oui – répétez les appels `drawImage` pour chaque calque supplémentaire.  
- **Quelle version de Java est prise en charge ?** Java 8 et versions ultérieures.

## Prérequis

Avant de commencer, assurez‑vous de disposer de :

1. **Bibliothèque Aspose.PSD** – téléchargez‑la depuis [here](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit (JDK)** – Java 8+ est recommandé.  
3. **Répertoire de documents** – un dossier sur votre machine où les images sources et le PSD résultant seront stockés.

## Importer les packages

Commencez par importer les classes Aspose.PSD requises dans votre projet :

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

## Guide étape par étape

### Étape 1 : Créer les options PSD (préparer le fichier)

Nous créons d’abord une instance `PsdOptions` qui contiendra les paramètres de sortie.

```java
PsdOptions imageOptions = new PsdOptions();
```

### Étape 2 : Définir le FileCreateSource (spécifier où le PSD sera enregistré)

Attribuez un `FileCreateSource` aux options, en pointant vers le fichier de résultat souhaité.

```java
imageOptions.setSource(new FileCreateSource(dataDir + "Two_images_result_out.psd", false));
```

### Étape 3 : Créer l’instance Image (initialiser la taille du canevas)

Créez un objet `Image` avec les options et spécifiez un canevas de 600 × 600 pixels.

```java
Image image = Image.create(imageOptions, 600, 600);
```

### Étape 4 : Initialiser Graphics et dessiner la première image

Un objet `Graphics` nous permet de peindre sur le canevas. Nous effaçons l’arrière‑plan en blanc et dessinons la première image source sur la moitié gauche.

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(Image.load(dataDir + "example1.psd"), 0, 0, 300, 600);
```

### Étape 5 : Dessiner la deuxième image (compléter la combinaison)

Nous plaçons maintenant la deuxième image sur la moitié droite du même canevas.

```java
graphics.drawImage(Image.load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

### Étape 6 : Enregistrer le fichier PSD résultant

Enfin, persistez le canevas combiné sur le disque.

```java
image.save();
```

Félicitations ! Vous avez réussi à **fusionner des images en PSD** et à créer un fichier PSD en Java.

## Pourquoi combiner des images avec Aspose.PSD ?

- **Gestion des calques** – chaque appel `drawImage` ajoute un calque séparé que vous pouvez modifier ultérieurement.  
- **Flexibilité des formats** – prend en charge PSD, PNG, JPEG, BMP, et bien d’autres.  
- **Aucune dépendance native** – Java pur, fonctionne sur tout OS exécutant le JDK.  

## Problèmes courants et solutions

| Problème | Cause | Solution |
|----------|-------|----------|
| Erreur `File not found` lors du chargement des images sources | Chemin `dataDir` incorrect | Vérifiez que `dataDir` pointe vers le dossier contenant `example1.psd` et `example2.psd`. |
| Le PSD de sortie est vide | `graphics.clear` appelé après le dessin | Assurez‑vous que `graphics.clear(Color.getWhite())` est exécuté **avant** tout appel `drawImage`. |
| Exception de licence à l’exécution | Licence Aspose.PSD manquante ou expirée | Appliquez une licence valide avec `License license = new License(); license.setLicense("Aspose.PSD.lic");` avant tout appel d’API. |

## Foire aux questions

### Q1 : Aspose.PSD est‑il compatible avec tous les formats d’image ?
R1 : Aspose.PSD se concentre principalement sur le format PSD. Cependant, il prend en charge divers autres formats en entrée et en sortie.

### Q2 : Puis‑je effectuer des modifications supplémentaires sur l’image combinée ?
R2 : Absolument ! Après avoir combiné les images, vous pouvez manipuler davantage le PSD résultant à l’aide des nombreuses fonctionnalités d’Aspose.PSD.

### Q3 : Existe‑t‑il des exigences de licence pour utiliser Aspose.PSD ?
R3 : Oui, une licence valide est requise pour une utilisation commerciale. Obtenez‑la depuis [here](https://purchase.aspose.com/buy).

### Q4 : Un essai gratuit est‑il disponible pour Aspose.PSD ?
R4 : Oui, vous pouvez explorer Aspose.PSD avec un essai gratuit [here](https://releases.aspose.com/).

### Q5 : Où puis‑je trouver du support pour les questions liées à Aspose.PSD ?
R5 : Consultez le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour le support communautaire et les discussions.

---

**Dernière mise à jour :** 2025-12-30  
**Testé avec :** Aspose.PSD 24.11 pour Java  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}