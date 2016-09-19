---
title: "CRichEditView::InsertItem"
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
ms.assetid: 1399ad83-f42d-480a-92e9-6b3b342a8339
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::InsertItem
Call this function to insert a [CRichEditCntrItem](../vs140/CRichEditCntrItem-Class.md) object into a rich edit view.  
  
## Syntax  
  
```  
  
      HRESULT InsertItem(  
   CRichEditCntrItem* pItem   
);  
```  
  
#### Parameters  
 `pItem`  
 Pointer to the item to be inserted.  
  
## Return Value  
 An `HRESULT` value indicating the success of the insertion.  
  
## Remarks  
 For more information on `HRESULT`, see [Structure of COM Error Codes](http://msdn.microsoft.com/library/windows/desktop/ms690088) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditView::InsertFileAsObject](../vs140/CRichEditView--InsertFileAsObject.md)   
 [CRichEditCntrItem Class](../vs140/CRichEditCntrItem-Class.md)