---
title: "CRichEditView::IsRichEditFormat"
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
ms.assetid: 888c6851-8a12-4a2f-b73d-63eae0684e9c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::IsRichEditFormat
Call this function to determine if `cf` is a Clipboard format which is text, rich text, or rich text with OLE items.  
  
## Syntax  
  
```  
  
      static BOOL AFX_CDECL IsRichEditFormat(  
   CLIPFORMAT cf   
);  
```  
  
#### Parameters  
 `cf`  
 The Clipboard format of interest.  
  
## Return Value  
 Nonzero if `cf` is a rich edit or text Clipboard format.  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::CanPaste](../vs140/CRichEditCtrl--CanPaste.md)   
 [CRichEditCtrl::Paste](../vs140/CRichEditCtrl--Paste.md)   
 [CRichEditView::DoPaste](../vs140/CRichEditView--DoPaste.md)