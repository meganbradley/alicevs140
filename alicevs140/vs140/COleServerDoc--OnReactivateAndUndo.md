---
title: "COleServerDoc::OnReactivateAndUndo"
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
ms.assetid: edd82065-f220-41b2-8c16-9b73271d24d7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerDoc::OnReactivateAndUndo
The framework calls this function when the user chooses to undo changes made to an item that has been activated in place, changed, and subsequently deactivated.  
  
## Syntax  
  
```  
  
virtual BOOL OnReactivateAndUndo( );  
```  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 The default implementation does nothing except return **FALSE** to indicate failure.  
  
 Override this function if your application supports undo. Usually you would perform the undo operation, then activate the item by calling `ActivateInPlace`. If the container application is written with the Microsoft Foundation Class Library, calling `COleClientItem::ReactivateAndUndo` causes this function to be called.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerDoc Class](../vs140/COleServerDoc-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerDoc::ActivateInPlace](../vs140/COleServerDoc--ActivateInPlace.md)   
 [COleServerDoc::IsInPlaceActive](../vs140/COleServerDoc--IsInPlaceActive.md)   
 [COleClientItem::ReactivateAndUndo](../vs140/COleClientItem--ReactivateAndUndo.md)