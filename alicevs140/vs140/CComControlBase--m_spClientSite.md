---
title: "CComControlBase::m_spClientSite"
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
ms.assetid: 9883c293-8b58-4e18-ba1d-2c8005d61358
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::m_spClientSite
A pointer to the control's client site within the container.  
  
## Syntax  
  
```  
  
CComPtr<IOleClientSite> m_spClientSite;  
```  
  
## Remarks  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)   
 [CComPtr Class](../vs140/CComPtr-Class.md)   
 [IOleClientSite](http://msdn.microsoft.com/library/windows/desktop/ms693706)