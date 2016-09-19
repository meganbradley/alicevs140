---
title: "COleControl::OnGetInPlaceMenu"
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
ms.assetid: 2eae9775-5a52-4dc5-a8d6-99b320fae9ec
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::OnGetInPlaceMenu
Called by the framework when the control is UI activated to obtain the menu to be merged into the container's existing menu.  
  
## Syntax  
  
```  
  
virtual HMENU OnGetInPlaceMenu( );  
```  
  
## Return Value  
 The handle of the control's menu, or **NULL** if the control has none. The default implementation returns **NULL**.  
  
## Remarks  
 For more information on merging OLE resources, see the article [Menus and Resources (OLE)](../vs140/Menus-and-Resources--OLE-.md).  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)