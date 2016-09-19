---
title: "CRichEditCtrl::LineLength"
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
ms.assetid: 05d222fa-9be2-4bb6-b079-06e0335c2e31
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::LineLength
Retrieves the length of a line in a rich edit control.  
  
## Syntax  
  
```  
  
      int LineLength(  
   int nLine = -1   
) const;  
```  
  
#### Parameters  
 `nLine`  
 Specifies the character index of a character in the line whose length is to be retrieved. If this parameter is –1, the length of the current line (the line that contains the caret) is returned, not including the length of any selected text within the line. When `LineLength` is called for a single-line edit control, this parameter is ignored.  
  
## Return Value  
 When `LineLength` is called for a multiple-line edit control, the return value is the length (in bytes) of the line specified by `nLine`. When `LineLength` is called for a single-line edit control, the return value is the length (in bytes) of the text in the edit control.  
  
## Remarks  
 Use the [LineIndex](../vs140/CRichEditCtrl--LineIndex.md) member function to retrieve a character index for a given line number within this `CRichEditCtrl` object.  
  
 For more information, see [EM_LINELENGTH](http://msdn.microsoft.com/library/windows/desktop/bb761613) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [LineIndex](../vs140/CRichEditCtrl--LineIndex.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::LineIndex](../vs140/CRichEditCtrl--LineIndex.md)