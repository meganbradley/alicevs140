---
title: "MACRO"
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
ms.assetid: 89434f7c-bc2c-4e91-8940-fe2db8785233
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MACRO
Marks a macro block called *name* and establishes *parameter* placeholders for arguments passed when the macro is called.  
  
## Syntax  
  
```  
  
   name MACRO [[parameter [[:REQ | :=default | :VARARG]]]]...  
statements  
ENDM [[value]]  
```  
  
## Remarks  
 A macro function returns *value* to the calling statement.  
  
## See Also  
 [Directives Reference](../vs140/Directives-Reference.md)