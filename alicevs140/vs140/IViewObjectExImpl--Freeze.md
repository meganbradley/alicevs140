---
title: "IViewObjectExImpl::Freeze"
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
ms.assetid: 3d6565a7-c23c-43eb-b0cc-af747afc1c19
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IViewObjectExImpl::Freeze
Freezes the drawn representation of a control so it won't change until an `Unfreeze`. The ATL implementation returns **E_NOTIMPL**.  
  
## Syntax  
  
```  
  
      STDMETHOD(Freeze)(  
   DWORD /* dwAspect */,  
   LONG /* lindex */,  
   void* /* pvAspect */,  
   DWORD* /* pdwFreeze */  
);  
```  
  
## Remarks  
 See [IViewObject::Freeze](http://msdn.microsoft.com/library/windows/desktop/ms688728) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IViewObjectExImpl Class](../vs140/IViewObjectExImpl-Class.md)