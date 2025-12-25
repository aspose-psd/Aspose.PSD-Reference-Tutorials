---
date: 2025-12-25
description: Apprenez à convertir PSD en PNG en utilisant Aspose.PSD pour Java avec
  prise en charge du moniteur d’interruption, y compris un exemple d’interruption
  de thread Java et des conseils pour enregistrer un PSD au format PNG.
linktitle: Support for Interrupt Monitor
second_title: Aspose.PSD Java API
title: Comment convertir un PSD en PNG avec la prise en charge du moniteur d’interruption
  dans Aspose.PSD pour Java
url: /fr/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir PSD en PNG avec le Moniteur d’interruption dans Aspose.PSD pour Java

## Introduction

Si vous devez **convertir PSD en PNG** tout en conservant un contrôle total sur les conversions d’images de longue durée, le Moniteur d’interruption d’Aspose.PSD pour Java est l’outil que vous recherchiez. Dans ce tutoriel, nous parcourrons un **exemple d’interruption de thread Java** réel qui vous permet d’arrêter une conversion en cours, vous offrant ainsi la flexibilité de gérer les ressources, d’appliquer des délais d’attente ou de répondre aux annulations d’utilisateurs.

## Quick Answers
- **Que fait le Moniteur d’interruption ?** Il vous permet de signaler à une conversion d’image en cours de s’arrêter en toute sécurité.  
- **Puis‑je convertir PSD en PNG avec ?** Oui – le moniteur fonctionne avec toute opération d’enregistrement, y compris PNG.  
- **Un thread séparé est‑il requis ?** En général, vous exécutez la conversion dans un thread séparé afin de pouvoir l’interrompre.  
- **Quelle version d’Aspose.PSD est nécessaire ?** Toute version récente incluant `com.aspose.psd.multithreading.InterruptMonitor`.  
- **Ai‑je besoin d’une licence pour la production ?** Oui, une licence Aspose.PSD valide est requise pour une utilisation hors période d’essai.

## Qu’est‑ce que « convertir PSD en PNG » avec un Moniteur d’interruption ?

Convertir un grand document Photoshop (PSD/PSB) en image PNG peut être très gourmand en CPU. En attachant un **Moniteur d’interruption** au processus de conversion, vous obtenez la capacité d’arrêter le traitement de manière programmatique – idéal pour les services web, les travaux batch ou les applications UI où les utilisateurs peuvent annuler les opérations.

## Pourquoi utiliser le Moniteur d’interruption ?

- **Interface réactive :** Empêche votre application de se bloquer pendant le traitement d’un gros fichier.  
- **Gestion des ressources :** Arrête les conversions qui dépassent les limites de temps ou de mémoire.  
- **Gestion des erreurs :** Nettoie proprement les fichiers de sortie partiels lorsqu’une interruption survient.

## Prérequis

- Environnement de développement Java (JDK 8 ou supérieur).  
- Bibliothèque Aspose.PSD pour Java – téléchargez‑la **[ici](https://releases.aspose.com/psd/java/)**.  
- Un dossier contenant les fichiers PSD/PSB que vous souhaitez traiter.

## Import Packages

Commencez par importer les classes requises. Cela vous donne accès aux options d’image, au moniteur d’interruption et aux utilitaires de threading.

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

## Step‑by‑Step Guide

### Step 1: Set Your Document Directory

```java
String dataDir = "Your Document Directory";
```

Remplacez `"Your Document Directory"` par le chemin absolu où résident vos fichiers PSD.

### Step 2: Define Image Options and Output Path

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

Ici nous **enregistrons le PSD en PNG** en utilisant `PngOptions`. Ajustez les noms de fichiers selon vos besoins.

### Step 3: Initialize Interrupt Monitor and SaveImageWorker

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

L’instance `InterruptMonitor` sera utilisée plus tard pour arrêter la conversion. `SaveImageWorker` lie le moniteur à la tâche de conversion.

### Step 4: Start Image Conversion in a Separate Thread

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

Nous lançons la conversion sur un thread d’arrière‑plan afin que le thread principal reste réactif. L’appel `Thread.sleep(3000)` simule un scénario de dépassement de délai.

### Step 5: Interrupt the Process (Java Thread Interrupt Example)

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

Appeler `monitor.interrupt()` déclenche la logique **how to interrupt monitor**. Après l’interruption, nous nettoyons tout fichier PNG partiellement écrit.

## Common Issues and Solutions

| Problème | Raison | Solution |
|----------|--------|----------|
| La conversion ne s’arrête jamais | Le moniteur n’est pas lié au worker | Assurez‑vous que `SaveImageWorker` reçoit la même instance `InterruptMonitor`. |
| Le fichier de sortie reste après l’interruption | Le code de nettoyage n’est pas exécuté | Vérifiez que le bloc `finally` s’exécute et que le chemin du fichier est correct. |
| `OutOfMemoryError` sur de gros fichiers PSB | Options de streaming non utilisées | Utilisez `PsdImage` avec `LoadOptions` qui permettent un chargement mémoire‑efficace. |

## Frequently Asked Questions

### Q1 : Qu’est‑ce qu’un Moniteur d’interruption dans Aspose.PSD pour Java ?

R1 : Le Moniteur d’interruption permet aux développeurs **de gérer et d’interrompre les processus de conversion d’image**, offrant un contrôle fin sur les tâches de longue durée.

### Q2 : Comment obtenir la bibliothèque Aspose.PSD pour Java ?

R2 : Vous pouvez télécharger la bibliothèque Aspose.PSD pour Java **[ici](https://releases.aspose.com/psd/java/)**.

### Q3 : Existe‑t‑il un essai gratuit d’Aspose.PSD pour Java ?

R3 : Oui, vous pouvez explorer un essai gratuit d’Aspose.PSD **[ici](https://releases.aspose.com/)**.

### Q4 : Où puis‑je trouver du support pour Aspose.PSD pour Java ?

R4 : Consultez le forum de support Aspose.PSD pour Java **[ici](https://forum.aspose.com/c/psd/34)**.

### Q5 : Comment acheter une licence pour Aspose.PSD pour Java ?

R5 : Vous pouvez acheter une licence pour Aspose.PSD pour Java **[ici](https://purchase.aspose.com/buy)**.

---

**Dernière mise à jour :** 2025-12-25  
**Testé avec :** Aspose.PSD 24.11 pour Java  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}