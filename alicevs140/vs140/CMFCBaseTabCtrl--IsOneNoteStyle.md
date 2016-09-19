---
title: "CMFCBaseTabCtrl::IsOneNoteStyle"
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
ms.assetid: 3b3a4b8c-a98e-4d3f-aa9c-4efcf8118e9f
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::IsOneNoteStyle
Determines whether tabs are displayed in the style of Microsoft OneNote.  
  
## Syntax  
  
```  
virtual BOOL IsOneNoteStyle() const;  
```  
  
## Return Value  
 `TRUE` if tabs are displayed in the style of Microsoft OneNote; otherwise `FALSE`.  
  
## Remarks  
 Call the method [CMDIFrameWndEx::EnableMDITabs](../vs140/CMDIFrameWndEx--EnableMDITabs.md) to enable the Microsoft OneNote style. You can also enable this style when you instantiate the [CMFCTabCtrl Class](../vs140/CMFCTabCtrl-Class.md): simply pass the style STYLE_3D_ONENOTE to the method [CMFCTabCtrl::Create](../vs140/CMFCTabCtrl--Create.md).  
  
 By default, the Microsoft OneNote style is not supported in a custom class derived from the [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md). However, it is supported in the `CMFCTabCtrl` class.  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)