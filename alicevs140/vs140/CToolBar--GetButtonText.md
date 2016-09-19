---
title: "CToolBar::GetButtonText"
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
ms.assetid: d6526674-0ee4-4e24-8321-daff3c023480
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBar::GetButtonText
Call this member function to retrieve the text that appears on a button.  
  
## Syntax  
  
```  
  
      CString GetButtonText(  
   int nIndex   
) const;  
void GetButtonText(  
   int nIndex,  
   CString& rString   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 Index of the text to be retrieved.  
  
 `rString`  
 A reference to a [CString](../vs140/CStringT-Class.md) object that will contain the text to be retrieved.  
  
## Return Value  
 A `CString` object containing the button text.  
  
## Remarks  
 The second form of this member function fills a `CString` object with the string text.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CToolBar Class](../vs140/CToolBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBar::SetButtonText](../vs140/CToolBar--SetButtonText.md)