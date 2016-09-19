---
title: "ML Nonfatal Error A2085"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c2fef415-a32b-4249-896c-6d981fc6e327
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ML Nonfatal Error A2085
**instruction or register not accepted in current CPU mode**  
  
 An attempt was made to use an instruction, register, or keyword that was not valid for the current processor mode.  
  
 For example, 32-bit registers require [.386](../vs140/.386.md) or above. Control registers such as CR0 require privileged mode [.386P](../vs140/.386P.md) or above. This error will also be generated for the **NEAR32**, **FAR32**, and **FLAT** keywords, which require .**386** or above.  
  
## See Also  
 [ML Error Messages](../vs140/ML-Error-Messages.md)