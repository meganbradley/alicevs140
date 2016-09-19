---
title: "COleClientItem::OnDiscardUndoState"
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
ms.assetid: 1e1bec8d-d645-4de2-bb9e-c0dfa6e29db9
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::OnDiscardUndoState
Called by the framework when the user performs an action that discards the undo state while editing the OLE item.  
  
## Syntax  
  
```  
  
virtual void OnDiscardUndoState();  
```  
  
## Remarks  
 The default implementation does nothing. Override this function if you are implementing the undo command in your container application. In your override, discard the container application's undo state.  
  
 If the server was written with the Microsoft Foundation Class Library, the server can cause this function to be called by calling [COleServerDoc::DiscardUndoState](../vs140/COleServerDoc--DiscardUndoState.md).  
  
 For more information, see [IOleInPlaceSite::DiscardUndoState](http://msdn.microsoft.com/library/windows/desktop/ms688642) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerDoc::DiscardUndoState](../vs140/COleServerDoc--DiscardUndoState.md)