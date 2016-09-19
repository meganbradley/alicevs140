---
title: "CStatic::GetBitmap"
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
ms.assetid: 9c2f32ea-a92b-4222-93e0-16f54887f784
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStatic::GetBitmap
Gets the handle of the bitmap, previously set with [SetBitmap](../vs140/CStatic--SetBitmap.md), that is associated with `CStatic`.  
  
## Syntax  
  
```  
  
HBITMAP GetBitmap( ) const;  
  
```  
  
## Return Value  
 A handle to the current bitmap, or **NULL** if no bitmap has been set.  
  
## Example  
 [!CODE [NVC_MFC_CStatic#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CStatic#3)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CStatic Class](../vs140/CStatic-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CStatic::SetBitmap](../vs140/CStatic--SetBitmap.md)   
 [STM_GETIMAGE](http://msdn.microsoft.com/library/windows/desktop/bb760778)   
 [Bitmaps](http://msdn.microsoft.com/library/windows/desktop/dd183377)