---
title: "COleClientItem::OnDeactivateAndUndo"
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
ms.assetid: 5063d392-9211-492e-ac1e-1b8a525bdd45
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::OnDeactivateAndUndo
Called by the framework when the user invokes the undo command after activating the OLE item in place.  
  
## Syntax  
  
```  
  
virtual void OnDeactivateAndUndo( );  
```  
  
## Remarks  
 The default implementation calls [DeactivateUI](../vs140/COleClientItem--DeactivateUI.md) to deactivate the server's user interface. Override this function if you are implementing the undo command in your container application. In your override, call the base class version of the function and then undo the last command executed in your application.  
  
 For more information, see [IOleInPlaceSite::DeactivateAndUndo](http://msdn.microsoft.com/library/windows/desktop/ms683743) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::DeactivateUI](../vs140/COleClientItem--DeactivateUI.md)