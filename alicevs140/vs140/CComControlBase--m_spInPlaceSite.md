---
title: "CComControlBase::m_spInPlaceSite"
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
ms.assetid: 1d2f194b-ad24-4216-914c-68d472c91943
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::m_spInPlaceSite
A pointer to the container's [IOleInPlaceSite](http://msdn.microsoft.com/library/windows/desktop/ms686586), [IOleInPlaceSiteEx](http://msdn.microsoft.com/library/windows/desktop/ms693461), or [IOleInPlaceSiteWindowless](http://msdn.microsoft.com/library/windows/desktop/ms682300) interface pointer.  
  
## Syntax  
  
```  
  
CComPtr<IOleInPlaceSiteWindowless> m_spInPlaceSite;  
```  
  
## Remarks  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
 The `m_spInPlaceSite` pointer is valid only if the [m_bNegotiatedWnd](../vs140/CComControlBase--m_bNegotiatedWnd.md) flag is **TRUE**.  
  
 The following table shows how the `m_spInPlaceSite` pointer type depends on the [m_bWndLess](../vs140/CComControlBase--m_bWndLess.md) and [m_bInPlaceSiteEx](../vs140/CComControlBase--m_bInPlaceSiteEx.md) data member flags:  
  
|m_spInPlaceSite Type|m_bWndLess Value|m_bInPlaceSiteEx Value|  
|---------------------------|-----------------------|-----------------------------|  
|**IOleInPlaceSiteWindowless**|**TRUE**|**TRUE** or **FALSE**|  
|**IOleInPlaceSiteEx**|**FALSE**|**TRUE**|  
|`IOleInPlaceSite`|**FALSE**|**FALSE**|  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)   
 [CComPtr Class](../vs140/CComPtr-Class.md)