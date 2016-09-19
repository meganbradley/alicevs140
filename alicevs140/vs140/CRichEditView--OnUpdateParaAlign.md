---
title: "CRichEditView::OnUpdateParaAlign"
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
ms.assetid: 9e7d4ded-7790-44a7-85ef-9402636de145
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::OnUpdateParaAlign
The framework calls this function to update the command UI for paragraph effect commands.  
  
## Syntax  
  
```  
  
      void OnUpdateParaAlign(  
   CCmdUI* pCmdUI,  
   WORD wAlign   
);  
```  
  
#### Parameters  
 `pCmdUI`  
 Pointer to a [CCmdUI](../vs140/CCmdUI-Class.md) object.  
  
 `wAlign`  
 The paragraph alignment to check. One of the following values:  
  
-   `PFA_LEFT` Align the paragraphs with the left margin.  
  
-   `PFA_RIGHT` Align the paragraphs with the right margin.  
  
-   `PFA_CENTER` Center the paragraphs between the margins.  
  
## Example  
 [!CODE [NVC_MFCDocView#159](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#159)]  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditView::GetParaFormatSelection](../vs140/CRichEditView--GetParaFormatSelection.md)   
 [CRichEditView::OnParaAlign](../vs140/CRichEditView--OnParaAlign.md)   
 [CRichEditView::SetParaFormat](../vs140/CRichEditView--SetParaFormat.md)