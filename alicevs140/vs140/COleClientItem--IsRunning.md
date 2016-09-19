---
title: "COleClientItem::IsRunning"
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
ms.assetid: 802fe2af-50ee-4b77-86f1-e9e76c70c88c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::IsRunning
Call this function to see whether the OLE item is running; that is, whether the item is loaded and running in the server application.  
  
## Syntax  
  
```  
  
BOOL IsRunning( ) const;  
```  
  
## Return Value  
 Nonzero if the OLE item is running; otherwise 0.  
  
## Remarks  
 For more information, see [OleIsRunning](http://msdn.microsoft.com/library/windows/desktop/ms688705) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)