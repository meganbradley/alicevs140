---
title: "PX_Float"
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
ms.assetid: 6928452d-3a4a-482d-acdb-936ef83bbcf9
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# PX_Float
Call this function within your control's `DoPropExchange` member function to serialize or initialize a property of type **float**.  
  
## Syntax  
  
```  
  
      BOOL PX_Float(  
   CPropExchange* pPX,  
   LPCTSTR pszPropName,  
   float& floatValue   
);  
BOOL PX_Float(  
   CPropExchange* pPX,  
   LPCTSTR pszPropName,  
   float& floatValue,  
   float floatDefault   
);  
```  
  
#### Parameters  
 `pPX`  
 Pointer to the [CPropExchange](../vs140/CPropExchange-Class.md) object (typically passed as a parameter to `DoPropExchange`).  
  
 `pszPropName`  
 The name of the property being exchanged.  
  
 `floatValue`  
 Reference to the variable where the property is stored (typically a member variable of your class).  
  
 `floatDefault`  
 Default value for the property.  
  
## Return Value  
 Nonzero if the exchange was successful; 0 if unsuccessful.  
  
## Remarks  
 The property's value is read from or written to the variable referenced by `floatValue`, as appropriate. If `floatDefault` is specified, it will be used as the property's default value. This value is used if, for any reason, the control's serialization process fails.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [COleControl::DoPropExchange](../vs140/COleControl--DoPropExchange.md)   
 [PX_Double](../vs140/PX_Double.md)   
 [PX_String](../vs140/PX_String.md)