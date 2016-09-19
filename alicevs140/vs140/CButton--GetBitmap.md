---
title: "CButton::GetBitmap"
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
ms.assetid: 76d3eb3e-0ee4-44bf-b9b7-534efa8bdead
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CButton::GetBitmap
Call this member function to get the handle of a bitmap, previously set with [SetBitmap](../vs140/CButton--SetBitmap.md), that is associated with a button.  
  
## Syntax  
  
```  
  
HBITMAP GetBitmap( ) const;  
  
```  
  
## Return Value  
 A handle to a bitmap. **NULL** if no bitmap is previously specified.  
  
## Example  
 [!CODE [NVC_MFC_CButton#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CButton#4)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CButton Class](../vs140/CButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CButton::SetBitmap](../vs140/CButton--SetBitmap.md)   
 [CBitmapButton::LoadBitmaps](../vs140/CBitmapButton--LoadBitmaps.md)   
 [Bitmaps](http://msdn.microsoft.com/library/windows/desktop/dd183377)