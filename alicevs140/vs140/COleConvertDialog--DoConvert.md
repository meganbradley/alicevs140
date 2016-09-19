---
title: "COleConvertDialog::DoConvert"
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
ms.assetid: ec720b1f-2fbe-4d94-8a50-3b5e1ec7e5e3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleConvertDialog::DoConvert
Call this function, after returning successfully from [DoModal](../vs140/COleConvertDialog--DoModal.md), either to convert or to activate an object of type [COleClientItem](../vs140/COleClientItem-Class.md).  
  
## Syntax  
  
```  
  
      BOOL DoConvert(  
  COleClientItem* pItem   
);  
```  
  
#### Parameters  
 `pItem`  
 Points to the item to be converted or activated. Cannot be **NULL**.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 The item is converted or activated according to the information selected by the user in the Convert dialog box.  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COleConvertDialog Class](../vs140/COleConvertDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [COleConvertDialog::DoModal](../vs140/COleConvertDialog--DoModal.md)   
 [COleConvertDialog::GetSelectionType](../vs140/COleConvertDialog--GetSelectionType.md)   
 [COleClientItem::ConvertTo](../vs140/COleClientItem--ConvertTo.md)   
 [COleClientItem::ActivateAs](../vs140/COleClientItem--ActivateAs.md)