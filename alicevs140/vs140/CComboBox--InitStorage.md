---
title: "CComboBox::InitStorage"
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
ms.assetid: 3f1300af-14c5-415a-9c82-bfa6a7f452ad
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::InitStorage
Allocates memory for storing list box items in the list-box portion of the combo box.  
  
## Syntax  
  
```  
  
      int InitStorage(  
   int nItems,  
   UINT nBytes   
);  
```  
  
#### Parameters  
 `nItems`  
 Specifies the number of items to add.  
  
 `nBytes`  
 Specifies the amount of memory, in bytes, to allocate for item strings.  
  
## Return Value  
 If successful, the maximum number of items that the list-box portion of the combo box can store before a memory reallocation is needed, otherwise **CB_ERRSPACE**, meaning not enough memory is available.  
  
## Remarks  
 Call this function before adding a large number of items to the list-box portion of the `CComboBox`.  
  
 Windows 95/98 only: The `wParam` parameter is limited to 16-bit values. This means list boxes cannot contain more than 32,767 items. Although the number of items is restricted, the total size of the items in a list box is limited only by available memory.  
  
 This function helps speed up the initialization of list boxes that have a large number of items (more than 100). It preallocates the specified amount of memory so that subsequent [AddString](../vs140/CComboBox--AddString.md), [InsertString](../vs140/CComboBox--InsertString.md), and [Dir](../vs140/CComboBox--Dir.md) functions take the shortest possible time. You can use estimates for the parameters. If you overestimate, some extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the preallocated amount.  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#26](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#26)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::CComboBox](../vs140/CComboBox--CComboBox.md)   
 [CComboBox::Create](../vs140/CComboBox--Create.md)   
 [CComboBox::ResetContent](../vs140/CComboBox--ResetContent.md)   
 [CB_INITSTORAGE](http://msdn.microsoft.com/library/windows/desktop/bb775872)