---
title: "CComboBox::GetItemDataPtr"
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
ms.assetid: 9ea5b5f5-435b-475f-8fbe-e7cb971ceb8a
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::GetItemDataPtr
Retrieves the application-supplied 32-bit value associated with the specified combo-box item as a pointer (**void\***).  
  
## Syntax  
  
```  
  
      void* GetItemDataPtr(  
   int nIndex   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 Contains the zero-based index of an item in the combo box's list box.  
  
## Return Value  
 Retrieves a pointer, or –1 if an error occurs.  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#22](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#22)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::SetItemDataPtr](../vs140/CComboBox--SetItemDataPtr.md)   
 [CComboBox::GetItemData](../vs140/CComboBox--GetItemData.md)   
 [CComboBox::SetItemData](../vs140/CComboBox--SetItemData.md)   
 [CB_GETITEMDATA](http://msdn.microsoft.com/library/windows/desktop/bb775859)