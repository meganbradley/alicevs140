---
title: "CPageSetupDialog::OnDrawPage"
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
ms.assetid: ba40bb7a-c1bc-446f-8d14-2337c926811c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPageSetupDialog::OnDrawPage
Called by the framework to draw a screen image of a printed page.  
  
## Syntax  
  
```  
  
      virtual UINT OnDrawPage(  
   CDC* pDC,  
   UINT nMessage,  
   LPRECT lpRect   
);  
```  
  
#### Parameters  
 `pDC`  
 Pointer to the printer device context.  
  
 `nMessage`  
 Specifies a message, indicating the area of the page currently being drawn. Can be one of the following:  
  
-   **WM_PSD_FULLPAGERECT** The entire page area.  
  
-   **WM_PSD_MINMARGINRECT** Current minimum margins.  
  
-   **WM_PSD_MARGINRECT** Current margins.  
  
-   **WM_PSD_GREEKTEXTRECT** Contents of the page.  
  
-   **WM_PSD_ENVSTAMPRECT** Area reserved for a postage stamp representation.  
  
-   **WM_PSD_YAFULLPAGERECT** Area for a return address representation. This area extends to the edges of the sample page area.  
  
 `lpRect`  
 Pointer to a [CRect](../vs140/CRect-Class.md) or [RECT](../vs140/RECT-Structure.md) object containing the coordinates of the drawing area.  
  
## Return Value  
 Nonzero value if handled; otherwise 0.  
  
## Remarks  
 This image is then displayed as part of the common OLE Page Setup dialog box. The default implementation draws an image of a page of text.  
  
 Override this function to customize the drawing of a specific area of the image, or the entire image. You can do this by using a `switch` statement with **case** statements checking the value of `nMessage`. For example, to customize the rendering of the contents of the page image, you could use the following example code:  
  
 [!CODE [NVC_MFCDocView#96](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#96)]  
  
 Note that you do not need to handle every case of `nMessage`. You can choose to handle one component of the image, several components of the image, or the whole area.  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPageSetupDialog Class](../vs140/CPageSetupDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPageSetupDialog::PreDrawPage](../vs140/CPageSetupDialog--PreDrawPage.md)