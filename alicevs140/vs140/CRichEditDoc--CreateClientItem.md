---
title: "CRichEditDoc::CreateClientItem"
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
ms.assetid: cb7f8109-a294-4a19-af71-355192544a8f
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditDoc::CreateClientItem
Call this function to create a `CRichEditCntrItem` object and add it to this document.  
  
## Syntax  
  
```  
  
      virtual CRichEditCntrItem* CreateClientItem(  
   REOBJECT* preo = NULL   
) const = 0;  
```  
  
#### Parameters  
 *preo*  
 Pointer to an [REOBJECT](http://msdn.microsoft.com/library/windows/desktop/bb787946) structure which describes an OLE item. The new `CRichEditCntrItem` object is constructed around this OLE item. If *preo* is **NULL**, the new client item is empty.  
  
## Return Value  
 Pointer to a new [CRichEditCntrItem](../vs140/CRichEditCntrItem-Class.md) object which has been added to this document.  
  
## Remarks  
 This function does not perform any OLE initialization.  
  
 For more information, see the [REOBJECT](http://msdn.microsoft.com/library/windows/desktop/bb787946) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditDoc Class](../vs140/CRichEditDoc-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCntrItem::CRichEditCntrItem](../vs140/CRichEditCntrItem--CRichEditCntrItem.md)   
 [COleDocument::AddItem](../vs140/COleDocument--AddItem.md)