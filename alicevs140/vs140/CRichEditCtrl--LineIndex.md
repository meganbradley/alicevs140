---
title: "CRichEditCtrl::LineIndex"
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
ms.assetid: 4e4bc33d-93fb-4b0c-ae04-3fee60ae6179
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::LineIndex
Retrieves the character index of a line within this `CRichEditCtrl` object.  
  
## Syntax  
  
```  
  
      int LineIndex(  
   int nLine = -1   
) const;  
```  
  
#### Parameters  
 `nLine`  
 Contains the index value for the desired line in the text of the edit control, or contains –1. If `nLine` is –1, it specifies the current line, that is, the line that contains the caret.  
  
## Return Value  
 The character index of the line specified in `nLine` or –1 if the specified line number is greater then the number of lines in the edit control.  
  
## Remarks  
 The character index is the number of characters from the beginning of the rich edit control to the specified line.  
  
 For more information, see [EM_LINEINDEX](http://msdn.microsoft.com/library/windows/desktop/bb761611) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CRichEditCtrl#21](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CRichEditCtrl#21)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::LineFromChar](../vs140/CRichEditCtrl--LineFromChar.md)   
 [CRichEditCtrl::GetLineCount](../vs140/CRichEditCtrl--GetLineCount.md)