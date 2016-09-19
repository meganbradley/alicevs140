---
title: "CButton::SetBitmap"
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
ms.assetid: 1f03c1eb-31d3-488e-8fbf-a5ea81899ed5
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CButton::SetBitmap
Call this member function to associate a new bitmap with the button.  
  
## Syntax  
  
```  
  
      HBITMAP SetBitmap(  
   HBITMAP hBitmap   
);  
```  
  
#### Parameters  
 `hBitmap`  
 The handle of a bitmap.  
  
## Return Value  
 The handle of a bitmap previously associated with the button.  
  
## Remarks  
 The bitmap will be automatically placed on the face of the button, centered by default. If the bitmap is too large for the button, it will be clipped on either side. You can choose other alignment options, including the following:  
  
-   **BS_TOP**  
  
-   **BS_LEFT**  
  
-   **BS_RIGHT**  
  
-   **BS_CENTER**  
  
-   **BS_BOTTOM**  
  
-   **BS_VCENTER**  
  
 Unlike [CBitmapButton](../vs140/CBitmapButton-Class.md), which uses four bitmaps per button, `SetBitmap` uses only one bitmap per the button. When the button is pressed, the bitmap appears to shift down and to the right.  
  
 You are responsible for releasing the bitmap when you are done with it.  
  
## Example  
 [!CODE [NVC_MFC_CButton#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CButton#4)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CButton Class](../vs140/CButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CButton::GetBitmap](../vs140/CButton--GetBitmap.md)   
 [CBitmapButton Class](../vs140/CBitmapButton-Class.md)   
 [CBitmapButton::LoadBitmaps](../vs140/CBitmapButton--LoadBitmaps.md)   
 [Bitmaps](http://msdn.microsoft.com/library/windows/desktop/dd183377)