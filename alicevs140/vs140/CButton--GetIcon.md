---
title: "CButton::GetIcon"
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
ms.assetid: 3b183f4c-ae8d-46a5-b45e-77a02786033e
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CButton::GetIcon
Call this member function to get the handle of an icon, previously set with [SetIcon](../vs140/CButton--SetIcon.md), that is associated with a button.  
  
## Syntax  
  
```  
  
HICON GetIcon( ) const;  
  
```  
  
## Return Value  
 A handle to an icon. **NULL** if no icon is previously specified.  
  
## Example  
 [!CODE [NVC_MFC_CButton#8](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CButton#8)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CButton Class](../vs140/CButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CButton::SetIcon](../vs140/CButton--SetIcon.md)   
 [CBitmapButton::LoadBitmaps](../vs140/CBitmapButton--LoadBitmaps.md)   
 [Bitmaps](http://msdn.microsoft.com/library/windows/desktop/dd183377)