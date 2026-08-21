---
date: 2026-06-08
description: Aspose.PSD for Java를 사용하여 PSD를 PNG로 저장하고 필요할 때 변환을 중단하는 방법을 배웁니다. 이미지
  워크플로를 효율적으로 관리하세요.
keywords:
- save psd as png
- how to interrupt conversion
- psd to png conversion
- manage image workflow
linktitle: 인터럽트 모니터 지원
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
title: Aspose.PSD for Java에서 인터럽트 모니터를 사용하여 PSD를 PNG로 저장하는 방법
url: /ko/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java에서 인터럽트 모니터를 사용하여 PSD를 PNG로 저장하기

## 소개

오래 걸리는 변환 작업을 완전히 제어하면서 **save PSD as PNG**가 필요하다면, Aspose.PSD for Java의 Interrupt Monitor가 정확히 그 기능을 제공합니다. 이 튜토리얼에서는 모니터 설정, PSD 파일을 PNG로 변환, 필요 시 작업을 안전하게 중단하는 과정을 단계별로 안내합니다. 또한 이 기능이 일반적인 이미지 처리 워크플로우에 어떻게 들어맞는지와 견고한 애플리케이션에 왜 필수적인지 확인할 수 있습니다.

## 빠른 답변
- **Can I interrupt a PSD‑to‑PNG conversion?** 예, `InterruptMonitor`를 사용하여 필요 시 프로세스를 중지할 수 있습니다.  
- **Which method saves a PSD as PNG?** `save(outputPath, new PngOptions())`를 호출합니다.  
- **Do I need a license for production?** 상업용 라이선스가 필요하며, 무료 체험판을 이용할 수 있습니다.  
- **What Java version is supported?** Java 8 및 이후 버전을 완전히 지원합니다.  
- **Is the library thread‑safe?** 변환을 별도의 스레드에서 실행할 수 있으며, 모니터가 중단을 안전하게 처리합니다.

## 전제 조건

Interrupt Monitor 사용의 복잡한 내용에 들어가기 전에, 다음 전제 조건이 준비되어 있는지 확인하십시오:

