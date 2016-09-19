---
title: "CButton::GetSplitGlyph"
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
ms.assetid: fd5aa3ee-5afd-4509-8777-ccf066341ac8
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CButton::GetSplitGlyph
Retrieves the glyph associated with the current split button control.  
  
## Syntax  
  
```  
TCHAR GetSplitGlyph() const;  
```  
  
## Return Value  
 The glyph character associated with the current split button control.  
  
## Remarks  
 A glyph is the physical representation of a character in a particular font. For example, a split button control might be decorated with the glyph of the Unicode check mark character (U+2713).  
  
 Use this method only with controls whose button style is `BS_SPLITBUTTON` or `BS_DEFSPLITBUTTON`.  
  
 This method initializes the `mask` member of a [BUTTON_SPLITINFO](http://msdn.microsoft.com/library/windows/desktop/bb775955) structure with the `BCSIF_GLYPH` flag, and then sends that structure in the [BCM_GETSPLITINFO](http://msdn.microsoft.com/library/windows/desktop/bb775969) message that is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. When the message function returns, this method retrieves the glyph from the `himlGlyph` member of the structure.  
  
## Requirements  
 **Header:** afxwin.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CButton Class](../vs140/CButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CButton::SetSplitGlyph](../vs140/CButton--SetSplitGlyph.md)