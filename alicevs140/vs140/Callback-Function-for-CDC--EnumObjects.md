---
title: "Callback Function for CDC::EnumObjects"
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
ms.assetid: 380088b1-88a5-4fb4-bbb5-dd9e8386572b
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Callback Function for CDC::EnumObjects
The *ObjectFunc* name is a placeholder for the application-supplied function name.  
  
## Syntax  
  
```  
  
      int CALLBACK EXPORT ObjectFunc(   
   LPSTR lpszLogObject,   
   LPSTR* lpData    
);  
```  
  
#### Parameters  
 *lpszLogObject*  
 Points to a [LOGPEN](../vs140/LOGPEN-Structure.md) or [LOGBRUSH](../vs140/LOGBRUSH-Structure.md) data structure that contains information about the logical attributes of the object.  
  
 `lpData`  
 Points to the application-supplied data passed to the `EnumObjects` function.  
  
## Return Value  
 The callback function returns an `int`. The value of this return is user-defined. If the callback function returns 0, `EnumObjects` stops enumeration early.  
  
## Remarks  
 The actual name must be exported.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [Structures, Styles, Callbacks, and Message Maps](../vs140/Structures--Styles--Callbacks--and-Message-Maps.md)   
 [CDC::EnumObjects](../vs140/CDC--EnumObjects.md)