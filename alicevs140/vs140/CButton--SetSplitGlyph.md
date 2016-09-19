---
title: "CButton::SetSplitGlyph"
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
ms.assetid: d3aead8b-926d-4694-b86f-1a81a5848a9c
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CButton::SetSplitGlyph
Associates a specified glyph with the current split button control.  
  
## Syntax  
  
```  
BOOL SetSplitGlyph(  
     TCHAR chGlyph  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `chGlyph`|A character that specifies the glyph to use as the split button drop-down arrow.|  
  
## Return Value  
 `true` if this method is successful; otherwise, `false`.  
  
## Remarks  
 Use this method only with controls that have the button style `BS_SPLITBUTTON` or `BS_DEFSPLITBUTTON`.  
  
 A glyph is the physical representation of a character in a particular font. The `chGlyph`parameter is not used as the glyph, but is instead used to select a glyph from a set of system-defined glyphs. The default drop-down arrow glyph is specified by a character '6', and resembles the Unicode character BLACK DOWN-POINTING TRIANGLE (U+25BC).  
  
 This method initializes the `mask` member of a [BUTTON_SPLITINFO](http://msdn.microsoft.com/library/windows/desktop/bb775955) structure with the `BCSIF_GLYPH` flag and the `himlGlyph` member with the `chGlyph` parameter, and then sends that structure in the [BCM_GETSPLITINFO](http://msdn.microsoft.com/library/windows/desktop/bb775969) message that is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CButton Class](../vs140/CButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CButton::GetSplitGlyph](../vs140/CButton--GetSplitGlyph.md)   
 [BCM_SETSPLITINFO](http://msdn.microsoft.com/library/windows/desktop/bb775981)   
 [BUTTON_SPLITINFO](http://msdn.microsoft.com/library/windows/desktop/bb775955)