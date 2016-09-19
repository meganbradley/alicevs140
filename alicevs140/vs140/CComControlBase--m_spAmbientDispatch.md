---
title: "CComControlBase::m_spAmbientDispatch"
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
ms.assetid: 848d8288-6eb0-4f93-b825-fcb9609596ee
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::m_spAmbientDispatch
A `CComDispatchDriver` object that lets you retrieve and set an object's properties through an `IDispatch` pointer.  
  
## Syntax  
  
```  
  
CComDispatchDriver m_spAmbientDispatch;  
```  
  
## Remarks  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)   
 [CComDispatchDriver](../vs140/CComDispatchDriver.md)