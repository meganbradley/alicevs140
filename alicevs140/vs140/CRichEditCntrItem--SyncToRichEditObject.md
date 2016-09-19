---
title: "CRichEditCntrItem::SyncToRichEditObject"
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
ms.assetid: a385a21b-8112-4dcc-8070-69244723a58a
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCntrItem::SyncToRichEditObject
Call this function to synchronize the device aspect, [DVASPECT](http://msdn.microsoft.com/library/windows/desktop/ms690318), of this **CRichEditCntrltem** to that specified by *reo*.  
  
## Syntax  
  
```  
  
      void SyncToRichEditObject(  
   REOBJECT& reo   
);  
```  
  
#### Parameters  
 *reo*  
 Reference to an [REOBJECT](http://msdn.microsoft.com/library/windows/desktop/bb787946) structure which describes an OLE item.  
  
## Remarks  
 For more information, see [DVASPECT](http://msdn.microsoft.com/library/windows/desktop/ms690318) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditCntrItem Class](../vs140/CRichEditCntrItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)