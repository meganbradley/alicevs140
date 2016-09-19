---
title: "BITMAPINFO Structure"
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
ms.topic: article
ms.assetid: a00caa49-e4df-419f-89a7-ab03c13a1b5b
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BITMAPINFO Structure
The `BITMAPINFO` structure defines the dimensions and color information for a Windows device-independent bitmap (DIB).  
  
## Syntax  
  
```  
typedef struct tagBITMAPINFO {  
   BITMAPINFOHEADER bmiHeader;  
   RGBQUAD bmiColors[1];  
} BITMAPINFO;  
```  
  
#### Parameters  
 `bmiHeader`  
 Specifies a [BITMAPINFOHEADER](http://msdn.microsoft.com/library/windows/desktop/dd183376) structure that contains information about the dimensions and color format of a device-independent bitmap.  
  
 `bmiColors`  
 Specifies an array of [RGBQUAD](http://msdn.microsoft.com/library/windows/desktop/dd162938) or `DWORD` data types that define the colors in the bitmap.  
  
## Remarks  
 A device-independent bitmap consists of two distinct parts: a `BITMAPINFO` structure that describes the dimensions and colors of the bitmap, and an array of bytes that specify the pixels in the bitmap. The bits in the array are packed together, but each scan line must be padded with zeros to end on a `LONG` boundary. If the height is positive, the origin of the bitmap is the lower-left corner. If the height is negative, the origin is the upper-left corner.  
  
 A *packed bitmap* is a bitmap where the byte array immediately follows the `BITMAPINFO` structure. Packed bitmaps are referenced by a single pointer.  
  
 For more information about the `BITMAPINFO` structure and appropriate values for members of the `BITMAPINFOHEADER` and `RGBQUAD` structures, see the following topics in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] documentation.  
  
-   [BITMAPINFO structure](http://msdn.microsoft.com/library/windows/desktop/dd183375)  
  
-   [BITMAPINFOHEADER](http://msdn.microsoft.com/library/windows/desktop/dd183376) structure  
  
-   [RGBQUAD](http://msdn.microsoft.com/library/windows/desktop/dd162938) structure  
  
## Requirements  
 **Header:** wingdi.h  
  
## See Also  
 [Structures, Styles, Callbacks, and Message Maps](../vs140/Structures--Styles--Callbacks--and-Message-Maps.md)   
 [CBrush::CreateDIBPatternBrush](../vs140/CBrush--CreateDIBPatternBrush.md)   
 [BITMAPINFOHEADER](http://msdn.microsoft.com/library/windows/desktop/dd183376)   
 [RGBQUAD](http://msdn.microsoft.com/library/windows/desktop/dd162938)