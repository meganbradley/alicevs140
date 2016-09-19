---
title: "COleClientItem::UpdateLink"
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
ms.assetid: 3f707f4e-82b3-4e83-901d-53c6f9c1b3ce
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::UpdateLink
Call this function to update the presentation data of the OLE item immediately.  
  
## Syntax  
  
```  
  
BOOL UpdateLink( );  
```  
  
## Return Value  
 Nonzero on success; otherwise 0.  
  
## Remarks  
 For linked items, the function finds the link source to obtain a new presentation for the OLE item. This process may involve running one or more server applications, which could be time-consuming. For embedded items, the function operates recursively, checking whether the embedded item contains links that might be out of date and updating them. The user can also manually update individual links using the Links dialog box.  
  
 For more information, see [IOleLink::Update](http://msdn.microsoft.com/library/windows/desktop/ms692660) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleLinksDialog Class](../vs140/COleLinksDialog-Class.md)