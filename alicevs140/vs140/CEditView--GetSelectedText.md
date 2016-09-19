---
title: "CEditView::GetSelectedText"
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
ms.assetid: 5b400de3-acb8-4e09-90bf-33342c640493
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEditView::GetSelectedText
Call `GetSelectedText` to copy the selected text into a `CString` object, up to the end of the selection or the character preceding the first carriage-return character in the selection.  
  
## Syntax  
  
```  
  
      void GetSelectedText(  
   CString& strResult   
) const;  
```  
  
#### Parameters  
 `strResult`  
 A reference to the `CString` object that is to receive the selected text.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CEditView Class](../vs140/CEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEditView::OnReplaceSel](../vs140/CEditView--OnReplaceSel.md)