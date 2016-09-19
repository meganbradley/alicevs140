---
title: "CView::OnPrepareDC"
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
ms.assetid: e7d3920c-1f3e-440c-ab1d-0544974b119b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CView::OnPrepareDC
Called by the framework before the [OnDraw](../vs140/CView--OnDraw.md) member function is called for screen display and before the [OnPrint](../vs140/CView--OnPrint.md) member function is called for each page during printing or print preview.  
  
## Syntax  
  
```  
  
      virtual void OnPrepareDC(  
   CDC* pDC,  
   CPrintInfo* pInfo = NULL   
);  
```  
  
#### Parameters  
 `pDC`  
 Points to the device context to be used for rendering an image of the document.  
  
 `pInfo`  
 Points to a [CPrintInfo](../vs140/CPrintInfo-Structure.md) structure that describes the current print job if `OnPrepareDC` is being called for printing or print preview; the `m_nCurPage` member specifies the page about to be printed. This parameter is **NULL** if `OnPrepareDC` is being called for screen display.  
  
## Remarks  
 The default implementation of this function does nothing if the function is called for screen display. However, this function is overridden in derived classes, such as [CScrollView](../vs140/CScrollView-Class.md), to adjust attributes of the device context; consequently, you should always call the base class implementation at the beginning of your override.  
  
 If the function is called for printing, the default implementation examines the page information stored in the `pInfo` parameter. If the length of the document has not been specified, `OnPrepareDC` assumes the document to be one page long and stops the print loop after one page has been printed. The function stops the print loop by setting the `m_bContinuePrinting` member of the structure to **FALSE**.  
  
 Override `OnPrepareDC` for any of the following reasons:  
  
-   To adjust attributes of the device context as needed for the specified page. For example, if you need to set the mapping mode or other characteristics of the device context, do so in this function.  
  
-   To perform print-time pagination. Normally you specify the length of the document when printing begins, using the [OnPreparePrinting](../vs140/CView--OnPreparePrinting.md) member function. However, if you don't know in advance how long the document is (for example, when printing an undetermined number of records from a database), override `OnPrepareDC` to test for the end of the document while it is being printed. When there is no more of the document to be printed, set the `m_bContinuePrinting` member of the `CPrintInfo` structure to **FALSE**.  
  
-   To send escape codes to the printer on a page-by-page basis. To send escape codes from `OnPrepareDC`, call the **Escape** member function of the `pDC` parameter.  
  
 Call the base class version of `OnPrepareDC` at the beginning of your override.  
  
## Example  
 [!CODE [NVC_MFCDocView#183](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#183)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CView Class](../vs140/CView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::Escape](../vs140/CDC--Escape.md)   
 [CPrintInfo Structure](../vs140/CPrintInfo-Structure.md)   
 [CView::OnBeginPrinting](../vs140/CView--OnBeginPrinting.md)   
 [CView::OnDraw](../vs140/CView--OnDraw.md)   
 [CView::OnPreparePrinting](../vs140/CView--OnPreparePrinting.md)   
 [CView::OnPrint](../vs140/CView--OnPrint.md)