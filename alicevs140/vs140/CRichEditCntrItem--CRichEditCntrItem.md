---
title: "CRichEditCntrItem::CRichEditCntrItem"
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
ms.assetid: 2e9d139e-2c34-475d-acb7-8beed6885ece
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCntrItem::CRichEditCntrItem
Call this function to create a `CRichEditCntrItem` object and add it to the container document.  
  
## Syntax  
  
```  
  
      CRichEditCntrItem(  
   REOBJECT* preo = NULL,  
   CRichEditDoc* pContainer = NULL   
);  
```  
  
#### Parameters  
 *preo*  
 Pointer to an [REOBJECT](http://msdn.microsoft.com/library/windows/desktop/bb787946) structure which describes an OLE item. The new `CRichEditCntrItem` object is constructed around this OLE item. If *preo* is **NULL**, the client item is empty.  
  
 `pContainer`  
 Pointer to the container document that will contain this item. If `pContainer` is **NULL**, you must explicitly call [COleDocument::AddItem](../vs140/COleDocument--AddItem.md) to add this client item to a document.  
  
## Remarks  
 This function does not perform any OLE initialization.  
  
 For more information, see the [REOBJECT](http://msdn.microsoft.com/library/windows/desktop/bb787946) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditCntrItem Class](../vs140/CRichEditCntrItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDocument::AddItem](../vs140/COleDocument--AddItem.md)   
 [CRichEditDoc Class](../vs140/CRichEditDoc-Class.md)