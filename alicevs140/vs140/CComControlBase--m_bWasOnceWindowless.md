---
title: "CComControlBase::m_bWasOnceWindowless"
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
ms.assetid: af2d1477-b3e4-41bb-89ab-afee281b9d37
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::m_bWasOnceWindowless
Flag indicating the control has been windowless, but may or may not be windowless now.  
  
## Syntax  
  
```  
  
unsigned m_bWasOnceWindowless:1;  
```  
  
## Remarks  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)   
 [CComControlBase::m_bWndLess](../vs140/CComControlBase--m_bWndLess.md)