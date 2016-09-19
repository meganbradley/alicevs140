---
title: "BEGIN_CONNECTION_PART"
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
ms.assetid: b9588d3e-e582-4f53-b1ab-b7ebb4380dbb
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BEGIN_CONNECTION_PART
Use the `BEGIN_CONNECTION_PART` macro to begin the definition of additional connection points beyond the event and property notification connection points.  
  
## Syntax  
  
```  
  
BEGIN_CONNECTION_PART(  
theClass  
,   
localClass )  
```  
  
#### Parameters  
 `theClass`  
 Specifies the name of the control class whose connection point this is.  
  
 *localClass*  
 Specifies the name of the local class that implements the connection point.  
  
## Remarks  
 In the declaration (.h) file that defines the member functions for your class, start the connection point with the `BEGIN_CONNECTION_PART` macro, then add the `CONNECTION_IID` macro and any other member functions you wish to implement, and complete the connection point map with the `END_CONNECTION_PART` macro.  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [BEGIN_CONNECTION_MAP](../vs140/BEGIN_CONNECTION_MAP.md)   
 [END_CONNECTION_PART](../vs140/END_CONNECTION_PART.md)   
 [DECLARE_CONNECTION_MAP](../vs140/DECLARE_CONNECTION_MAP.md)