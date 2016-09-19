---
title: "IOleInPlaceActiveObjectImpl::ResizeBorder"
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
ms.assetid: f45fc24e-23d1-4ea6-927a-8b40c8af7aac
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleInPlaceActiveObjectImpl::ResizeBorder
Informs the control it needs to resize its borders.  
  
## Syntax  
  
```  
  
      HRESULT ResizeBorder(  
   LPRECT prcBorder,  
   IOleInPlaceUIWindow* pUIWindow,  
   BOOL fFrameWindow   
);  
```  
  
## Return Value  
 Returns `S_OK`.  
  
## Remarks  
 See [IOleInPlaceActiveObject::ResizeBorder](http://msdn.microsoft.com/library/windows/desktop/ms680053) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleInPlaceActiveObjectImpl Class](../vs140/IOleInPlaceActiveObjectImpl-Class.md)