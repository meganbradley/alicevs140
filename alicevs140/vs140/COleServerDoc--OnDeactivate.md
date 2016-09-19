---
title: "COleServerDoc::OnDeactivate"
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
ms.assetid: 1b0dce0d-32dc-4b6a-9e71-ffb0853f86f6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerDoc::OnDeactivate
Called by the framework when the user deactivates an embedded or linked item that is currently in-place active.  
  
## Syntax  
  
```  
  
virtual void OnDeactivate( );  
```  
  
## Remarks  
 This function restores the container application's user interface to its original state and destroys any menus and other controls that were created for in-place activation.  
  
 The undo state information should be unconditionally released at this point.  
  
 For more information, see the article [Activation](../vs140/Activation--C---.md)..  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerDoc Class](../vs140/COleServerDoc-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerDoc::ActivateInPlace](../vs140/COleServerDoc--ActivateInPlace.md)   
 [COleServerDoc::OnDeactivateUI](../vs140/COleServerDoc--OnDeactivateUI.md)   
 [COleServerDoc::DestroyInPlaceFrame](../vs140/COleServerDoc--DestroyInPlaceFrame.md)