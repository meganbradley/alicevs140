---
title: "Microsoft::WRL::Wrappers Namespace"
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
ms.topic: reference
ms.assetid: 36ac38c7-1fc3-42da-a879-5c68661dc9e1
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Microsoft::WRL::Wrappers Namespace
Defines Resource Acquisition Is Initialization (RAII) wrapper types that simplify the lifetime management of objects, strings, and handles.  
  
## Syntax  
  
```  
namespace Microsoft::WRL::Wrappers;  
```  
  
## Members  
  
### Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|`FileHandle`|`HandleT<HandleTraits::FileHandleTraits>`|  
  
### Classes  
  
|Name|Description|  
|----------|-----------------|  
|[CriticalSection Class](../vs140/CriticalSection-Class.md)|Represents a critical section object.|  
|[Event Class](../vs140/Event-Class--Windows-Runtime-C---Template-Library-.md)|Represents an event.|  
|[HandleT Class](../vs140/HandleT-Class.md)|Represents a handle to an object.|  
|[HString Class](../vs140/HString-Class.md)|Provides support for manipulating HSTRING handles.|  
|[HStringReference Class](../vs140/HStringReference-Class.md)|Represents an HSTRING that is created from an existing string.|  
|[Mutex Class](../vs140/Mutex-Class.md)|Represents a synchronization object that exclusively controls a shared resource.|  
|[RoInitializeWrapper Class](../vs140/RoInitializeWrapper-Class.md)|Initializes the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].|  
|[Semaphore Class](../vs140/Semaphore-Class.md)|Represents a synchronization object that controls a shared resource that can support a limited number of users.|  
|[SRWLock Class](../vs140/SRWLock-Class.md)|Represents a slim reader/writer lock.|  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## See Also  
 [Microsoft::WRL Namespace](../vs140/Microsoft--WRL-Namespace.md)