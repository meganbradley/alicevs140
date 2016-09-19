---
title: "CImageList::Draw"
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
ms.assetid: 8799ff57-6540-41f7-b1c2-153c6cef8ba4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImageList::Draw
Call this function to draw the image that is being dragged during a drag-and-drop operation.  
  
## Syntax  
  
```  
  
      BOOL Draw(  
   CDC* pDC,  
   int nImage,  
   POINT pt,  
   UINT nStyle   
);  
```  
  
#### Parameters  
 `pDC`  
 Pointer to the destination device context.  
  
 `nImage`  
 Zero-based index of the image to draw.  
  
 `pt`  
 Location at which to draw within the specified device context.  
  
 `nStyle`  
 Flag specifying the drawing style. It can be one or more of these values:  
  
|Value|Meaning|  
|-----------|-------------|  
|`ILD_BLEND25`, **ILD_FOCUS**|Draws the image, blending 25 percent with the system highlight color. This value has no effect if the image list does not contain a mask.|  
|`ILD_BLEND50`, **ILD_SELECTED**, **ILD_BLEND**|Draws the image, blending 50 percent with the system highlight color. This value has no effect if the image list does not contain a mask.|  
|**ILD_MASK**|Draws the mask.|  
|`ILD_NORMAL`|Draws the image using the background color for the image list. If the background color is the `CLR_NONE` value, the image is drawn transparently using the mask.|  
|`ILD_TRANSPARENT`|Draws the image transparently using the mask, regardless of the background color.|  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Example  
 See the example for [CImageList::SetOverlayImage](../vs140/CImageList--SetOverlayImage.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CImageList Class](../vs140/CImageList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CImageList::BeginDrag](../vs140/CImageList--BeginDrag.md)   
 [CImageList::EndDrag](../vs140/CImageList--EndDrag.md)   
 [CImageList::DragMove](../vs140/CImageList--DragMove.md)   
 [CImageList::DrawEx](../vs140/CImageList--DrawEx.md)