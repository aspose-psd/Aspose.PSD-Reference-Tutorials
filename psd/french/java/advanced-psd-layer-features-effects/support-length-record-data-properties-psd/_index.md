---
date: 2026-02-20
description: Apprenez comment prendre en charge les propriétés d’enregistrement de
  longueur et traiter par lots les fichiers PSD à l’aide d’Aspose.PSD pour Java. Guide
  étape par étape avec des exemples de code.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: Propriétés d'enregistrement de la longueur du support – Modifier les formes
  vectorielles PSD (Java)
url: /fr/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Prise en charge des propriétés d’enregistrement de longueur – Modifier les formes vectorielles PSD (Java)

## Introduction
Si vous devez **modifier les formes vectorielles PSD** de façon programmatique, la bibliothèque Aspose.PSD for Java vous donne un contrôle complet sur les fichiers Photoshop directement depuis votre code Java. Dans ce tutoriel, nous passerons en revue tout ce que vous devez savoir pour **prendre en charge les propriétés d’enregistrement de longueur** — une étape essentielle lorsque vous souhaitez modifier les calques de formes vectorielles. À la fin, vous pourrez ouvrir un PSD, ajuster ses propriétés de forme vectorielle et enregistrer le fichier mis à jour sans jamais quitter votre IDE. Plongeons‑y !

## Quick Answers
- **Que signifie « modifier les formes vectorielles PSD » ?** Ajuster la géométrie, les opérations de chemin ou d’autres propriétés des calques basés sur le vecteur à l’intérieur d’un fichier PSD.  
- **Quelle bibliothèque gère cela ?** Aspose.PSD for Java.  
- **Ai‑je besoin d’une licence ?** Un essai gratuit suffit pour l’évaluation ; une licence commerciale est requise pour la production.  
- **Combien de temps prend l’implémentation ?** Environ 10‑15 minutes pour un script de modification de forme basique.  
- **Quelles sont les principales prérequis ?** Java JDK, Aspose.PSD for Java et un fichier PSD d’exemple.

## Qu’est‑ce que la « prise en charge des propriétés d’enregistrement de longueur » ?
Prendre en charge les propriétés d’enregistrement de longueur signifie accéder aux objets `LengthRecord` qui décrivent chaque chemin vectoriel à l’intérieur d’un PSD et les mettre à jour. Modifier ces enregistrements vous permet de contrôler la façon dont les formes se combinent, s’intersectent ou se soustraient les unes des autres.

## Pourquoi utiliser Aspose.PSD for Java pour prendre en charge les propriétés d’enregistrement de longueur ?
- **Pas besoin de Photoshop** – travaillez directement avec les fichiers PSD sur n’importe quel serveur.  
- **API riche** – accédez aux calques, ressources et données vectorielles avec des classes fortement typées.  
- **Multiplateforme** – fonctionne sous Windows, Linux ou macOS avec n’importe quel JDK.  
- **Optimisée pour la performance** – gestion efficace de la mémoire et opérations d’enregistrement rapides.  

