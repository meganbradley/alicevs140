---
title: "CImage::GetExporterFilterString"
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
ms.assetid: 9fe239dc-edf1-4e7f-89be-a7fca3ec2381
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImage::GetExporterFilterString
Finds image formats available for saving images.  
  
## Syntax  
  
```  
  
      static HRESULT GetExporterFilterString(  
   CSimpleString& strExporters,  
   CSimpleArray< GUID >& aguidFileTypes,  
   LPCTSTR pszAllFilesDescription = NULL,  
   DWORD dwExclude = excludeDefaultSave,  
   TCHAR chSeparator = _T( '|' )  
);  
```  
  
#### Parameters  
 *strExporters*  
 A reference to a **CSimpleString** object. See **Remarks** for more information.  
  
 `aguidFileTypes`  
 An array of GUIDs, with each element corresponding to one of the file types in the string. In the example in `pszAllFilesDescription` below, `aguidFileTypes`[0] is `GUID_NULL` and the remaining array values are the image file formats supported by the current operating system.  
  
> [!NOTE]
>  For a complete list of constants, see [Image File Format Constants](_gdiplus_constant_image_file_format_constants) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `pszAllFilesDescription`  
 If this parameter is not **NULL**, the filter string will have one additional filter at the beginning of the list. This filter will have the current value of `pszAllFilesDescription` for its description, and accepts files of any extension supported by any other exporter in the list.  
  
 For example:  
  
 [!CODE [NVC_ATLMFC_Utilities#73](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#73)]  
  
 `dwExclude`  
 Set of bit flags specifying which file types to exclude from the list. Allowable flags are:  
  
-   **excludeGIF** = 0x01   Excludes GIF files.  
  
-   **excludeBMP** = 0x02   Excludes BMP (Windows Bitmap) files.  
  
-   **excludeEMF** = 0x04   Excludes EMF (Enhanced Metafile) files.  
  
-   **excludeWMF** = 0x08   Excludes WMF (Windows Metafile) files.  
  
-   **excludeJPEG** = 0x10   Excludes JPEG files.  
  
-   **excludePNG** = 0x20   Excludes PNG files.  
  
-   **excludeTIFF** = 0x40   Excludes TIFF files.  
  
-   **excludeIcon** = 0x80   Excludes ICO (Windows Icon) files.  
  
-   **excludeOther** = 0x80000000   Excludes any other file type not listed above.  
  
-   **excludeDefaultLoad** = 0   For load, all file types are included by default  
  
-   **excludeDefaultSave** = **excludeIcon &#124; excludeEMF &#124; excludeWMF** For saving, these files are excluded by default because they usually have special requirements.  
  
 `chSeparator`  
 The separator used between the image formats. See **Remarks** for more information.  
  
## Return Value  
 A standard `HRESULT`.  
  
## Remarks  
 You can pass the resulting format string to your MFC [CFileDialog](../vs140/CFileDialog-Class.md) object to expose the file extensions of the available image formats in the File Save As dialog box.  
  
 The parameter *strExporter* has the format:  
  
 file description0&#124;\*.ext0&#124;filedescription1&#124;\*.ext1&#124;...file description*n*&#124;\*.ext*n*&#124;&#124;  
  
 where '&#124;' is the separator character specified by `chSeparator`. For example:  
  
 `"Bitmap format|*.bmp|JPEG format|*.jpg|GIF format|*.gif|PNG format|*.png||"`  
  
 Use the default separator '&#124;' if you pass this string to an MFC `CFileDialog` object. Use the null separator '\0' if you pass this string to a common File Save dialog box.  
  
## Requirements  
 **Header:** atlimage.h  
  
## See Also  
 [CImage Class](../vs140/CImage-Class.md)   
 [CImage::GetImporterFilterString](../vs140/CImage--GetImporterFilterString.md)   
 [CFileDialog::m_ofn](../vs140/CFileDialog--m_ofn.md)   
 [CFileDialog::GetFileExt](../vs140/CFileDialog--GetFileExt.md)   
 [OPENFILENAME](http://msdn.microsoft.com/library/windows/desktop/ms646839)   
 [CFileDialog::SetDefExt](../vs140/CFileDialog--SetDefExt.md)