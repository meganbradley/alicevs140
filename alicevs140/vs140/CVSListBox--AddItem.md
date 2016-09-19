---
title: "CVSListBox::AddItem"
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
ms.assetid: 2a8ccaeb-9675-4950-8c4e-828c947de0cc
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CVSListBox::AddItem
Adds a string to a list control.  
  
## Syntax  
  
```  
virtual int AddItem(  
   const CString& strIext,  
   DWORD_PTR dwData=0,  
   int iIndex=-1   
);  
```  
  
#### Parameters  
 [in] `strIext`  
 A reference to a string.  
  
 [in] `dwData`  
 An application-specific 32-bit value that is associated with the string. The default value is 0.  
  
 [in] `iIndex`  
 The zero-based index of the position that will hold the string. If the `iIndex` parameter is -1, the string is added to the end of the list. The default value is -1.  
  
## Return Value  
 The zero-based index of the position of the string in the list control.  
  
## Remarks  
 Use the [CVSListBox::GetItemData](../vs140/CVSListBox--GetItemData.md) method to retrieve the value that is specified by the `dwData` parameter. This value can be an application-specific integer or a pointer to other data.  
  
## Requirements  
 **Header:** afxvslistbox.h  
  
## See Also  
 [CVSListBox Class](../vs140/CVSListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CVSListBox::GetItemData](../vs140/CVSListBox--GetItemData.md)