---
title: "IPerPropertyBrowsingImpl::GetPredefinedStrings"
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
ms.assetid: dd483ada-d52e-4e6e-b74d-8925e093960d
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IPerPropertyBrowsingImpl::GetPredefinedStrings
Fills each array with zero items.  
  
## Syntax  
  
```  
  
      STDMETHOD(GetPredefinedStrings)(  
   DISPID dispID,  
   CALPOLESTR* pCaStringsOut,  
   CADWORD* pCaCookiesOut   
);  
```  
  
## Return Value  
 ATL's implementation of [GetPredefinedValue](../vs140/IPerPropertyBrowsingImpl--GetPredefinedValue.md) returns **E_NOTIMPL**.  
  
## Remarks  
 See [IPerPropertyBrowsing::GetPredefinedStrings](http://msdn.microsoft.com/library/windows/desktop/ms679724) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IPerPropertyBrowsingImpl Class](../vs140/IPerPropertyBrowsingImpl-Class.md)   
 [CADWORD](http://msdn.microsoft.com/library/windows/desktop/ms682383)   
 [CALPOLESTR](http://msdn.microsoft.com/library/windows/desktop/ms686617)