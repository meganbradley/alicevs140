---
title: "IViewObjectExImpl::GetRect"
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
ms.assetid: 5cbb965e-ead7-4476-8660-85d2804f06fc
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IViewObjectExImpl::GetRect
Returns a rectangle describing a requested drawing aspect. The ATL implementation returns **E_NOTIMPL**.  
  
## Syntax  
  
```  
  
      STDMETHOD(GetRect)(  
   DWORD /* dwAspect */,  
   LPRECTL /* pRect */  
);  
```  
  
## Remarks  
 See [IViewObjectEx::GetRect](http://msdn.microsoft.com/library/windows/desktop/ms695246) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IViewObjectExImpl Class](../vs140/IViewObjectExImpl-Class.md)