- **Java Development Environment:** 시스템에 Java 개발 환경을 설정하십시오.  
- **Aspose.PSD Library:** Aspose.PSD for Java 라이브러리를 확보하십시오. [here](https://releases.aspose.com/psd/java/)에서 다운로드할 수 있습니다. 또한 메인 Aspose 사이트를 [here](https://releases.aspose.com/)에서 방문할 수 있습니다.  
- **Document Directory:** PSD 문서를 저장할 지정된 디렉터리를 준비하십시오.

## 패키지 가져오기

Java 프로젝트에 필요한 패키지를 가져오는 것으로 시작하십시오. 이렇게 하면 Aspose.PSD 기능에 접근할 수 있습니다.

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

이제 예제 코드를 단계별 가이드로 분해하여 Aspose.PSD for Java 프로젝트에 Interrupt Monitor를 통합하는 방법을 살펴보겠습니다.

## Interrupt Monitor를 사용하여 PSD를 PNG로 저장하는 방법?

`PsdImage`는 메모리에 로드된 PSD 문서를 나타냅니다.  
`SaveImageWorker`는 별도의 스레드에서 이미지 변환을 수행합니다.  

`new PsdImage("source.psd")`로 PSD 파일을 로드하고, `SaveImageWorker`에 `InterruptMonitor`를 연결한 뒤 `save("output.png", new PngOptions())`를 호출합니다. 모니터는 취소 요청을 감시하고 변환을 깔끔하게 중단하여 몇 밀리초 내에 애플리케이션으로 제어를 반환합니다.

### 1단계: 문서 디렉터리 설정

```java
String dataDir = "Your Document Directory";
```

“Your Document Directory”를 PSD 문서가 저장된 실제 경로로 교체하십시오.

### 2단계: 이미지 옵션 및 출력 경로 정의

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

이미지 옵션, 원본 PSD 파일 및 변환된 이미지의 원하는 출력 경로를 지정하십시오.

### 3단계: Interrupt Monitor 및 SaveImageWorker 초기화

`InterruptMonitor` 클래스는 실행 중인 변환을 감시하며 `requestInterrupt()`가 호출될 때 중단할 수 있습니다.  

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

`InterruptMonitor`와 `SaveImageWorker` 인스턴스를 생성하고, 모니터를 이미지 변환 작업자에 연결하십시오.

### 4단계: 이미지 변환 스레드 시작

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

이미지 변환 프로세스를 위한 새 스레드를 시작하고, 중단을 예상하기 위해 타임아웃 기간을 설정하십시오.

### 5단계: 프로세스 중단

`monitor.requestInterrupt()`를 호출하면 모니터가 진행 중인 변환을 중단하도록 신호를 보냅니다.  

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

`InterruptMonitor`를 사용하여 이미지 변환 프로세스를 중단하고 중단이 완료될 때까지 기다리십시오. 마지막으로 출력 파일을 삭제하여 정리합니다.

## PSD‑to‑PNG 변환에 Interrupt Monitor를 사용하는 이유

Aspose.PSD는 PNG, JPEG, BMP, TIFF 등을 포함한 **30개 이상의 출력 형식**을 지원하며, 전체 문서를 메모리에 로드하지 않고 **500 MB**까지의 파일을 처리할 수 있습니다. 인터럽트 모니터를 추가하면 CPU 낭비를 줄이고 배치 처리 파이프라인의 응답성을 향상시킬 수 있으며, 특히 변환이 예상 시간 제한을 초과할 때 유용합니다.

## 일반적인 문제와 해결책

- **Conversion hangs indefinitely:** 모니터가 `save`를 호출하기 **전**에 연결되었는지 확인하십시오.  
- **Output file is corrupted after interruption:** 모니터는 깔끔하게 중단하지만, 파일을 사용하기 전에 항상 파일이 존재하는지 확인하십시오.  
- **Thread‑safety concerns:** 각 변환을 별도의 스레드에서 실행하십시오; 모니터는 해당 작업자에만 영향을 미칩니다.

## 자주 묻는 질문

**Q1: Aspose.PSD for Java에서 Interrupt Monitor란 무엇인가요?**  
A: Interrupt Monitor는 개발자가 오래 걸리는 이미지 변환을 일시 중지하거나 취소할 수 있게 하여 리소스 사용을 실시간으로 제어할 수 있게 합니다.

**Q2: Aspose.PSD for Java 라이브러리를 어떻게 얻을 수 있나요?**  
A: Aspose.PSD for Java 라이브러리를 [here](https://releases.aspose.com/psd/java/)에서 다운로드할 수 있습니다.

**Q3: Aspose.PSD for Java에 대한 무료 체험판이 있나요?**  
A: 예, Aspose.PSD의 무료 체험판을 [here](https://releases.aspose.com/)에서 확인할 수 있습니다.

**Q4: Aspose.PSD for Java에 대한 지원을 어디서 찾을 수 있나요?**  
A: Aspose.PSD for Java 지원 포럼을 [here](https://forum.aspose.com/c/psd/34)에서 방문하십시오.

**Q5: Aspose.PSD for Java 라이선스를 어떻게 구매할 수 있나요?**  
A: Aspose.PSD for Java 라이선스를 [here](https://purchase.aspose.com/buy)에서 구매할 수 있습니다.

**Q6: 여러 PSD 파일을 동시에 PNG로 변환할 수 있나요?**  
A: 예, 각 파일마다 별도의 스레드를 생성하고 각 변환 작업자에 개별 `InterruptMonitor`를 연결하십시오.

**Q7: PSD‑to‑PNG 변환 시 라이브러리가 색 프로파일을 처리하나요?**  
A: 물론입니다; Aspose.PSD는 포함된 ICC 프로파일을 보존하고 자동으로 출력 PNG에 적용합니다.

---

**마지막 업데이트:** 2026-06-08  
**테스트 환경:** Aspose.PSD 23.12 for Java  
**작성자:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 관련 튜토리얼

- [Aspose.PSD for Java에서 PSD를 PNG로 저장하고 렌더링 드롭 섀도우 적용](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Aspose.PSD for Java를 사용하여 PSD를 PNG로 내보내고 새 일반 레이어 추가](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [PSD 파일에서 Interrupt Monitor 지원 - Java](/psd/java/psd-layer-management-effects/support-interrupt-monitor-psd-files/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}