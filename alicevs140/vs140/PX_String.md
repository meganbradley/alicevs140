---
title: "PX_String"
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
ms.assetid: c0d854f2-208b-45d4-b52f-50dccc812d31
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# PX_String
Call this function within your control's **DoPropExchange** member function to serialize or initialize a character string property.  
  
## Syntax  
  
```  
  
      BOOL PX_String(  
   CPropExchange* pPX,  
   LPCTSTR pszPropName,  
   CString& strValue   
);  
BOOL PX_String(  
   CPropExchange* pPX,  
   LPCTSTR pszPropName,  
   CString& strValue,  
   CString strDefault   
);  
```  
  
#### Parameters  
 `pPX`  
 Pointer to the [CPropExchange](../vs140/CPropExchange-Class.md) object (typically passed as a parameter to `DoPropExchange`).  
  
 `pszPropName`  
 The name of the property being exchanged.  
  
 `strValue`  
 Reference to the variable where the property is stored (typically a member variable of your class).  
  
 `strDefault`  
 Default value for the property.  
  
## Return Value  
 Nonzero if the exchange was successful; 0 if unsuccessful.  
  
## Remarks  
 The property's value is read from or written to the variable referenced by `strValue`, as appropriate. If `strDefault` is specified, it will be used as the property's default value. This value is used if, for any reason, the control's serialization process fails.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [COleControl::DoPropExchange](../vs140/COleControl--DoPropExchange.md)   
 [CStringT Class](../vs140/CStringT-Class.md)