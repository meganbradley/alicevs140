---
title: "CListBox::InitStorage"
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
ms.assetid: be3a3faa-bf8e-45af-b609-92b9f0bbedec
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::InitStorage
Allocates memory for storing list-box items.  
  
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
 If successful, the maximum number of items that the list box can store before a memory reallocation is needed, otherwise **LB_ERRSPACE**, meaning not enough memory is available.  
  
## Remarks  
 Call this function before adding a large number of items to a `CListBox`.  
  
 This function helps speed up the initialization of list boxes that have a large number of items (more than 100). It preallocates the specified amount of memory so that subsequent [AddString](../vs140/CListBox--AddString.md), [InsertString](../vs140/CListBox--InsertString.md), and [Dir](../vs140/CListBox--Dir.md) functions take the shortest possible time. You can use estimates for the parameters. If you overestimate, some extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the preallocated amount.  
  
 Windows 95/98 only: The `nItems` parameter is limited to 16-bit values. This means list boxes cannot contain more than 32,767 items. Although the number of items is restricted, the total size of the items in a list box is limited only by available memory.  
  
## Example  
 [!CODE [NVC_MFC_CListBox#23](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#23)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::CListBox](../vs140/CListBox--CListBox.md)   
 [CListBox::Create](../vs140/CListBox--Create.md)   
 [CListBox::ResetContent](../vs140/CListBox--ResetContent.md)   
 [LB_INITSTORAGE](http://msdn.microsoft.com/library/windows/desktop/bb761319)