---
title: "CMFCRibbonEdit::OnDrawOnList"
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
ms.assetid: 55334176-8d9c-4b23-98a4-fd808c1f56e5
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonEdit::OnDrawOnList
Called by the framework to draw the [CMFCRibbonEdit](../vs140/CMFCRibbonEdit-Class.md) control in a commands list box.  
  
## Syntax  
  
```  
virtual void OnDrawOnList(  
   CDC* pDC,  
   CString strText,  
   int nTextOffset,  
   CRect rect,  
   BOOL bIsSelected,  
   BOOL bHighlighted  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 Pointer to a device context for the [CMFCRibbonEdit](../vs140/CMFCRibbonEdit-Class.md) control.  
  
 [in] `strText`  
 The display text[](../vs140/CMFCRibbonEdit-Class.md "CMFCRibbonEdit Class").  
  
 [in] `nTextOffset`  
 Distance, in pixels, from the left side of the list box to the display text.  
  
 [in] `rect`  
 The display rectangle for the [CMFCRibbonEdit](../vs140/CMFCRibbonEdit-Class.md) control.  
  
 [in] `bIsSelected`  
 This parameter is not used.  
  
 [in] `bHighlighted`  
 This parameter is not used.  
  
## Remarks  
 The commands list box displays ribbon controls to enable users to customize the quick access toolbar.  
  
## Requirements  
 **Header:** afxribbonedit.h  
  
## See Also  
 [CMFCRibbonEdit Class](../vs140/CMFCRibbonEdit-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)