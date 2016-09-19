---
title: "IOleInPlaceActiveObjectImpl::OnFrameWindowActivate"
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
ms.assetid: 35b26159-9c7d-4de7-89a0-4c2331ad1863
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleInPlaceActiveObjectImpl::OnFrameWindowActivate
Notifies the control when the container's top-level frame window is activated or deactivated.  
  
## Syntax  
  
```  
  
      HRESULT OnFrameWindowActivate(  
   BOOL fActivate   
);  
```  
  
## Return Value  
 Returns `S_OK`.  
  
## Remarks  
 See [IOleInPlaceActiveObject::OnFrameWindowActivate](http://msdn.microsoft.com/library/windows/desktop/ms683969) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleInPlaceActiveObjectImpl Class](../vs140/IOleInPlaceActiveObjectImpl-Class.md)