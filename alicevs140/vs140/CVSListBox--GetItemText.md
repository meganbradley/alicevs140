---
title: "CVSListBox::GetItemText"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 059315a6-5cc2-44a6-bd7a-b40ea4a960fa
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CVSListBox::GetItemText
Retrieves the text of an editable list control item.  
  
## Syntax  
  
```  
virtual CString GetItemText(  
   int iIndex   
) const;  
```  
  
#### Parameters  
 [in] `iIndex`  
 The zero-based index of an editable list control item.  
  
## Return Value  
 A [CString](../vs140/CStringT-Class.md) object that contains the text of the specified item.  
  
## Remarks  
  
## Requirements  
 **Header:** afxvslistbox.h  
  
## See Also  
 [CVSListBox Class](../vs140/CVSListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)