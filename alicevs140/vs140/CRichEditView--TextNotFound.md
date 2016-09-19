---
title: "CRichEditView::TextNotFound"
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
ms.assetid: 89a3ec32-f7a2-4c22-b395-dae62b8f15af
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::TextNotFound
Call this function to reset the internal search state of the [CRichEditView](../vs140/CRichEditView-Class.md) control after a failed call to [FindText](../vs140/CRichEditView--FindText.md).  
  
## Syntax  
  
```  
  
      void TextNotFound(  
   LPCTSTR lpszFind  
);  
```  
  
#### Parameters  
 `lpszFind`  
 Contains the text string that was not found.  
  
## Remarks  
 It is recommended that this method be called immediately after failed calls to [FindText](../vs140/CRichEditView--FindText.md) so that the internal search state of the control is properly reset.  
  
 The `lpszFind` parameter should include the same content as the string provided to [FindText](../vs140/CRichEditView--FindText.md). After resetting the internal search state, this method will call the [OnTextNotFound](../vs140/CRichEditView--OnTextNotFound.md) method with the provided search string.  
  
## Example  
 See the example for [CRichEditView::FindText](../vs140/CRichEditView--FindText.md).  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditView::FindText](../vs140/CRichEditView--FindText.md)   
 [CRichEditView::OnTextNotFound](../vs140/CRichEditView--OnTextNotFound.md)