---
title: "COleControl::GetAmbientProperty"
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
ms.topic: reference
ms.assetid: b6a8c3b2-6f4f-48b0-9074-a3c86c4af025
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::GetAmbientProperty
Gets the value of an ambient property of the container.  
  
## Syntax  
  
```  
  
      BOOL GetAmbientProperty(  
   DISPID dispid,  
   VARTYPE vtProp,  
   void* pvProp   
);  
```  
  
#### Parameters  
 *dwDispid*  
 The dispatch ID of the desired ambient property.  
  
 `vtProp`  
 A variant type tag that specifies the type of the value to be returned in `pvProp`.  
  
 `pvProp`  
 A pointer to the address of the variable that will receive the property value or return value. The actual type of this pointer must match the type specified by `vtProp`.  
  
|vtProp|Type of pvProp|  
|------------|--------------------|  
|`VT_BOOL`|**BOOL\***|  
|`VT_BSTR`|**CString\***|  
|`VT_I2`|**short\***|  
|`VT_I4`|**long\***|  
|`VT_R4`|**float\***|  
|`VT_R8`|**double\***|  
|`VT_CY`|**CY\***|  
|**VT_COLOR**|**OLE_COLOR\***|  
|**VT_DISPATCH**|**LPDISPATCH\***|  
|**VT_FONT**|**LPFONTDISP\***|  
  
## Return Value  
 Nonzero if the ambient property is supported; otherwise 0.  
  
## Remarks  
 If you use `GetAmbientProperty` to retrieve the ambient DisplayName and ScaleUnits properties, set `vtProp` to `VT_BSTR` and `pvProp` to **CString\***. If you are retrieving the ambient Font property, set `vtProp` to **VT_FONT** and `pvProp` to **LPFONTDISP\***.  
  
 Note that functions have already been provided for common ambient properties, such as [AmbientBackColor](../vs140/COleControl--AmbientBackColor.md) and [AmbientFont](../vs140/COleControl--AmbientFont.md).  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::AmbientForeColor](../vs140/COleControl--AmbientForeColor.md)   
 [COleControl::AmbientScaleUnits](../vs140/COleControl--AmbientScaleUnits.md)   
 [COleControl::AmbientShowGrabHandles](../vs140/COleControl--AmbientShowGrabHandles.md)