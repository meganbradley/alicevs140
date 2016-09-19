---
title: "IOleControlImpl::FreezeEvents"
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
ms.assetid: cea12375-76e2-4aa1-8632-da2998bca60d
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleControlImpl::FreezeEvents
In ATL's implementation, `FreezeEvents` increments the control class's `m_nFreezeEvents` data member if `bFreeze` is **TRUE**, and decrements `m_nFreezeEvents` if `bFreeze` is **FALSE**.  
  
## Syntax  
  
```  
  
      HRESULT FreezeEvents(  
   BOOL bFreeze   
);  
```  
  
## Remarks  
 `FreezeEvents` then returns `S_OK`.  
  
 See [IOleControl::FreezeEvents](http://msdn.microsoft.com/library/windows/desktop/ms678482) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleControlImpl Class](../vs140/IOleControlImpl-Class.md)   
 [CComControlBase::m_nFreezeEvents](../vs140/CComControlBase--m_nFreezeEvents.md)