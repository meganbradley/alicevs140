---
title: "CImage::Save"
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
ms.assetid: 48442b7f-e897-49bd-95a1-a4c4b465582c
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImage::Save
Saves an image to the specified stream or file on disk.  
  
## Syntax  
  
```  
  
      HRESULT Save(  
   IStream* pStream,  
   REFGUID guidFileType  
) const throw();  
HRESULT Save(  
   LPCTSTR pszFileName,  
   REFGUID guidFileType= GUID_NULL  
) const throw();  
```  
  
#### Parameters  
 `pStream`  
 A pointer to a COM IStream object containing the file image data.  
  
 *pszFileName*  
 A pointer to the file name for the image.  
  
 `guidFileType`  
 The file type to save the image as. Can be one of the following:  
  
-   **ImageFormatBMP** An uncompressed bitmap image.  
  
-   **ImageFormatPNG** A Portable Network Graphic (PNG) compressed image.  
  
-   **ImageFormatJPEG** A JPEG compressed image.  
  
-   **ImageFormatGIF** A GIF compressed image.  
  
> [!NOTE]
>  For a complete list of constants, see [Image File Format Constants](_gdiplus_constant_image_file_format_constants) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 A standard `HRESULT`.  
  
## Remarks  
 Call this function to save the image using a specified name and type. If the `guidFileType` parameter is not included, the file name's file extension will be used to determine the image format. If no extension is provided, the image will be saved in BMP format.  
  
## Example:  
 [!CODE [NVC_ATLMFC_Utilities#72](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#72)]  
  
## Requirements  
 **Header:** atlimage.h  
  
## See Also  
 [CImage Class](../vs140/CImage-Class.md)   
 [CImage::Load](../vs140/CImage--Load.md)