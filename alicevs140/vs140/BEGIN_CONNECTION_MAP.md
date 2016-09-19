---
title: "BEGIN_CONNECTION_MAP"
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
ms.assetid: 1e66bcc3-3610-49ae-8211-1d5b19efbe46
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BEGIN_CONNECTION_MAP
Each `COleControl`-derived class in your program can provide a connection map to specify connection points that your control will support.  
  
## Syntax  
  
```  
  
BEGIN_CONNECTION_MAP(  
theClass  
,   
theBase )  
```  
  
#### Parameters  
 `theClass`  
 Specifies the name of the control class whose connection map this is.  
  
 *theBase*  
 Specifies the name of the base class of `theClass`.  
  
## Remarks  
 In the implementation (.CPP) file that defines the member functions for your class, start the connection map with the `BEGIN_CONNECTION_MAP` macro, then add macro entries for each of your connection points using the [CONNECTION_PART](../vs140/CONNECTION_PART.md) macro. Finally, complete the connection map with the [END_CONNECTION_MAP](../vs140/END_CONNECTION_MAP.md) macro.  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [BEGIN_CONNECTION_PART](../vs140/BEGIN_CONNECTION_PART.md)   
 [DECLARE_CONNECTION_MAP](../vs140/DECLARE_CONNECTION_MAP.md)