---
title: "IPointerInactiveImpl::OnInactiveSetCursor"
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
ms.assetid: f45cdd4f-ed6f-41ef-932c-6af322f99aa8
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IPointerInactiveImpl::OnInactiveSetCursor
Sets the mouse pointer for the inactive object.  
  
## Syntax  
  
```  
  
      HRESULT OnInactiveSetCursor(  
   LPCRECT pRectBounds,  
   long x,  
   long y,  
   DWORD dwMouseMsg,  
   BOOL fSetAlways  
);  
```  
  
## Return Value  
 Returns **E_NOTIMPL**.  
  
## Remarks  
 See [IPointerInactive::OnInactiveSetCursor](http://msdn.microsoft.com/library/windows/desktop/ms694336) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IPointerInactiveImpl Class](../vs140/IPointerInactiveImpl-Class.md)