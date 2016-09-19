---
title: "DECLARE_OLECREATE"
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
ms.assetid: 8d9fd746-b7dd-45f3-92f5-82e8ac7d496d
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_OLECREATE
Enables objects of `CCmdTarget`-derived classes to be created through OLE automation.  
  
## Syntax  
  
```  
  
DECLARE_OLECREATE(  
class_name )  
```  
  
#### Parameters  
 *class_name*  
 The actual name of the class.  
  
## Remarks  
 This macro enables other OLE-enabled applications to create objects of this type.  
  
 Add the `DECLARE_OLECREATE` macro in the .h module for the class, and then include that module in all .cpp modules that need access to objects of this class.  
  
 If `DECLARE_OLECREATE` is included in the class declaration, then `IMPLEMENT_OLECREATE` must be included in the class implementation. A class declaration using `DECLARE_OLECREATE` must also use `DECLARE_DYNCREATE` or `DECLARE_SERIAL`.  
  
## Requirements  
 **Header**: afxdisp.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [IMPLEMENT_OLECREATE](../vs140/IMPLEMENT_OLECREATE.md)   
 [DECLARE_DYNCREATE](../vs140/DECLARE_DYNCREATE.md)   
 [DECLARE_SERIAL](../vs140/DECLARE_SERIAL.md)