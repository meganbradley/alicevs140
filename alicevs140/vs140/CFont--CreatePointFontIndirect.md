---
title: "CFont::CreatePointFontIndirect"
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
ms.assetid: dc8fdbfa-1b87-42ce-90a1-50de8c0883ec
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFont::CreatePointFontIndirect
This function is the same as [CreateFontIndirect](../vs140/CFont--CreateFontIndirect.md) except that the **lfHeight** member of the `LOGFONT` is interpreted in tenths of a point rather than device units.  
  
## Syntax  
  
```  
  
      BOOL CreatePointFontIndirect(  
   const LOGFONT* lpLogFont,  
   CDC* pDC = NULL   
);  
```  
  
#### Parameters  
 `lpLogFont`  
 Points to a [LOGFONT](http://msdn.microsoft.com/library/windows/desktop/dd145037) structure that defines the characteristics of the logical font. The **lfHeight** member of the `LOGFONT` structure is measured in tenths of a point rather than logical units. (For instance, set **lfHeight** to 120 to request a 12-point font.)  
  
 `pDC`  
 Pointer to the [CDC](../vs140/CDC-Class.md) object to be used to convert the height in **lfHeight** to logical units. If **NULL**, a screen device context is used for the conversion.  
  
## Return Value  
 Nonzero if successful, otherwise 0.  
  
## Remarks  
 This function automatically converts the height in **lfHeight** to logical units using the `CDC` object pointed to by `pDC` before passing the `LOGFONT` structure on to Windows.  
  
 When you finish with the `CFont` object created by the `CreatePointFontIndirect` function, first select the font out of the device context, then delete the `CFont` object.  
  
## Example  
 [!CODE [NVC_MFCDocView#74](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#74)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFont Class](../vs140/CFont-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFont::CreatePointFont](../vs140/CFont--CreatePointFont.md)   
 [CFont::CreateFontIndirect](../vs140/CFont--CreateFontIndirect.md)