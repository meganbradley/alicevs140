---
title: "Reserved Words"
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
ms.assetid: 9b9f49e5-0739-45ab-a37e-81e3915ceb25
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Reserved Words
The following words are reserved by the linker. These names can be used as arguments in [module-definition statements](../vs140/Module-Definition--.Def--Files.md) only if the name is enclosed in double quotation marks ("").  
  
||||  
|-|-|-|  
|**APPLOADER**1|**INITINSTANCE**2|**PRELOAD**|  
|**BASE**|**IOPL**|**PRIVATE**|  
|**CODE**|**LIBRARY**1|**PROTMODE**2|  
|**CONFORMING**|**LOADONCALL**1|**PURE**1|  
|**DATA**|**LONGNAMES**2|**READONLY**|  
|**DESCRIPTION**|`MOVABLE`1|**READWRITE**|  
|**DEV386**|**MOVEABLE**1|**REALMODE**1|  
|**DISCARDABLE**|**MULTIPLE**|**RESIDENT**|  
|**DYNAMIC**|**NAME**|**RESIDENTNAME**1|  
|**EXECUTE-ONLY**|**NEWFILES**2|**SECTIONS**|  
|**EXECUTEONLY**|`NODATA`1|**SEGMENTS**|  
|**EXECUTEREAD**|**NOIOPL**1|**SHARED**|  
|**EXETYPE**|**NONAME**|**SINGLE**|  
|**EXPORTS**|**NONCONFORMING**1|**STACKSIZE**|  
|**FIXED**1|**NONDISCARDABLE**|**STUB**|  
|**FUNCTIONS**2|**NONE**|**VERSION**|  
|**HEAPSIZE**|**NONSHARED**|**WINDOWAPI**|  
|**IMPORTS**|**NOTWINDOWCOMPAT**1|**WINDOWCOMPAT**|  
|**IMPURE**1|**OBJECTS**|**WINDOWS**|  
|**INCLUDE**2|**OLD**1||  
  
 1 The linker emits a warning ("ignored") when it encounters this term. However, the word is still reserved.  
  
 2 The linker ignores this word but emits no warning.  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)   
 [Linker Options](../Topic/Linker%20Options.md)