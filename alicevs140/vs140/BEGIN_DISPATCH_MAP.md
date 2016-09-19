---
title: "BEGIN_DISPATCH_MAP"
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
ms.assetid: 49e2651e-d97c-4e17-8d41-7011d8920a15
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BEGIN_DISPATCH_MAP
Declares the definition of your dispatch map.  
  
## Syntax  
  
```  
  
BEGIN_DISPATCH_MAP(  
theClass  
,   
baseClass )  
```  
  
#### Parameters  
 `theClass`  
 Specifies the name of the class that owns this dispatch map.  
  
 `baseClass`  
 Specifies the base class name of `theClass`.  
  
## Remarks  
 In the implementation (.cpp) file that defines the member functions for your class, start the dispatch map with the `BEGIN_DISPATCH_MAP` macro, add macro entries for each of your dispatch functions and properties, and complete the dispatch map with the `END_DISPATCH_MAP` macro.  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [Dispatch Maps](../vs140/Dispatch-Maps.md)   
 [DECLARE_DISPATCH_MAP](../vs140/DECLARE_DISPATCH_MAP.md)   
 [END_DISPATCH_MAP](../vs140/END_DISPATCH_MAP.md)   
 [DISP_FUNCTION](../vs140/DISP_FUNCTION.md)   
 [DISP_PROPERTY](../vs140/DISP_PROPERTY.md)   
 [DISP_PROPERTY_EX](../vs140/DISP_PROPERTY_EX.md)   
 [DISP_DEFVALUE](../vs140/DISP_DEFVALUE.md)