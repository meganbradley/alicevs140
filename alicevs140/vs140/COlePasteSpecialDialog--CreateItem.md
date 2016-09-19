---
title: "COlePasteSpecialDialog::CreateItem"
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
ms.assetid: 317f63e1-5168-4bfc-a38d-a85573f44998
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COlePasteSpecialDialog::CreateItem
Creates the new item that was chosen in the Paste Special dialog box.  
  
## Syntax  
  
```  
  
      BOOL CreateItem(  
   COleClientItem* pNewItem   
);  
```  
  
#### Parameters  
 *pNewItem*  
 Points to a `COleClientItem` instance. Cannot be **NULL**.  
  
## Return Value  
 Nonzero if the item was created successfully; otherwise 0.  
  
## Remarks  
 This function should only be called after [DoModal](../vs140/COlePasteSpecialDialog--DoModal.md) returns **IDOK**.  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COlePasteSpecialDialog Class](../vs140/COlePasteSpecialDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [COlePasteSpecialDialog::DoModal](../vs140/COlePasteSpecialDialog--DoModal.md)   
 [COlePasteSpecialDialog::GetSelectionType](../vs140/COlePasteSpecialDialog--GetSelectionType.md)   
 [COlePasteSpecialDialog::COlePasteSpecialDialog](../vs140/COlePasteSpecialDialog--COlePasteSpecialDialog.md)