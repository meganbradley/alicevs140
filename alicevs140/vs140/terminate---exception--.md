---
title: "terminate (&lt;exception&gt;)"
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
ms.assetid: cd8f9085-254f-4948-9be2-ddbec3ad07ee
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# terminate (&lt;exception&gt;)
Calls a terminate handler.  
  
## Syntax  
  
```  
  
void terminate( );  
  
```  
  
## Remarks  
 The function calls a terminate handler, a function of type `void`. If **terminate** is called directly by the program, the terminate handler is the one most recently set by a call to [set_terminate](../vs140/set_terminate---exception--.md). If **terminate** is called for any of several other reasons during evaluation of a throw expression, the terminate handler is the one in effect immediately after evaluating the throw expression.  
  
 A terminate handler may not return to its caller. At program startup, the terminate handler is a function that calls **abort**.  
  
## Example  
 See [set_unexpected](../vs140/set_unexpected---exception--.md) for an example of the use of **terminate**.  
  
## Requirements  
 **Header:** <exception\>  
  
 **Namespace:** std