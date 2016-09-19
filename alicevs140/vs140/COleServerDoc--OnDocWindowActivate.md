---
title: "COleServerDoc::OnDocWindowActivate"
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
ms.assetid: 2ae5a5c4-b1d8-4eba-9e0a-afbebcb9e0cd
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerDoc::OnDocWindowActivate
The framework calls this function to activate or deactivate a document window for in-place editing.  
  
## Syntax  
  
```  
  
      virtual void OnDocWindowActivate(  
   BOOL bActivate   
);  
```  
  
#### Parameters  
 `bActivate`  
 Specifies whether the document window is to be activated or deactivated.  
  
## Remarks  
 The default implementation removes or adds the frame-level user interface elements as appropriate. Override this function if you want to perform additional actions when the document containing your item is activated or deactivated.  
  
 For more information, see the article [Activation](../vs140/Activation--C---.md)..  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerDoc Class](../vs140/COleServerDoc-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerDoc::ActivateInPlace](../vs140/COleServerDoc--ActivateInPlace.md)   
 [COleServerDoc::OnReactivateAndUndo](../vs140/COleServerDoc--OnReactivateAndUndo.md)   
 [COleServerDoc::OnShowControlBars](../vs140/COleServerDoc--OnShowControlBars.md)   
 [COleServerDoc::OnDeactivateUI](../vs140/COleServerDoc--OnDeactivateUI.md)   
 [COleServerDoc::OnFrameWindowActivate](../vs140/COleServerDoc--OnFrameWindowActivate.md)   
 [COleIPFrameWnd Class](../vs140/COleIPFrameWnd-Class.md)