---
title: "IObjectWithSiteImpl::SetChildSite"
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
ms.assetid: afe679b4-978a-4cd3-bb91-08bef7218bf4
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IObjectWithSiteImpl::SetChildSite
Provides the object with the site's **IUnknown** pointer.  
  
## Syntax  
  
```  
  
      HRESULT SetChildSite(  
   IUnknown* pUnkSite   
);  
```  
  
#### Parameters  
 *pUnkSite*  
 [in] Pointer to the **IUnknown** interface pointer of the site managing this object. If NULL, the object should call `IUnknown::Release` on any existing site at which point the object no longer knows its site.  
  
## Return Value  
 Returns `S_OK`.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [IObjectWithSiteImpl Class](../vs140/IObjectWithSiteImpl-Class.md)   
 [IObjectWithSiteImpl::GetSite](../vs140/IObjectWithSiteImpl--GetSite.md)