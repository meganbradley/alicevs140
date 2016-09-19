---
title: "IObjectWithSiteImpl::m_spUnkSite"
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
ms.assetid: 0e779dea-8121-4d44-bafa-b6cd35157e22
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IObjectWithSiteImpl::m_spUnkSite
Manages the site's **IUnknown** pointer.  
  
## Syntax  
  
```  
  
CComPtr< IUnknown > m_spUnkSite;  
  
```  
  
## Remarks  
 `m_spUnkSite` initially receives this pointer through a call to [SetSite](../vs140/IObjectWithSiteImpl--SetSite.md).  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [IObjectWithSiteImpl Class](../vs140/IObjectWithSiteImpl-Class.md)   
 [CComPtr Class](../vs140/CComPtr-Class.md)