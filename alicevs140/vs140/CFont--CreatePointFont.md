---
title: "CFont::CreatePointFont"
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
ms.assetid: 211af19d-bddd-4ec5-8ad4-4f8528618909
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFont::CreatePointFont
This function provides a simple way to create a font of a specified typeface and point size.  
  
## Syntax  
  
```  
  
      BOOL CreatePointFont(  
   int nPointSize,  
   LPCTSTR lpszFaceName,  
   CDC* pDC = NULL   
);  
```  
  
#### Parameters  
 `nPointSize`  
 Requested font height in tenths of a point. (For instance, pass 120 to request a 12-point font.)  
  
 `lpszFaceName`  
 A `CString` or pointer to a null-terminated string that specifies the typeface name of the font. The length of this string must not exceed 30 characters. The Windows **EnumFontFamilies** function can be used to enumerate all currently available fonts. If `lpszFaceName` is **NULL**, the GDI uses a device-independent typeface.  
  
 `pDC`  
 Pointer to the [CDC](../vs140/CDC-Class.md) object to be used to convert the height in `nPointSize` to logical units. If **NULL**, a screen device context is used for the conversion.  
  
## Return Value  
 Nonzero if successful, otherwise 0.  
  
## Remarks  
 It automatically converts the height in `nPointSize` to logical units using the `CDC` object pointed to by `pDC`.  
  
 When you finish with the `CFont` object created by the `CreatePointFont` function, first select the font out of the device context, then delete the `CFont` object.  
  
## Example  
 [!CODE [NVC_MFCDocView#73](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#73)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFont Class](../vs140/CFont-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFont::CreatePointFontIndirect](../vs140/CFont--CreatePointFontIndirect.md)   
 [CFont::CreateFont](../vs140/CFont--CreateFont.md)