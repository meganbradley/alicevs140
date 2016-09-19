---
title: "COleServerDoc::OnShowControlBars"
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
ms.assetid: 26f4faad-d134-4a86-8527-3d997f2807c8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerDoc::OnShowControlBars
The framework calls this function to show or hide the server application's control bars associated with the frame window identified by `pFrameWnd`.  
  
## Syntax  
  
```  
  
      virtual void OnShowControlBars(  
   CFrameWnd *pFrameWnd,  
   BOOL bShow   
);  
```  
  
#### Parameters  
 `pFrameWnd`  
 Pointer to the frame window whose control bars should be hidden or shown.  
  
 `bShow`  
 Determines whether control bars are shown or hidden.  
  
## Remarks  
 The default implementation enumerates all control bars owned by that frame window and hides or shows them.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerDoc Class](../vs140/COleServerDoc-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerDoc::ActivateInPlace](../vs140/COleServerDoc--ActivateInPlace.md)   
 [COleServerDoc::OnReactivateAndUndo](../vs140/COleServerDoc--OnReactivateAndUndo.md)   
 [COleServerDoc::OnFrameWindowActivate](../vs140/COleServerDoc--OnFrameWindowActivate.md)   
 [COleServerDoc::IsInPlaceActive](../vs140/COleServerDoc--IsInPlaceActive.md)