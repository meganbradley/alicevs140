---
title: "IPointerInactiveImpl::OnInactiveMouseMove"
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
ms.assetid: e74fec6a-8f96-41d7-9d27-5fc79f5134b9
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IPointerInactiveImpl::OnInactiveMouseMove
Notifies the object that the mouse pointer has moved over it, indicating the object can fire mouse events.  
  
## Syntax  
  
```  
  
      HRESULT OnInactiveMouseMove(  
   LPCRECT pRectBounds,  
   long x,  
   long y,  
   DWORD dwMouseMsg   
);  
```  
  
## Return Value  
 Returns **E_NOTIMPL**.  
  
## Remarks  
 See [IPointerInactive::OnInactiveMouseMove](http://msdn.microsoft.com/library/windows/desktop/ms693374) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IPointerInactiveImpl Class](../vs140/IPointerInactiveImpl-Class.md)