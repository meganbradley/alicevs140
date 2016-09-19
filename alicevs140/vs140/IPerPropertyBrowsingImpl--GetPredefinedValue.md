---
title: "IPerPropertyBrowsingImpl::GetPredefinedValue"
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
ms.assetid: a6bded10-e919-4ba9-a54d-61e8637e73f7
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IPerPropertyBrowsingImpl::GetPredefinedValue
Retrieves a **VARIANT** containing the value of a property identified by a given DISPID. The DISPID is associated with the string name retrieved from `GetPredefinedStrings`.  
  
## Syntax  
  
```  
  
      STDMETHOD(GetPredefinedValue)(  
   DISPID dispID,  
   DWORD dwCookie,  
   VARIANT* pVarOut   
);  
```  
  
## Return Value  
 Returns **E_NOTIMPL**.  
  
## Remarks  
 ATL's implementation of [GetPredefinedStrings](../vs140/IPerPropertyBrowsingImpl--GetPredefinedStrings.md) retrieves no corresponding strings.  
  
 See [IPerPropertyBrowsing::GetPredefinedValue](http://msdn.microsoft.com/library/windows/desktop/ms690401) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IPerPropertyBrowsingImpl Class](../vs140/IPerPropertyBrowsingImpl-Class.md)