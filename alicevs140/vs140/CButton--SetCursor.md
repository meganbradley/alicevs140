---
title: "CButton::SetCursor"
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
ms.assetid: 5cb6c748-e81d-4ecf-8d31-cfa1f015b4e7
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CButton::SetCursor
Call this member function to associate a new cursor with the button.  
  
## Syntax  
  
```  
  
      HCURSOR SetCursor(  
   HCURSOR hCursor   
);  
```  
  
#### Parameters  
 `hCursor`  
 The handle of a cursor.  
  
## Return Value  
 The handle of a cursor previously associated with the button.  
  
## Remarks  
 The cursor will be automatically placed on the face of the button, centered by default. If the cursor is too large for the button, it will be clipped on either side. You can choose other alignment options, including the following:  
  
-   **BS_TOP**  
  
-   **BS_LEFT**  
  
-   **BS_RIGHT**  
  
-   **BS_CENTER**  
  
-   **BS_BOTTOM**  
  
-   **BS_VCENTER**  
  
 Unlike [CBitmapButton](../vs140/CBitmapButton-Class.md), which uses four bitmaps per button, `SetCursor` uses only one cursor per the button. When the button is pressed, the cursor appears to shift down and to the right.  
  
## Example  
 [!CODE [NVC_MFC_CButton#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CButton#7)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CButton Class](../vs140/CButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CButton::GetCursor](../vs140/CButton--GetCursor.md)   
 [CBitmapButton::LoadBitmaps](../vs140/CBitmapButton--LoadBitmaps.md)   
 [Bitmaps](http://msdn.microsoft.com/library/windows/desktop/dd183377)