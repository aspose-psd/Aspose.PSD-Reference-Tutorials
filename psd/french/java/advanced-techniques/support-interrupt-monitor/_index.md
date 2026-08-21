---
date: 2026-06-08
description: Apprenez comment enregistrer un PSD au format PNG en utilisant Aspose.PSD
  for Java et interrompre la conversion si nécessaire. Gérez efficacement le flux
  de travail d'image.
keywords:
- save psd as png
- how to interrupt conversion
- psd to png conversion
- manage image workflow
linktitle: Support pour Interrupt Monitor
schemas:
- author: Aspose
  dateModified: '2026-06-08'
  description: Learn how to save PSD as PNG using Aspose.PSD for Java and interrupt
    conversion when needed. Manage image workflow efficiently.
  headline: How to Save PSD as PNG with Interrupt Monitor in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to save PSD as PNG using Aspose.PSD for Java and interrupt
    conversion when needed. Manage image workflow efficiently.
  name: How to Save PSD as PNG with Interrupt Monitor in Aspose.PSD for Java
  steps:
  - name: Set Your Document Directory
    text: Ensure to replace “Your Document Directory” with the actual path where your
      PSD documents are stored.
  - name: Define Image Options and Output Path
    text: Specify the image options, source PSD file, and the desired output path
      for the converted image.
  - name: Initialize Interrupt Monitor and SaveImageWorker
    text: The `InterruptMonitor` class watches a running conversion and can interrupt
      it when `requestInterrupt()` is called. Create instances of `InterruptMonitor`
      and `SaveImageWorker`, linking the monitor to the image conversion worker.
  - name: Start Image Conversion Thread
    text: Initiate a new thread for the image conversion process and introduce a timeout
      period to anticipate interruption.
  - name: Interrupt the Process
    text: Calling `monitor.requestInterrupt()` signals the monitor to abort the ongoing
      conversion. Interrupt the image conversion process using the `InterruptMonitor`
      and wait for the interruption to complete. Finally, clean up by deleting the
      output file.
  type: HowTo
- questions:
  - answer: Yes, use `InterruptMonitor` to stop the process on demand.
    question: Can I interrupt a PSD‑to‑PNG conversion?
  - answer: Call `save(outputPath, new PngOptions())`.
    question: Which method saves a PSD as PNG?
  - answer: A commercial license is required; a free trial is available.
    question: Do I need a license for production?
  - answer: Java 8 and later are fully supported.
    question: What Java version is supported?
  - answer: Conversions can run in separate threads; the monitor handles interruptions
      safely.
    question: Is the library thread‑safe?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Comment enregistrer un PSD au format PNG avec Interrupt Monitor dans Aspose.PSD
  for Java
url: /fr/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Enregistrer un PSD en PNG avec le moniteur d’interruption dans Aspose.PSD pour Java

## Introduction

Si vous devez **enregistrer un PSD en PNG** tout en conservant un contrôle total sur les conversions de longue durée, le moniteur d’interruption d’Aspose.PSD pour Java vous offre exactement cela. Dans ce tutoriel, nous allons parcourir la configuration du moniteur, la conversion d’un fichier PSD en PNG, et l’annulation sécurisée de l’opération lorsque cela est nécessaire. Vous verrez également comment cela s’intègre dans un flux de travail typique de traitement d’images et pourquoi c’est indispensable pour des applications robustes.

## Réponses rapides
- **Puis-je interrompre une conversion PSD‑vers‑PNG ?** Oui, utilisez `InterruptMonitor` pour arrêter le processus à la demande.  
- **Quelle méthode enregistre un PSD en PNG ?** Appelez `save(outputPath, new PngOptions())`.  
- **Ai‑je besoin d’une licence pour la production ?** Une licence commerciale est requise ; un essai gratuit est disponible.  
- **Quelle version de Java est prise en charge ?** Java 8 et les versions ultérieures sont entièrement prises en charge.  
- **La bibliothèque est‑elle thread‑safe ?** Les conversions peuvent s’exécuter dans des threads séparés ; le moniteur gère les interruptions en toute sécurité.

## Prérequis

Avant de plonger dans les subtilités de l’utilisation du moniteur d’interruption, assurez‑vous d’avoir les prérequis suivants en place :

