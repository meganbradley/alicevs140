---
title: "COMM"
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
ms.assetid: a23548c4-ad04-41fa-91da-945f228de742
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COMM
Creates a communal variable with the attributes specified in `definition`.  
  
## Syntax  
  
```  
  
COMM definition [[, definition]] ...  
```  
  
## Remarks  
 Each `definition` has the following form:  
  
 [[*langtype*]] [[**NEAR** &#124; **FAR**]] *label***:**`type`[[**:***count*]]  
  
 The *label* is the name of the variable. The `type` can be any type specifier ([BYTE](../vs140/BYTE--MASM-.md), [WORD](../vs140/WORD.md), and so on) or an integer specifying the number of bytes. The *count* specifies the number of data objects (one is the default).  
  
## See Also  
 [Directives Reference](../vs140/Directives-Reference.md)