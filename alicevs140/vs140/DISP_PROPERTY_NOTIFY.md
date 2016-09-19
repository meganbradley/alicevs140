---
title: "DISP_PROPERTY_NOTIFY"
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
ms.assetid: 2c22c48d-ab55-4b21-a545-a125546a6512
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DISP_PROPERTY_NOTIFY
Defines an OLE automation property with notification in a dispatch map.  
  
## Syntax  
  
```  
  
DISP_PROPERTY_NOTIFY(  
theClass  
,   
szExternalName  
,   
memberName  
,   
pfnAfterSet  
,   
vtPropType  
 )  
  
```  
  
#### Parameters  
 `theClass`  
 Name of the class.  
  
 `szExternalName`  
 External name of the property.  
  
 `memberName`  
 Name of the member variable in which the property is stored.  
  
 `pfnAfterSet`  
 Name of the notification function for `szExternalName`.  
  
 `vtPropType`  
 A value specifying the property's type.  
  
## Remarks  
 Unlike properties defined with `DISP_PROPERTY`, a property defined with `DISP_PROPERTY_NOTIFY` will automatically call the function specified by `pfnAfterSet` when the property is changed.  
  
 The `vtPropType` argument is of type **VARTYPE**. Possible values for this argument are taken from the `VARENUM` enumeration:  
  
|Symbol|**Property type**|  
|------------|-----------------------|  
|`VT_I2`|**short**|  
|`VT_I4`|**long**|  
|`VT_R4`|**float**|  
|`VT_R8`|**double**|  
|`VT_CY`|**CY**|  
|`VT_DATE`|**DATE**|  
|`VT_BSTR`|`CString`|  
|**VT_DISPATCH**|`LPDISPATCH`|  
|`VT_ERROR`|`SCODE`|  
|`VT_BOOL`|**BOOL**|  
|**VT_VARIANT**|**VARIANT**|  
|**VT_UNKNOWN**|`LPUNKNOWN`|  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [Dispatch Maps](../vs140/Dispatch-Maps.md)   
 [DISP_PROPERTY](../vs140/DISP_PROPERTY.md)   
 [DISP_FUNCTION](../vs140/DISP_FUNCTION.md)