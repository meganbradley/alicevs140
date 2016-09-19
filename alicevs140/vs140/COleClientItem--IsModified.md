---
title: "COleClientItem::IsModified"
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
ms.assetid: 603ba16b-988f-4992-8a8e-05462f7ebb39
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::IsModified
Call this function to see whether the OLE item is dirty (modified since it was last saved).  
  
## Syntax  
  
```  
  
BOOL IsModified( ) const;  
```  
  
## Return Value  
 Nonzero if the OLE item is dirty; otherwise 0.  
  
## Remarks  
 For more information, see [IPersistStorage::IsDirty](http://msdn.microsoft.com/library/windows/desktop/ms683910) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)