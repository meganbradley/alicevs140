---
title: "CButton::GetCursor"
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
ms.assetid: 1ec82c5e-a2f9-4321-b4f6-33cdf605bdcc
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CButton::GetCursor
Call this member function to get the handle of a cursor, previously set with [SetCursor](../vs140/CButton--SetCursor.md), that is associated with a button.  
  
## Syntax  
  
```  
  
HCURSOR GetCursor( );  
  
```  
  
## Return Value  
 A handle to a cursor image. **NULL** if no cursor is previously specified.  
  
## Example  
 [!CODE [NVC_MFC_CButton#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CButton#7)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CButton Class](../vs140/CButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CButton::SetCursor](../vs140/CButton--SetCursor.md)   
 [CBitmapButton::LoadBitmaps](../vs140/CBitmapButton--LoadBitmaps.md)   
 [Bitmaps](http://msdn.microsoft.com/library/windows/desktop/dd183377)