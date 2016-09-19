---
title: "COleClientItem::IsLinkUpToDate"
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
ms.assetid: 4db8de44-316b-416a-a5b7-42444dd36a37
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::IsLinkUpToDate
Call this function to see whether the OLE item is up to date.  
  
## Syntax  
  
```  
  
BOOL IsLinkUpToDate( ) const;  
```  
  
## Return Value  
 Nonzero if the OLE item is up to date; otherwise 0.  
  
## Remarks  
 A linked item can be out of date if its source document has been updated. An embedded item that contains links within it can similarly become out of date. The function does a recursive check of the OLE item. Note that determining whether an OLE item is out of date can be as expensive as actually performing an update.  
  
 This is called automatically by the [COleLinksDialog](../vs140/COleLinksDialog-Class.md) implementation.  
  
 For more information, see [IOleObject::IsUpToDate](http://msdn.microsoft.com/library/windows/desktop/ms686624) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)