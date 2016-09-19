---
title: "IOleObjectImpl::SetClientSite"
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
ms.assetid: 2e0d20cb-6c68-44e5-94c2-3ffb0a083285
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleObjectImpl::SetClientSite
Tells the control about its client site in the container.  
  
## Syntax  
  
```  
  
      STDMETHOD(SetClientSite)(  
   IOleClientSite* pClientSite   
);  
```  
  
## Remarks  
 The method then returns `S_OK`.  
  
 See [IOleObject::SetClientSite](http://msdn.microsoft.com/library/windows/desktop/ms684013) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleObjectImpl Class](../vs140/IOleObjectImpl-Class.md)   
 [IOleObjectImpl::GetClientSite](../vs140/IOleObjectImpl--GetClientSite.md)