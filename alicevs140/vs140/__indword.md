---
title: "__indword"
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
ms.assetid: 1068d686-586e-4e36-b962-d1d7c3315260
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __indword
**Microsoft Specific**  
  
 Reads one double word of data from the specified port using the `in` instruction.  
  
## Syntax  
  
```  
unsigned long __indword(  
   unsigned short Port  
);  
```  
  
#### Parameters  
 [in] `Port`  
 The port to read from.  
  
## Return Value  
 The word read from the port.  
  
## Requirements  
  
|Intrinsic|Architecture|  
|---------------|------------------|  
|`__indword`|x86, [!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|  
  
 **Header file** <intrin.h>  
  
## Remarks  
 This routine is only available as an intrinsic.  
  
## END Microsoft Specific  
  
## See Also  
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)