## Prérequis
1. **Java Development Kit (JDK)** – téléchargez‑le depuis le [site d’Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) ou utilisez votre gestionnaire de paquets préféré.  
2. **Aspose.PSD for Java** – obtenez le dernier JAR depuis la [page des releases Aspose](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse ou tout éditeur compatible Java.  
4. **Un fichier PSD** – créez‑en un dans Photoshop ou récupérez un PSD d’exemple pour expérimenter.  
5. **Connaissances de base en Java** – familiarité avec les classes, objets et la gestion des exceptions.

## Import Packages
Tout d’abord, importez les classes dont vous aurez besoin pour travailler avec les fichiers PSD et les ressources de formes vectorielles.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Étape 1 : Configurer vos répertoires source et de sortie
Définissez où se trouve le PSD original et où vous souhaitez enregistrer le fichier modifié.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Étape 2 : Charger le fichier PSD
Utilisez `Image.load` pour ouvrir le fichier et le caster en `PsdImage` afin d’accéder aux fonctionnalités spécifiques aux PSD.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Étape 3 : Localiser la ressource Vsms dans le calque
Les données de forme vectorielle résident dans une `VsmsResource`. Parcourez les ressources du deuxième calque pour la trouver.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Étape 4 : Accéder aux enregistrements de longueur
Chaque `LengthRecord` représente un chemin vectoriel distinct. Récupérez ceux que vous avez l’intention de modifier.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Étape 5 : Modifier les propriétés d’opération de chemin
Vous pouvez maintenant **modifier les formes vectorielles PSD** en changeant leurs `PathOperations`. Cela détermine comment les formes interagissent (ex. exclusion, intersection, soustraction).

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Étape 6 : Enregistrer le fichier PSD modifié
Persistez vos modifications dans un nouveau fichier.

```java
psdImage.save(outPsdFilePath);
```

## Étape 7 : Nettoyer les ressources
Libérez la mémoire en disposant du `PsdImage`.

```java
psdImage.dispose();
```

## Comment traiter par lots des fichiers PSD avec la prise en charge des propriétés d’enregistrement de longueur
Si vous devez appliquer les mêmes ajustements de formes vectorielles à de nombreux PSD, encapsulez le code ci‑dessus dans une boucle qui parcourt un répertoire de fichiers. Mettez à jour `inPsdFilePath` et `outPsdFilePath` à chaque itération, et vous pourrez **traiter par lots des fichiers PSD** efficacement.

## Pièges courants & Astuces
- **Vérifications de null** – assurez‑vous toujours que `resource` n’est pas `null` avant d’accéder aux chemins.  
- **Limites d’index de chemin** – vérifiez que les indices que vous utilisez (`[2]`, `[7]`, `[11]`) existent pour le PSD spécifique que vous éditez.  
- **Licence** – exécuter sans licence valide ajoutera un filigrane au PSD enregistré.  

## Conclusion
Vous disposez maintenant d’un exemple complet, de bout en bout, montrant comment **modifier les formes vectorielles PSD** en prenant en charge les propriétés d’enregistrement de longueur avec Aspose.PSD for Java. Que vous automatisiez des pipelines d’actifs ou construisiez un outil de conception personnalisé, ces API vous offrent la flexibilité de manipuler les calques vectoriels sans intervention manuelle dans Photoshop. Explorez davantage en expérimentant d’autres `PathOperations` ou en combinant plusieurs modifications de `LengthRecord` pour des formes complexes.

## Foire aux questions

**Q : Comment gérer un PSD qui ne contient aucune couche de forme vectorielle ?**  
R : La `VsmsResource` sera absente, donc `resource` restera `null`. Ajoutez une vérification et sautez l’étape de modification ou informez l’utilisateur.

**Q : Puis‑je changer d’autres propriétés comme la couleur de remplissage ou l’épaisseur du trait ?**  
R : Oui, `LengthRecord` propose des setters supplémentaires pour le remplissage, le trait et l’opacité. Consultez la documentation de l’API pour tous les détails.

**Q : Est‑il possible de traiter plusieurs fichiers PSD en lot ?**  
R : Absolument. Encapsulez le code dans une boucle qui parcourt un répertoire de fichiers PSD, en ajustant les chemins d’entrée et de sortie à chaque itération.

**Q : Dois‑je fermer les flux manuellement lors du chargement depuis un chemin de fichier ?**  
R : La méthode `Image.load` gère les flux de fichiers en interne, mais si vous chargez depuis un `InputStream`, pensez à le fermer après utilisation.

**Q : Quelle version d’Aspose.PSD est requise pour ces API ?**  
R : Les classes `LengthRecord` et `PathOperations` sont disponibles depuis Aspose.PSD 20.10. Il est recommandé d’utiliser la version la plus récente.

---

**Dernière mise à jour :** 2026-02-20  
**Testé avec :** Aspose.PSD for Java 24.11  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}