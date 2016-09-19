---
title: "CMFCImageEditorDialog::CMFCImageEditorDialog"
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
ms.assetid: 59a0ef1e-65cc-4b40-9f72-78bb575562eb
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCImageEditorDialog::CMFCImageEditorDialog
Constructs a `CMFCImageEditorDialog` object.  
  
## Syntax  
  
```  
CMFCImageEditorDialog(  
   CBitmap* pBitmap,  
   CWnd* pParent=NULL,  
   int nBitsPixel=-1   
);  
```  
  
#### Parameters  
 `pBitmap`  
 Pointer to an image.  
  
 `pParent`  
 Pointer to the parent window of the current image editor dialog box.  
  
 `nBitsPixel`  
 The number of bits used to represent the color of a single pixel, which is also referred to as color depth.  If the `nBitsPixel` parameter is -1, the color depth is derived from the image specified by the `pBitmap` parameter. The default value is -1.  
  
## Return Value  
 To modify an image, pass an image pointer to the `CMFCImageEditorDialog` constructor. Then call the `DoModal` method to open a modal dialog box. When the `DoModal` method returns, the bitmap contains the new image.  
  
## Remarks  
  
## Example  
 The following example demonstrates how to construct an object of the `CMFCImageEditorDialog` class. This example is part of the [New Controls sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_NewControls#8](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_NewControls#8)]  
[!CODE [NVC_MFC_NewControls#40](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_NewControls#40)]  
  
## Requirements  
 **Header:** afximageeditordialog.h  
  
## See Also  
 [CMFCImageEditorDialog Class](../vs140/CMFCImageEditorDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)