- **Environnement de développement Java :** Configurez un environnement de développement Java sur votre système.  
- **Bibliothèque Aspose.PSD :** Obtenez la bibliothèque Aspose.PSD pour Java. Vous pouvez la télécharger [ici](https://releases.aspose.com/psd/java/). Vous pouvez également visiter le site principal d’Aspose [ici](https://releases.aspose.com/).  
- **Répertoire de documents :** Disposez d’un répertoire désigné pour vos documents PSD.

## Importer les packages

Commencez par importer les packages nécessaires dans votre projet Java. Cela garantit que vous avez accès aux fonctionnalités d’Aspose.PSD.

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

Maintenant, décomposons le code d’exemple en un guide étape par étape pour intégrer le moniteur d’interruption dans votre projet Aspose.PSD pour Java.

## Comment enregistrer un PSD en PNG en utilisant le moniteur d’interruption ?

`PsdImage` représente un document PSD chargé en mémoire.  
`SaveImageWorker` effectue la conversion d’image dans un thread séparé.  

Chargez votre fichier PSD avec `new PsdImage("source.psd")`, attachez un `InterruptMonitor` au `SaveImageWorker`, et appelez `save("output.png", new PngOptions())`. Le moniteur surveille les demandes d’annulation et interrompt proprement la conversion, rendant le contrôle à votre application en quelques millisecondes.

### Étape 1 : Définir votre répertoire de documents

```java
String dataDir = "Your Document Directory";
```

Assurez‑vous de remplacer « Your Document Directory » par le chemin réel où vos documents PSD sont stockés.

### Étape 2 : Définir les options d’image et le chemin de sortie

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

Spécifiez les options d’image, le fichier PSD source, et le chemin de sortie souhaité pour l’image convertie.

### Étape 3 : Initialiser le moniteur d’interruption et le SaveImageWorker

La classe `InterruptMonitor` surveille une conversion en cours et peut l’interrompre lorsque `requestInterrupt()` est appelée.  

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

Créez des instances de `InterruptMonitor` et de `SaveImageWorker`, en liant le moniteur au worker de conversion d’image.

### Étape 4 : Démarrer le thread de conversion d’image

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

Initiez un nouveau thread pour le processus de conversion d’image et introduisez une période de délai d’attente pour anticiper l’interruption.

### Étape 5 : Interrompre le processus

Appeler `monitor.requestInterrupt()` indique au moniteur d’interrompre la conversion en cours.  

```java
    // Interrupt the process
    monitor.interrupt();
    System.out.println("Interrupting the save thread #" + thread.getId() + " at " + getDateTime().toString());

    // Wait for interruption...
    thread.join();
} finally {
    // Delete the output file if it exists
    File f = new File(output);
    if (f.exists()) {
        f.delete();
    }
}
```

Interrompez le processus de conversion d’image en utilisant le `InterruptMonitor` et attendez que l’interruption se termine. Enfin, nettoyez en supprimant le fichier de sortie.

## Pourquoi utiliser le moniteur d’interruption pour la conversion PSD‑vers‑PNG ?

Aspose.PSD prend en charge **plus de 30 formats de sortie**, dont PNG, JPEG, BMP et TIFF, et peut traiter des fichiers jusqu’à **500 Mo** sans charger le document complet en mémoire. En ajoutant un moniteur d’interruption, vous réduisez le gaspillage CPU et améliorez la réactivité des pipelines de traitement par lots, surtout lorsqu’une conversion dépasse les limites de temps prévues.

## Problèmes courants et solutions

- **La conversion se bloque indéfiniment :** Assurez‑vous que le moniteur est attaché **avant** d’appeler `save`.  
- **Le fichier de sortie est corrompu après interruption :** Le moniteur interrompt proprement ; cependant, vérifiez toujours si le fichier existe avant de l’utiliser.  
- **Problèmes de thread‑safety :** Exécutez chaque conversion dans son propre thread ; le moniteur n’affecte que le worker qui lui est associé.

## Questions fréquemment posées

**Q1 : Qu’est‑ce qu’un moniteur d’interruption dans Aspose.PSD pour Java ?**  
R : Le moniteur d’interruption permet aux développeurs de mettre en pause ou d’annuler des conversions d’images de longue durée, offrant un contrôle en temps réel sur l’utilisation des ressources.

**Q2 : Comment puis‑je obtenir la bibliothèque Aspose.PSD pour Java ?**  
R : Vous pouvez télécharger la bibliothèque Aspose.PSD pour Java [ici](https://releases.aspose.com/psd/java/).

**Q3 : Existe‑t‑il un essai gratuit disponible pour Aspose.PSD pour Java ?**  
R : Oui, vous pouvez explorer un essai gratuit d’Aspose.PSD [ici](https://releases.aspose.com/).

**Q4 : Où puis‑je trouver du support pour Aspose.PSD pour Java ?**  
R : Visitez le forum de support Aspose.PSD pour Java [ici](https://forum.aspose.com/c/psd/34).

**Q5 : Comment puis‑je acheter une licence pour Aspose.PSD pour Java ?**  
R : Vous pouvez acheter une licence pour Aspose.PSD pour Java [ici](https://purchase.aspose.com/buy).

**Q6 : Puis‑je convertir plusieurs fichiers PSD en PNG en parallèle ?**  
R : Oui, créez un thread séparé pour chaque fichier et attachez un `InterruptMonitor` individuel à chaque worker de conversion.

**Q7 : La bibliothèque gère‑t‑elle les profils couleur lors de la conversion PSD‑vers‑PNG ?**  
R : Absolument ; Aspose.PSD préserve les profils ICC intégrés et les applique automatiquement au PNG de sortie.

---

**Dernière mise à jour:** 2026-06-08  
**Testé avec:** Aspose.PSD 23.12 for Java  
**Auteur:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriels associés

- [Enregistrer un PSD en PNG et appliquer une ombre portée de rendu dans Aspose.PSD pour Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Exporter un PSD en PNG & ajouter un nouveau calque régulier avec Aspose.PSD pour Java](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [Prise en charge du moniteur d’interruption dans les fichiers PSD - Java](/psd/java/psd-layer-management-effects/support-interrupt-monitor-psd-files/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}