---
title: "COleServerDoc::DestroyInPlaceFrame"
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
ms.assetid: e7657994-64d9-460c-b333-8ec958b9e5ed
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerDoc::DestroyInPlaceFrame
The framework calls this function to destroy an in-place frame window and return the server application's document window to its state before in-place activation.  
  
## Syntax  
  
```  
  
      virtual void DestroyInPlaceFrame(   
   COleIPFrameWnd* pFrameWnd    
);  
```  
  
#### Parameters  
 `pFrameWnd`  
 Pointer to the in-place frame window to be destroyed.  
  
## Remarks  
 This is an advanced overridable.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerDoc Class](../vs140/COleServerDoc-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerDoc::CreateInPlaceFrame](../vs140/COleServerDoc--CreateInPlaceFrame.md)