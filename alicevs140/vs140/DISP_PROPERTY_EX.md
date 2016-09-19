---
title: "DISP_PROPERTY_EX"
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
ms.assetid: 7c4749f7-8562-42c4-a8ad-286299bfa4b7
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DISP_PROPERTY_EX
Defines an OLE automation property and name the functions used to get and set the property's value in a dispatch map.  
  
## Syntax  
  
```  
  
DISP_PROPERTY_EX(  
theClass  
,   
pszName  
,   
memberGet  
,   
memberSet  
,   
vtPropType )  
```  
  
#### Parameters  
 `theClass`  
 Name of the class.  
  
 `pszName`  
 External name of the property.  
  
 `memberGet`  
 Name of the member function used to get the property.  
  
 `memberSet`  
 Name of the member function used to set the property.  
  
 `vtPropType`  
 A value specifying the property's type.  
  
## Remarks  
 The `memberGet` and `memberSet` functions have signatures determined by the `vtPropType` argument. The `memberGet` function takes no arguments and returns a value of the type specified by `vtPropType`. The `memberSet` function takes an argument of the type specified by `vtPropType` and returns nothing.  
  
 The `vtPropType` argument is of type **VARTYPE**. Possible values for this argument are taken from the `VARENUM` enumeration. For a list of these values, see the Remarks for the `vtRetVal` parameter in [DISP_FUNCTION](../vs140/DISP_FUNCTION.md). Note that `VT_EMPTY`, listed in the `DISP_FUNCTION` remarks, is not permitted as a property data type.  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [Dispatch Maps](../vs140/Dispatch-Maps.md)   
 [DECLARE_DISPATCH_MAP](../vs140/DECLARE_DISPATCH_MAP.md)   
 [DISP_PROPERTY](../vs140/DISP_PROPERTY.md)   
 [DISP_FUNCTION](../vs140/DISP_FUNCTION.md)   
 [BEGIN_DISPATCH_MAP](../vs140/BEGIN_DISPATCH_MAP.md)   
 [END_DISPATCH_MAP](../vs140/END_DISPATCH_MAP.md)