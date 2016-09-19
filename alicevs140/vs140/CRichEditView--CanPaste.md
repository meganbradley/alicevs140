---
title: "CRichEditView::CanPaste"
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
ms.assetid: a26eb57e-9632-4ce1-a8a0-b78b7c5323e2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::CanPaste
Call this function to determine if the Clipboard contains information that can be pasted into this rich edit view.  
  
## Syntax  
  
```  
  
BOOL CanPaste( ) const;  
  
```  
  
## Return Value  
 Nonzero if the Clipboard contains data in a format which this rich edit view can accept; otherwise, 0.  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::Paste](../vs140/CRichEditCtrl--Paste.md)   
 [CRichEditView::DoPaste](../vs140/CRichEditView--DoPaste.md)   
 [CRichEditView::IsRichEditFormat](../vs140/CRichEditView--IsRichEditFormat.md)