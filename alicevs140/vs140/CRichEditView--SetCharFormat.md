---
title: "CRichEditView::SetCharFormat"
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
ms.assetid: cc3fd397-012d-4c45-8be3-13982aa2a762
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::SetCharFormat
Call this function to set the character formatting attributes for new text in this `CRichEditView` object.  
  
## Syntax  
  
```  
  
      void SetCharFormat(  
   CHARFORMAT2 cf   
);  
```  
  
#### Parameters  
 `cf`  
 [CHARFORMAT2](http://msdn.microsoft.com/library/windows/desktop/bb787883) structure containing the new default character formatting attributes.  
  
## Remarks  
 Only the attributes specified by the **dwMask** member of `cf` are changed by this function.  
  
 For more information, see [EM_SETCHARFORMAT](http://msdn.microsoft.com/library/windows/desktop/bb774230) message and [CHARFORMAT2](http://msdn.microsoft.com/library/windows/desktop/bb787883) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFCDocView#152](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#152)]  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditView::GetCharFormatSelection](../vs140/CRichEditView--GetCharFormatSelection.md)   
 [CRichEditView::SetParaFormat](../vs140/CRichEditView--SetParaFormat.md)