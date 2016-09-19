---
title: "COleClientItem::ReactivateAndUndo"
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
ms.assetid: 4065c675-83d7-4d38-a320-809dd5a287a9
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::ReactivateAndUndo
Call this function to reactivate the OLE item and undo the last operation performed by the user during in-place editing.  
  
## Syntax  
  
```  
  
BOOL ReactivateAndUndo( );  
```  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 If your container application supports the undo command, call this function if the user chooses the undo command immediately after deactivating the OLE item.  
  
 If the server application is written with the Microsoft Foundation Class Libraries, this function causes the server to call [COleServerDoc::OnReactivateAndUndo](../vs140/COleServerDoc--OnReactivateAndUndo.md).  
  
 For more information, see [IOleInPlaceObject::ReactivateAndUndo](http://msdn.microsoft.com/library/windows/desktop/ms691372) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerDoc::OnReactivateAndUndo](../vs140/COleServerDoc--OnReactivateAndUndo.md)   
 [COleClientItem::OnDeactivateAndUndo](../vs140/COleClientItem--OnDeactivateAndUndo.md)