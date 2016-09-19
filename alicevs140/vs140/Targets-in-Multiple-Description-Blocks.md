---
title: "Targets in Multiple Description Blocks"
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
ms.assetid: 8618dcd9-c11d-4562-91a7-0c904ed438a8
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Targets in Multiple Description Blocks
To update a target in more than one description block using different commands, specify two consecutive colons (::) between targets and dependents.  
  
```  
target.lib :: one.asm two.asm three.asm  
    ml one.asm two.asm three.asm  
    lib target one.obj two.obj three.obj  
target.lib :: four.c five.c  
    cl /c four.c five.c  
    lib target four.obj five.obj  
```  
  
## See Also  
 [Targets](../vs140/Targets.md)