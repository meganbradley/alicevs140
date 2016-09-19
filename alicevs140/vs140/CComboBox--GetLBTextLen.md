---
title: "CComboBox::GetLBTextLen"
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
ms.assetid: c1a75548-907a-4e43-a179-85cd08e94c0c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::GetLBTextLen
Gets the length of a string in the list box of a combo box.  
  
## Syntax  
  
```  
  
      int GetLBTextLen(  
   int nIndex   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 Contains the zero-based index of the list-box string.  
  
## Return Value  
 The length of the string in bytes, excluding the terminating null character. If `nIndex` does not specify a valid index, the return value is **CB_ERR**.  
  
## Example  
 See the example for [CComboBox::GetLBText](../vs140/CComboBox--GetLBText.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::GetLBText](../vs140/CComboBox--GetLBText.md)   
 [CB_GETLBTEXTLEN](http://msdn.microsoft.com/library/windows/desktop/bb775864)