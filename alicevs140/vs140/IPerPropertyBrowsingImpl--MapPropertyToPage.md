---
title: "IPerPropertyBrowsingImpl::MapPropertyToPage"
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
ms.assetid: f89e403a-48ee-4edb-8baa-45a5a6c17f07
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IPerPropertyBrowsingImpl::MapPropertyToPage
Retrieves the CLSID of the property page associated with the specified property.  
  
## Syntax  
  
```  
  
      STDMETHOD(MapPropertyToPage)(  
   DISPID dispID,  
   CLSID* pClsid   
);  
```  
  
## Remarks  
 ATL uses the object's property map to obtain this information.  
  
 See [IPerPropertyBrowsing::MapPropertyToPage](http://msdn.microsoft.com/library/windows/desktop/ms694476) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IPerPropertyBrowsingImpl Class](../vs140/IPerPropertyBrowsingImpl-Class.md)   
 [BEGIN_PROP_MAP](../vs140/BEGIN_PROP_MAP.md)