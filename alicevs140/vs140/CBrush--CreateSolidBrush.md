---
title: "CBrush::CreateSolidBrush"
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
ms.assetid: 7cf61aef-04ec-46f6-9c0c-60d6befd9ed9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBrush::CreateSolidBrush
Initializes a brush with a specified solid color.  
  
## Syntax  
  
```  
  
      BOOL CreateSolidBrush(  
   COLORREF crColor   
);  
```  
  
#### Parameters  
 `crColor`  
 A [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) structure that specifies the color of the brush. The color specifies an RGB value and can be constructed with the `RGB` macro in WINDOWS.H.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 The brush can subsequently be selected as the current brush for any device context.  
  
 When an application has finished using the brush created by `CreateSolidBrush`, it should select the brush out of the device context.  
  
## Example  
 See the example for [CBrush::CBrush](../vs140/CBrush--CBrush.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CBrush Class](../vs140/CBrush-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CBrush::CreateBrushIndirect](../vs140/CBrush--CreateBrushIndirect.md)   
 [CBrush::CreateDIBPatternBrush](../vs140/CBrush--CreateDIBPatternBrush.md)   
 [CBrush::CreateHatchBrush](../vs140/CBrush--CreateHatchBrush.md)   
 [CBrush::CreatePatternBrush](../vs140/CBrush--CreatePatternBrush.md)   
 [CreateSolidBrush](http://msdn.microsoft.com/library/windows/desktop/dd183518)   
 [CGdiObject::DeleteObject](../vs140/CGdiObject--DeleteObject.md)