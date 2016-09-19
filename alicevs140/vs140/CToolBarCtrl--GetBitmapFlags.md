---
title: "CToolBarCtrl::GetBitmapFlags"
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
ms.assetid: f8ded00c-e9e8-4bd8-842c-36bf4ceb6664
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::GetBitmapFlags
Retrieves the bitmap flags from the toolbar.  
  
## Syntax  
  
```  
  
UINT GetBitmapFlags( ) const;  
```  
  
## Return Value  
 A **UINT** that has the **TBBF_LARGE** flag set if the display can support large toolbar bitmaps, clear otherwise.  
  
## Remarks  
 You should call it after creating the toolbar but before adding bitmaps to the toolbar. The return value indicates whether the display supports large bitmaps or not. If the display supports large bitmaps and if you choose to use them, call [SetBitmapSize](../vs140/CToolBarCtrl--SetBitmapSize.md) and [SetButtonSize](../vs140/CToolBarCtrl--SetButtonSize.md) before adding your large bitmap using [AddBitmap](../vs140/CToolBarCtrl--AddBitmap.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::AddBitmap](../vs140/CToolBarCtrl--AddBitmap.md)   
 [CToolBarCtrl::SetBitmapSize](../vs140/CToolBarCtrl--SetBitmapSize.md)   
 [CToolBarCtrl::SetButtonSize](../vs140/CToolBarCtrl--SetButtonSize.md)