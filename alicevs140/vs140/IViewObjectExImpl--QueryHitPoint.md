---
title: "IViewObjectExImpl::QueryHitPoint"
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
ms.assetid: 27d7911c-99bb-437e-a87c-36f2e698fa3b
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IViewObjectExImpl::QueryHitPoint
Checks if the specified point is in the specified rectangle and returns a [HITRESULT](http://msdn.microsoft.com/library/windows/desktop/ms682187) value in `pHitResult`.  
  
## Syntax  
  
```  
  
      STDMETHOD(QueryHitPoint)(  
   DWORD dwAspect,  
   LPCRECT pRectBounds,  
   POINT ptlLoc,  
   LONG /* lCloseHit */,  
   DWORD* /* pHitResult */   
);  
```  
  
## Remarks  
 The value can be either **HITRESULT_HIT** or **HITRESULT_OUTSIDE**.  
  
 If `dwAspect` equals [DVASPECT_CONTENT](http://msdn.microsoft.com/library/windows/desktop/ms690318), the method returns `S_OK`. Otherwise, the method returns **E_FAIL**.  
  
 See [IViewObjectEx::QueryHitPoint](http://msdn.microsoft.com/library/windows/desktop/ms691209) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IViewObjectExImpl Class](../vs140/IViewObjectExImpl-Class.md)   
 [IViewObjectExImpl::QueryHitRect](../vs140/IViewObjectExImpl--QueryHitRect.md)