---
title: "CBrush::CreateHatchBrush"
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
ms.assetid: 30028a59-abe1-4a6e-958e-a57eb832a2e5
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBrush::CreateHatchBrush
Initializes a brush with the specified hatched pattern and color.  
  
## Syntax  
  
```  
  
      BOOL CreateHatchBrush(  
   int nIndex,  
   COLORREF crColor   
);  
```  
  
#### Parameters  
 `nIndex`  
 Specifies the hatch style of the brush. It can be any one of the following values:  
  
-   `HS_BDIAGONAL` Downward hatch (left to right) at 45 degrees  
  
-   `HS_CROSS` Horizontal and vertical crosshatch  
  
-   `HS_DIAGCROSS` Crosshatch at 45 degrees  
  
-   `HS_FDIAGONAL` Upward hatch (left to right) at 45 degrees  
  
-   `HS_HORIZONTAL` Horizontal hatch  
  
-   `HS_VERTICAL` Vertical hatch  
  
 `crColor`  
 Specifies the foreground color of the brush as an RGB color (the color of the hatches). See [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for more information.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 The brush can subsequently be selected as the current brush for any device context.  
  
## Example  
 [!CODE [NVC_MFCDocView#24](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#24)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CBrush Class](../vs140/CBrush-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CBrush::CreateBrushIndirect](../vs140/CBrush--CreateBrushIndirect.md)   
 [CBrush::CreateDIBPatternBrush](../vs140/CBrush--CreateDIBPatternBrush.md)   
 [CBrush::CreatePatternBrush](../vs140/CBrush--CreatePatternBrush.md)   
 [CBrush::CreateSolidBrush](../vs140/CBrush--CreateSolidBrush.md)   
 [CGdiObject::CreateStockObject](../vs140/CGdiObject--CreateStockObject.md)   
 [CreateHatchBrush](http://msdn.microsoft.com/library/windows/desktop/dd183504)