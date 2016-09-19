---
title: "CRichEditView::GetParaFormatSelection"
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
ms.assetid: af54f34b-b645-4fc1-a580-a517d2b11e04
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::GetParaFormatSelection
Call this function to get the paragraph formatting attributes of the current selection.  
  
## Syntax  
  
```  
  
PARAFORMAT2& GetParaFormatSelection( );  
  
```  
  
## Return Value  
 A [PARAFORMAT2](http://msdn.microsoft.com/library/windows/desktop/bb787942) structure which contains the paragraph formatting attributes of the current selection.  
  
## Remarks  
 For more information, see [EM_GETPARAFORMAT](http://msdn.microsoft.com/library/windows/desktop/bb774182) message and [PARAFORMAT2](http://msdn.microsoft.com/library/windows/desktop/bb787942) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditView::GetCharFormatSelection](../vs140/CRichEditView--GetCharFormatSelection.md)   
 [CRichEditView::SetParaFormat](../vs140/CRichEditView--SetParaFormat.md)   
 [CRichEditCtrl::GetParaFormat](../vs140/CRichEditCtrl--GetParaFormat.md)