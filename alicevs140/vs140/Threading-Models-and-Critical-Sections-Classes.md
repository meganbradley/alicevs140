---
title: "Threading Models and Critical Sections Classes"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 759f05ef-6285-4be6-a2cc-78572dd75146
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Threading Models and Critical Sections Classes
The following classes define a threading model and critical section:  
  
-   [CAtlAutoThreadModule](../vs140/CAtlAutoThreadModule-Class.md) Implements a thread-pooled, apartment-model COM server.  
  
-   [CAtlAutoThreadModuleT](../vs140/CAtlAutoThreadModuleT-Class.md) Provides methods for implementing a thread-pooled, apartment-model COM server.  
  
-   [CComMultiThreadModel](../vs140/CComMultiThreadModel-Class.md) Provides thread-safe methods for incrementing and decrementing a variable. Provides a critical section.  
  
-   [CComMultiThreadModelNoCS](../vs140/CComMultiThreadModelNoCS-Class.md) Provides thread-safe methods for incrementing and decrementing a variable. Does not provide a critical section.  
  
-   [CComSingleThreadModel](../vs140/CComSingleThreadModel-Class.md) Provides methods for incrementing and decrementing a variable. Does not provide a critical section.  
  
-   [CComObjectThreadModel](../vs140/CComObjectThreadModel.md) Determines the appropriate threading-model class for a single object class.  
  
-   [CComGlobalsThreadModel](../vs140/CComGlobalsThreadModel.md) Determines the appropriate threading-model class for an object that is globally available.  
  
-   [CComAutoCriticalSection](../vs140/CComAutoCriticalSection-Class.md) Contains methods for obtaining and releasing a critical section. The critical section is automatically initialized.  
  
-   [CComCriticalSection](../vs140/CComCriticalSection-Class.md) Contains methods for obtaining and releasing a critical section. The critical section must be explicitly initialized.  
  
-   [CComFakeCriticalSection](../vs140/CComFakeCriticalSection-Class.md) Mirrors the methods in `CComCriticalSection` without providing a critical section. The methods in `CComFakeCriticalSection` do nothing.  
  
-   [CRTThreadTraits](../vs140/CRTThreadTraits-Class.md) Provides the creation function for a CRT thread. Use this class if the thread will use CRT functions.  
  
-   [Win32ThreadTraits](../vs140/Win32ThreadTraits-Class.md) Provides the creation function for a Windows thread. Use this class if the thread will not use CRT functions.  
  
## See Also  
 [Class Overview](../vs140/ATL-Class-Overview.md)