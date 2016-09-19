---
title: "CBrush::CreateBrushIndirect"
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
ms.assetid: 32979cad-6ccf-4bb1-aacc-44bd1c1fa430
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBrush::CreateBrushIndirect
Initializes a brush with a style, color, and pattern specified in a [LOGBRUSH](http://msdn.microsoft.com/library/windows/desktop/dd145035) structure.  
  
## Syntax  
  
```  
  
      BOOL CreateBrushIndirect(  
   const LOGBRUSH* lpLogBrush   
);  
```  
  
#### Parameters  
 *lpLogBrush*  
 Points to a [LOGBRUSH](http://msdn.microsoft.com/library/windows/desktop/dd145035) structure that contains information about the brush.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 The brush can subsequently be selected as the current brush for any device context.  
  
 A brush created using a monochrome (1 plane, 1 bit per pixel) bitmap is drawn using the current text and background colors. Pixels represented by a bit set to 0 will be drawn with the current text color. Pixels represented by a bit set to 1 will be drawn with the current background color.  
  
## Example  
 [!CODE [NVC_MFCDocView#22](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#22)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CBrush Class](../vs140/CBrush-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CBrush::CreateDIBPatternBrush](../vs140/CBrush--CreateDIBPatternBrush.md)   
 [CBrush::CreatePatternBrush](../vs140/CBrush--CreatePatternBrush.md)   
 [CBrush::CreateSolidBrush](../vs140/CBrush--CreateSolidBrush.md)   
 [CBrush::CreateHatchBrush](../vs140/CBrush--CreateHatchBrush.md)   
 [CGdiObject::CreateStockObject](../vs140/CGdiObject--CreateStockObject.md)   
 [CGdiObject::DeleteObject](../vs140/CGdiObject--DeleteObject.md)   
 [CreateBrushIndirect](http://msdn.microsoft.com/library/windows/desktop/dd183487)