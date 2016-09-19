---
title: "CFont::CreateFontIndirect"
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
ms.assetid: f9573b44-382a-40ab-b5d2-1769148c1816
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFont::CreateFontIndirect
Initializes a `CFont` object with the characteristics given in a [LOGFONT](http://msdn.microsoft.com/library/windows/desktop/dd145037)structure.  
  
## Syntax  
  
```  
  
      BOOL CreateFontIndirect(  
   const LOGFONT* lpLogFont   
);  
```  
  
#### Parameters  
 `lpLogFont`  
 Points to a `LOGFONT` structure that defines the characteristics of the logical font.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 The font can subsequently be selected as the current font for any device.  
  
 This font has the characteristics specified in the [LOGFONT](http://msdn.microsoft.com/library/windows/desktop/dd145037) structure. When the font is selected by using the [CDC::SelectObject](../vs140/CDC--SelectObject.md) member function, the GDI font mapper attempts to match the logical font with an existing physical font. If the font mapper fails to find an exact match for the logical font, it provides an alternative font whose characteristics match as many of the requested characteristics as possible.  
  
 When you no longer need the `CFont` object created by the `CreateFontIndirect` function, use `CDC::SelectObject` to select a different font into the device context, then delete the `CFont` object that is no longer needed.  
  
## Example  
 [!CODE [NVC_MFCDocView#72](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#72)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFont Class](../vs140/CFont-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFont::CreateFont](../vs140/CFont--CreateFont.md)   
 [CFont::CreatePointFontIndirect](../vs140/CFont--CreatePointFontIndirect.md)   
 [CDC::SelectObject](../vs140/CDC--SelectObject.md)   
 [CGdiObject::DeleteObject](../vs140/CGdiObject--DeleteObject.md)   
 [CreateFontIndirect](http://msdn.microsoft.com/library/windows/desktop/dd183500)   
 [LOGFONT](http://msdn.microsoft.com/library/windows/desktop/dd145037)