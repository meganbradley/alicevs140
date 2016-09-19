---
title: "DISP_PROPERTY_PARAM"
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
ms.assetid: 2047db26-7f98-4194-a1de-d2eccf7e5681
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DISP_PROPERTY_PARAM
Defines a property accessed with separate **Get** and `Set` member functions.  
  
## Syntax  
  
```  
  
DISP_PROPERTY_PARAM(  
theClass  
,   
pszExternalName  
,   
pfnGet  
,   
pfnSet  
,   
vtPropType  
,   
vtsParams  
 )  
  
```  
  
#### Parameters  
 `theClass`  
 Name of the class.  
  
 *pszExternalName*  
 External name of the property.  
  
 `pfnGet`  
 Name of the member function used to get the property.  
  
 `pfnSet`  
 Name of the member function used to set the property.  
  
 `vtPropType`  
 A value specifying the property's type.  
  
 `vtsParams`  
 A string of space-separated **VTS_** variant parameter types, one for each parameter.  
  
## Remarks  
 Unlike the `DISP_PROPERTY_EX` macro, this macro allows you to specify a parameter list for the property. This is useful for implementing properties that are indexed or parameterized.  
  
## Example  
 Consider the following declaration of get and set member functions that allow the user to request a specific row and column when accessing the property:  
  
 [!CODE [NVC_MFCActiveXControl#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCActiveXControl#9)]  
  
 These correspond to the following `DISP_PROPERTY_PARAM` macro in the control dispatch map:  
  
 [!CODE [NVC_MFCActiveXControl#10](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCActiveXControl#10)]  
  
 As another example, consider the following get and set member functions:  
  
 [!CODE [NVC_MFCActiveXControl#11](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCActiveXControl#11)]  
  
 These correspond to the following `DISP_PROPERTY_PARAM` macro in the control dispatch map:  
  
 [!CODE [NVC_MFCActiveXControl#12](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCActiveXControl#12)]  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [Dispatch Maps](../vs140/Dispatch-Maps.md)   
 [DISP_PROPERTY_EX](../vs140/DISP_PROPERTY_EX.md)