---
title: "CRichEditView::OnParaAlign"
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
ms.assetid: fed46c64-d765-49f3-a045-0e4ca51758c3
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::OnParaAlign
Call this function to change the paragraph alignment for the selected paragraphs.  
  
## Syntax  
  
```  
  
      void OnParaAlign(  
   WORD wAlign   
);  
```  
  
#### Parameters  
 `wAlign`  
 Desired paragraph alignment. One of the following values:  
  
-   `PFA_LEFT` Align the paragraphs with the left margin.  
  
-   `PFA_RIGHT` Align the paragraphs with the right margin.  
  
-   `PFA_CENTER` Center the paragraphs between the margins.  
  
## Example  
 [!CODE [NVC_MFCDocView#156](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#156)]  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditView::OnUpdateParaAlign](../vs140/CRichEditView--OnUpdateParaAlign.md)