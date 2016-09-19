---
title: "CFont::operator HFONT"
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
ms.assetid: df583301-da1e-4da8-98a0-b2f399e2aa24
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFont::operator HFONT
Use this operator to get the Windows GDI handle of the font attached to the `CFont` object.  
  
## Syntax  
  
```  
  
operator HFONT( ) const;  
  
```  
  
## Return Value  
 The handle of the Windows GDI font object attached to `CFont` if successful; otherwise **NULL**.  
  
## Remarks  
 Since this operator is automatically used for conversions from `CFont` to [Fonts and Text](http://msdn.microsoft.com/library/windows/desktop/dd144819), you can pass `CFont` objects to functions that expect **HFONT**s.  
  
 For more information about using graphic objects, see [Graphic Objects](http://msdn.microsoft.com/library/windows/desktop/dd144962) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFCDocView#77](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#77)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFont Class](../vs140/CFont-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)