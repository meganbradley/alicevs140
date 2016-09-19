---
title: "IObjectWithSiteImpl::GetSite"
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
ms.assetid: c9c50b41-22b0-4f54-8cab-36dc8cca5824
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IObjectWithSiteImpl::GetSite
Queries the site for a pointer to the interface identified by `riid`.  
  
## Syntax  
  
```  
  
      STDMETHOD(GetSite)(  
   REFIID riid,  
   void **ppvSite   
);  
```  
  
## Remarks  
 If the site supports this interface, the pointer is returned via `ppvSite`. Otherwise, `ppvSite` is set to **NULL**.  
  
 See [IObjectWithSite::GetSite](http://msdn.microsoft.com/library/windows/desktop/ms694452) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [IObjectWithSiteImpl Class](../vs140/IObjectWithSiteImpl-Class.md)   
 [IObjectWithSiteImpl::SetSite](../vs140/IObjectWithSiteImpl--SetSite.md)