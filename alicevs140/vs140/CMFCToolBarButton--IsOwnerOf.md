---
title: "CMFCToolBarButton::IsOwnerOf"
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
ms.assetid: 08164f59-d9b3-4ed5-85b8-6cf42f8d4059
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::IsOwnerOf
Determines whether the button is the owner of the provided window handle.  
  
## Syntax  
  
```  
virtual BOOL IsOwnerOf(  
   HWND hwnd  
);  
```  
  
#### Parameters  
 [in] `hwnd`  
 A window handle.  
  
## Return Value  
 Nonzero if the button is the owner of the provided window handle; otherwise 0.  
  
## Remarks  
 This method returns nonzero if `hwnd` either refers to the direct window handle or is a child of the window handle that is associated with the button. This method returns 0 if `hwnd` is `NULL`.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)