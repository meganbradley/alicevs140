---
title: "_U_STRINGorID::_U_STRINGorID"
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
ms.assetid: 9b6fd512-10b0-4a9c-95ff-2566a5d8623a
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _U_STRINGorID::_U_STRINGorID
The **UINT** constructor converts its argument to a resource type compatible with Windows resource-management functions using the **MAKEINTRESOURCE** macro and the result is stored in the class's single data member, [m_lpstr](../vs140/_U_STRINGorID--m_lpstr.md).  
  
## Syntax  
  
```  
  
      _U_STRINGorID(  
   UINT nID   
);  
_U_STRINGorID(  
   LPCTSTR lpString   
);  
```  
  
#### Parameters  
 `nID`  
 A resource ID.  
  
 `lpString`  
 A resource name.  
  
## Remarks  
 The argument to the `LPCTSTR` constructor is stored directly without conversion.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [_U_STRINGorID Class](../vs140/_U_STRINGorID-Class.md)   
 [_U_STRINGorID::m_lpstr](../vs140/_U_STRINGorID--m_lpstr.md)