---
title: "IOleInPlaceObjectWindowlessImpl::OnWindowMessage"
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
ms.assetid: 400b2b20-51f0-414c-a436-031431887c68
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleInPlaceObjectWindowlessImpl::OnWindowMessage
Dispatches a message from a container to a windowless control that is in-place active.  
  
## Syntax  
  
```  
  
      HRESULT OnWindowMessage(  
   UINT msg,  
   WPARAM WParam,  
   LPARAM LParam,  
   LRESULT plResultParam   
);  
```  
  
## Remarks  
 See [IOleInPlaceObjectWindowless::OnWindowMessage](http://msdn.microsoft.com/library/windows/desktop/ms693783) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleInPlaceObjectWindowlessImpl Class](../vs140/IOleInPlaceObjectWindowlessImpl-Class.md)