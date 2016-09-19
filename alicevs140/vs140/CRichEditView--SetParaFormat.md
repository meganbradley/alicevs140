---
title: "CRichEditView::SetParaFormat"
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
ms.assetid: 2fd8ca4c-79e6-4d00-8b2a-a422fb2242ce
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::SetParaFormat
Call this function to set the paragraph formatting attributes for the current selection in this `CRichEditView` object.  
  
## Syntax  
  
```  
  
      BOOL SetParaFormat(  
   PARAFORMAT2& pf   
);  
```  
  
#### Parameters  
 `pf`  
 [PARAFORMAT2](http://msdn.microsoft.com/library/windows/desktop/bb787942) structure containing the new default paragraph formatting attributes.  
  
## Return Value  
 Nonzero if successful; otherwise, 0.  
  
## Remarks  
 Only the attributes specified by the **dwMask** member of `pf` are changed by this function.  
  
 For more information, see [EM_SETPARAFORMAT](http://msdn.microsoft.com/library/windows/desktop/bb774276) message and [PARAFORMAT2](http://msdn.microsoft.com/library/windows/desktop/bb787942) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFCDocView#162](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#162)]  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditView::GetParaFormatSelection](../vs140/CRichEditView--GetParaFormatSelection.md)   
 [CRichEditView::SetCharFormat](../vs140/CRichEditView--SetCharFormat.md)