---
title: "CListBox::GetTextLen"
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
ms.assetid: 6b4451bc-4acb-4523-9bee-c46e8979a304
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::GetTextLen
Gets the length of a string in a list-box item.  
  
## Syntax  
  
```  
  
      int GetTextLen(  
   int nIndex   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 Specifies the zero-based index of the string.  
  
## Return Value  
 The length of the string in characters, excluding the terminating null character. If `nIndex` does not specify a valid index, the return value is **LB_ERR**.  
  
## Example  
 See the example for [CListBox::GetText](../vs140/CListBox--GetText.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::GetText](../vs140/CListBox--GetText.md)   
 [LB_GETTEXTLEN](http://msdn.microsoft.com/library/windows/desktop/bb761315)