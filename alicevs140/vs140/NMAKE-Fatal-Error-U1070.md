---
title: "NMAKE Fatal Error U1070"
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
ms.topic: error-reference
ms.assetid: 8639fc39-b4b1-48f5-ac91-0e9fb61680fd
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# NMAKE Fatal Error U1070
cycle in macro definition 'macroname'  
  
 The given macro definition contained a macro whose definition contained the given macro. Circular macro definitions are invalid.  
  
## Example  
 The following macro definitions  
  
```  
ONE=$(TWO)  
TWO=$(ONE)  
```  
  
 cause the following error:  
  
```  
cycle in macro definition 'TWO'  
```