---
title: "PX_Picture"
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
ms.assetid: 4cf86ec1-a14a-4786-973a-c45509994b34
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# PX_Picture
Call this function within your control's `DoPropExchange` member function to serialize or initialize a picture property of your control.  
  
## Syntax  
  
```  
  
      BOOL PX_Picture(  
   CPropExchange* pPX,  
   LPCTSTR pszPropName,  
   CPictureHolder& pict   
);  
BOOL PX_Picture(  
   CPropExchange* pPX,  
   LPCTSTR pszPropName,  
   CPictureHolder& pict,  
   CPictureHolder& pictDefault   
);  
```  
  
#### Parameters  
 `pPX`  
 Pointer to the [CPropExchange](../vs140/CPropExchange-Class.md) object (typically passed as a parameter to `DoPropExchange`).  
  
 `pszPropName`  
 The name of the property being exchanged.  
  
 `pict`  
 Reference to a [CPictureHolder](../vs140/CPictureHolder-Class.md) object where the property is stored (typically a member variable of your class).  
  
 `pictDefault`  
 Default value for the property.  
  
## Return Value  
 Nonzero if the exchange was successful; 0 if unsuccessful.  
  
## Remarks  
 The property's value is read from or written to the variable referenced by `pict`, as appropriate. If `pictDefault` is specified, it will be used as the property's default value. This value is used if, for any reason, the control's serialization process fails.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [COleControl::DoPropExchange](../vs140/COleControl--DoPropExchange.md)