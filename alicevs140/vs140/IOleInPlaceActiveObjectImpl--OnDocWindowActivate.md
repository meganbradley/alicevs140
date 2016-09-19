---
title: "IOleInPlaceActiveObjectImpl::OnDocWindowActivate"
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
ms.assetid: 61f9be5a-9caa-4c58-8e8e-971069c6848c
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleInPlaceActiveObjectImpl::OnDocWindowActivate
Notifies the control when the container's document window is activated or deactivated.  
  
## Syntax  
  
```  
  
      HRESULT OnDocWindowActivate(  
   BOOL fActivate   
);  
```  
  
## Return Value  
 Returns `S_OK`.  
  
## Remarks  
 See [IOleInPlaceActiveObject::OnDocWindowActivate](http://msdn.microsoft.com/library/windows/desktop/ms687281) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleInPlaceActiveObjectImpl Class](../vs140/IOleInPlaceActiveObjectImpl-Class.md)