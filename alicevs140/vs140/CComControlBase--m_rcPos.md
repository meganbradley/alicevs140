---
title: "CComControlBase::m_rcPos"
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
ms.assetid: 4d536492-f486-491c-8de0-3374f4ecd948
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::m_rcPos
The position in pixels of the control, expressed in the coordinates of the container.  
  
## Syntax  
  
```  
  
RECT m_rcPos;  
```  
  
## Remarks  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)   
 [CComControlBase::m_sizeExtent](../vs140/CComControlBase--m_sizeExtent.md)   
 [CComControlBase::m_sizeNatural](../vs140/CComControlBase--m_sizeNatural.md)   
 [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897)