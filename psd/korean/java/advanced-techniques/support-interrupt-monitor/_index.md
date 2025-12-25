---
date: 2025-12-25
description: Aspose.PSD for Java를 사용하여 인터럽트 모니터 지원과 함께 PSD를 PNG로 변환하는 방법을 배우고, Java
  스레드 인터럽트 예제와 PSD를 PNG로 저장하는 팁을 포함합니다.
linktitle: Support for Interrupt Monitor
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java에서 인터럽트 모니터 지원을 사용하여 PSD를 PNG로 변환하는 방법
url: /ko/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java의 Interrupt Monitor를 사용하여 PSD를 PNG로 변환하기

## 소개

전체적인 이미지 변환 제어가 필요한 **PSD를 PNG로 변환**이 필요하다면, Aspose.PSD for Java의 Interrupt Monitor가 바로 찾던 도구입니다. 이번 튜토리얼에서는 변환 중간에 중단할 수 있는 실제 **java thread interrupt example**을 살펴보며, 리소스 관리, 타임아웃 적용, 사용자 취소에 대응할 수 있는 유연성을 제공합니다.

## 빠른 답변
- **Interrupt Monitor는 무엇을 하나요?** 진행 중인 이미지 변환을 안전하게 중지하도록 신호를 보낼 수 있습니다.  
- **이것으로 PSD를 PNG로 변환할 수 있나요?** 네 – 모니터는 PNG를 포함한 모든 저장 작업에서 작동합니다.  
- **별도의 스레드가 필요합니까?** 일반적으로 변환을 별도 스레드에서 실행하여 중단할 수 있습니다.  
- **필요한 Aspose.PSD 버전은?** `com.aspose.psd.multithreading.InterruptMonitor`가 포함된 최신 버전이면 됩니다.  
- **프로덕션에 라이선스가 필요합니까?** 네, 비시험용으로는 유효한 Aspose.PSD 라이선스가 필요합니다.

## Interrupt Monitor와 함께 “PSD를 PNG로 변환”이란 무엇인가요?

대용량 Photoshop 문서(PSD/PSB)를 PNG 이미지로 변환하는 작업은 CPU 집약적일 수 있습니다. 변환 작업자에 **Interrupt Monitor**를 연결하면 프로그래밍 방식으로 프로세스를 중단할 수 있어, 웹 서비스, 배치 작업, 사용자 취소가 가능한 UI 애플리케이션 등에 최적입니다.

## 왜 Interrupt Monitor를 사용하나요?
- **반응형 UI:** 큰 파일을 처리하는 동안 애플리케이션이 멈추는 것을 방지합니다.  
- **리소스 관리:** 시간이나 메모리 한도를 초과하는 변환을 중단합니다.  
- **오류 처리:** 중단이 발생했을 때 부분적으로 생성된 출력 파일을 정상적으로 정리합니다.

## 사전 요구 사항

- Java 개발 환경 (JDK 8 이상).  
- Aspose.PSD for Java 라이브러리 – **[여기](https://releases.aspose.com/psd/java/)**에서 다운로드하세요.  
- 작업하려는 PSD/PSB 파일이 들어 있는 폴더.

## 패키지 가져오기

필요한 클래스를 가져와 이미지 옵션, Interrupt Monitor, 스레드 유틸리티에 접근합니다.

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

## 단계별 가이드

### 단계 1: 문서 디렉터리 설정

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"`를 PSD 파일이 위치한 절대 경로로 교체하세요.

### 단계 2: 이미지 옵션 및 출력 경로 정의

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

`PngOptions`를 사용하여 **PSD를 PNG로 저장**합니다. 필요에 따라 파일 이름을 조정하세요.

### 단계 3: Interrupt Monitor 및 SaveImageWorker 초기화

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

`InterruptMonitor` 인스턴스는 나중에 변환을 중지하는 데 사용됩니다. `SaveImageWorker`는 모니터를 변환 작업에 연결합니다.

### 단계 4: 별도 스레드에서 이미지 변환 시작

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

백그라운드 스레드에서 변환을 시작하여 메인 스레드가 응답성을 유지하도록 합니다. `Thread.sleep(3000)` 호출은 타임아웃 상황을 시뮬레이션합니다.

### 단계 5: 프로세스 중단 (Java Thread Interrupt 예제)

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

`monitor.interrupt()`를 호출하면 **중단 모니터** 로직이 실행됩니다. 중단 후에는 부분적으로 작성된 PNG 파일을 정리합니다.

## 일반적인 문제 및 해결책

| 문제 | 원인 | 해결 방법 |
|------|------|-----------|
| 변환이 절대 중지되지 않음 | 모니터가 워커에 연결되지 않음 | `SaveImageWorker`가 동일한 `InterruptMonitor` 인스턴스를 받도록 보장하세요. |
| 중단 후에도 출력 파일이 남음 | 정리 코드가 실행되지 않음 | `finally` 블록이 실행되는지와 파일 경로가 올바른지 확인하세요. |
| 대용량 PSB 파일에서 `OutOfMemoryError` | 스트리밍 옵션을 사용하지 않음 | 메모리 효율적인 로딩을 가능하게 하는 `LoadOptions`와 함께 `PsdImage`를 사용하세요. |

## 자주 묻는 질문

### Q1: Aspose.PSD for Java에서 Interrupt Monitor란 무엇인가요?

A1: Interrupt Monitor는 개발자가 이미지 변환 프로세스를 **관리하고 중단**할 수 있게 하여, 장시간 실행되는 작업을 세밀하게 제어할 수 있도록 합니다.

### Q2: Aspose.PSD for Java 라이브러리를 어떻게 얻을 수 있나요?

A2: Aspose.PSD for Java 라이브러리를 **[여기](https://releases.aspose.com/psd/java/)**에서 다운로드할 수 있습니다.

### Q3: Aspose.PSD for Java의 무료 체험판이 있나요?

A3: 네, Aspose.PSD의 무료 체험판을 **[여기](https://releases.aspose.com/)**에서 확인할 수 있습니다.

### Q4: Aspose.PSD for Java 지원을 어디서 찾을 수 있나요?

A4: Aspose.PSD for Java 지원 포럼은 **[여기](https://forum.aspose.com/c/psd/34)**에서 확인하세요.

### Q5: Aspose.PSD for Java 라이선스를 어떻게 구매하나요?

A5: Aspose.PSD for Java 라이선스는 **[여기](https://purchase.aspose.com/buy)**에서 구매할 수 있습니다.

**마지막 업데이트:** 2025-12-25  
**테스트 환경:** Aspose.PSD 24.11 for Java  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}