---
title: "CRichEditView::GetCharFormatSelection"
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
ms.assetid: bc9dbd03-105c-4062-860d-1b094c54bb6e
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::GetCharFormatSelection
Call this function to get the character formatting attributes of the current selection.  
  
## Syntax  
  
```  
  
CHARFORMAT2& GetCharFormatSelection( );  
  
```  
  
## Return Value  
 A [CHARFORMAT2](http://msdn.microsoft.com/library/windows/desktop/bb787883) structure which contains the character formatting attributes of the current selection.  
  
## Remarks  
 For more information, see the [EM_GETCHARFORMAT](http://msdn.microsoft.com/library/windows/desktop/bb788026) message and the [CHARFORMAT2](http://msdn.microsoft.com/library/windows/desktop/bb787883) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFCDocView#152](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#152)]  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditView::SetCharFormat](../vs140/CRichEditView--SetCharFormat.md)   
 [CRichEditView::GetParaFormatSelection](../vs140/CRichEditView--GetParaFormatSelection.md)   
 [CRichEditCtrl::GetSelectionCharFormat](../vs140/CRichEditCtrl--GetSelectionCharFormat.md)