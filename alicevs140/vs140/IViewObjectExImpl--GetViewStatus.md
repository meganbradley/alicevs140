---
title: "IViewObjectExImpl::GetViewStatus"
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
ms.assetid: 992ab6af-e865-45ae-b5bb-2b77ccc46642
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IViewObjectExImpl::GetViewStatus
Returns information about the opacity of the object and what drawing aspects are supported.  
  
## Syntax  
  
```  
  
      STDMETHOD(GetViewStatus)(  
   DWORD* pdwStatus   
);  
```  
  
## Remarks  
 By default, ATL sets `pdwStatus` to indicate that the control supports **VIEWSTATUS_OPAQUE** (possible values are in the [VIEWSTATUS](http://msdn.microsoft.com/library/windows/desktop/ms687201) enumeration).  
  
 See [IViewObjectEx::GetViewStatus](http://msdn.microsoft.com/library/windows/desktop/ms693371) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IViewObjectExImpl Class](../vs140/IViewObjectExImpl-Class.md)