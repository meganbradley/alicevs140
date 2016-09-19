---
title: "DISP_DEFVALUE"
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
ms.assetid: 05c64560-b5f7-44d9-8dc5-06a6b281b424
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DISP_DEFVALUE
Makes an existing property the default value of an object.  
  
## Syntax  
  
```  
  
DISP_DEFVALUE(  
theClass  
,   
pszName )  
```  
  
#### Parameters  
 `theClass`  
 Name of the class.  
  
 `pszName`  
 External name of the property that represents the "value" of the object.  
  
## Remarks  
 Using a default value can make programming your automation object simpler for Visual Basic applications.  
  
 The "default value" of your object is the property that is retrieved or set when a reference to an object does not specify a property or member function.  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [Dispatch Maps](../vs140/Dispatch-Maps.md)   
 [DECLARE_DISPATCH_MAP](../vs140/DECLARE_DISPATCH_MAP.md)   
 [DISP_PROPERTY_EX](../vs140/DISP_PROPERTY_EX.md)   
 [DISP_FUNCTION](../vs140/DISP_FUNCTION.md)   
 [BEGIN_DISPATCH_MAP](../vs140/BEGIN_DISPATCH_MAP.md)   
 [END_DISPATCH_MAP](../vs140/END_DISPATCH_MAP.md)