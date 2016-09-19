---
title: "CButton::SetIcon"
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
ms.assetid: b8a91ece-ff51-492a-a978-a4d4acba813a
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CButton::SetIcon
Call this member function to associate a new icon with the button.  
  
## Syntax  
  
```  
  
      HICON SetIcon(  
   HICON hIcon   
);  
```  
  
#### Parameters  
 `hIcon`  
 The handle of an icon.  
  
## Return Value  
 The handle of an icon previously associated with the button.  
  
## Remarks  
 The icon will be automatically placed on the face of the button, centered by default. If the icon is too large for the button, it will be clipped on either side. You can choose other alignment options, including the following:  
  
-   **BS_TOP**  
  
-   **BS_LEFT**  
  
-   **BS_RIGHT**  
  
-   **BS_CENTER**  
  
-   **BS_BOTTOM**  
  
-   **BS_VCENTER**  
  
 Unlike [CBitmapButton](../vs140/CBitmapButton-Class.md), which uses four bitmaps per button, `SetIcon` uses only one icon per the button. When the button is pressed, the icon appears to shift down and to the right.  
  
## Example  
 [!CODE [NVC_MFC_CButton#8](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CButton#8)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CButton Class](../vs140/CButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CButton::GetIcon](../vs140/CButton--GetIcon.md)   
 [CBitmapButton::LoadBitmaps](../vs140/CBitmapButton--LoadBitmaps.md)   
 [Bitmaps](http://msdn.microsoft.com/library/windows/desktop/dd183377)