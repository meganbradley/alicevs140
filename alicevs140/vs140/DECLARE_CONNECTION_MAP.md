---
title: "DECLARE_CONNECTION_MAP"
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
ms.assetid: 57ed7f69-6ade-4620-9917-2b70631d280d
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_CONNECTION_MAP
Each `COleControl`-derived class in your program can provide a connection map to specify additional connection points that your control supports.  
  
## Syntax  
  
```  
  
DECLARE_CONNECTION_MAP( )  
```  
  
## Remarks  
 If your control supports additional points, use the `DECLARE_CONNECTION_MAP` macro at the end of your class declaration. Then, in the .cpp file that defines the member functions for the class, use the `BEGIN_CONNECTION_MAP` macro, `CONNECTION_PART` macros for each of the control's connection points, and the `END_CONNECTION_MAP` macro to declare the end of the connection map.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [BEGIN_CONNECTION_PART](../vs140/BEGIN_CONNECTION_PART.md)   
 [BEGIN_CONNECTION_MAP](../vs140/BEGIN_CONNECTION_MAP.md)   
 [CONNECTION_IID](../vs140/CONNECTION_IID.md)