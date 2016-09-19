---
title: "CBrush::CreateDIBPatternBrush"
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
ms.assetid: 965a6718-c114-416f-b480-0493023b323a
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBrush::CreateDIBPatternBrush
Initializes a brush with the pattern specified by a device-independent bitmap (DIB).  
  
## Syntax  
  
```  
  
      BOOL CreateDIBPatternBrush(  
   HGLOBAL hPackedDIB,  
   UINT nUsage   
);  
BOOL CreateDIBPatternBrush(  
   const void* lpPackedDIB,  
   UINT nUsage   
);  
```  
  
#### Parameters  
 *hPackedDIB*  
 Identifies a global-memory object containing a packed device-independent bitmap (DIB).  
  
 *nUsage*  
 Specifies whether the **bmiColors[]** fields of the [BITMAPINFO](../vs140/BITMAPINFO-Structure.md) data structure (a part of the "packed DIB") contain explicit RGB values or indices into the currently realized logical palette. The parameter must be one of the following values:  
  
-   **DIB_PAL_COLORS** The color table consists of an array of 16-bit indexes.  
  
-   **DIB_RGB_COLORS** The color table contains literal RGB values.  
  
 *lpPackedDIB*  
 Points to a packed DIB consisting of a `BITMAPINFO` structure immediately followed by an array of bytes defining the pixels of the bitmap.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 The brush can subsequently be selected for any device context that supports raster operations.  
  
 The two versions differ in the way you handle the DIB:  
  
-   In the first version, to obtain a handle to the DIB you call the Windows **GlobalAlloc** function to allocate a block of global memory and then fill the memory with the packed DIB.  
  
-   In the second version, it is not necessary to call **GlobalAlloc** to allocate memory for the packed DIB.  
  
 A packed DIB consists of a `BITMAPINFO` data structure immediately followed by the array of bytes that defines the pixels of the bitmap. Bitmaps used as fill patterns should be 8 pixels by 8 pixels. If the bitmap is larger, Windows creates a fill pattern using only the bits corresponding to the first 8 rows and 8 columns of pixels in the upper-left corner of the bitmap.  
  
 When an application selects a two-color DIB pattern brush into a monochrome device context, Windows ignores the colors specified in the DIB and instead displays the pattern brush using the current text and background colors of the device context. Pixels mapped to the first color (at offset 0 in the DIB color table) of the DIB are displayed using the text color. Pixels mapped to the second color (at offset 1 in the color table) are displayed using the background color.  
  
 For information about using the following Windows functions, see the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]:  
  
-   [CreateDIBPatternBrush](http://msdn.microsoft.com/library/windows/desktop/dd183492) (This function is provided only for compatibility with applications written for versions of Windows earlier than 3.0; use the **CreateDIBPatternBrushPt** function.)  
  
-   [CreateDIBPatternBrushPt](http://msdn.microsoft.com/library/windows/desktop/dd183493) (This function should be used for Win32-based applications.)  
  
-   [GlobalAlloc](http://msdn.microsoft.com/library/windows/desktop/aa366574)  
  
## Example  
 [!CODE [NVC_MFCDocView#23](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#23)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CBrush Class](../vs140/CBrush-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CBrush::CreatePatternBrush](../vs140/CBrush--CreatePatternBrush.md)   
 [CBrush::CreateBrushIndirect](../vs140/CBrush--CreateBrushIndirect.md)   
 [CBrush::CreateSolidBrush](../vs140/CBrush--CreateSolidBrush.md)   
 [CBrush::CreateHatchBrush](../vs140/CBrush--CreateHatchBrush.md)   
 [CGdiObject::CreateStockObject](../vs140/CGdiObject--CreateStockObject.md)   
 [CDC::SelectObject](../vs140/CDC--SelectObject.md)   
 [CGdiObject::DeleteObject](../vs140/CGdiObject--DeleteObject.md)   
 [CDC::GetBrushOrg](../vs140/CDC--GetBrushOrg.md)   
 [CDC::SetBrushOrg](../vs140/CDC--SetBrushOrg.md)