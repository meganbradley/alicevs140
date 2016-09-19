---
title: "COlePasteSpecialDialog::AddFormat"
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
ms.assetid: 3e7c6ce7-5e30-43d2-a118-914e69d36c14
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COlePasteSpecialDialog::AddFormat
Call this function to add new formats to the list of formats your application can support in a Paste Special operation.  
  
## Syntax  
  
```  
  
      void AddFormat(  
   const FORMATETC& formatEtc,  
   LPTSTR lpszFormat,  
   LPTSTR lpszResult,  
   DWORD flags   
);  
void AddFormat(  
   UINT cf,  
   DWORD tymed,  
   UINT nFormatID,  
   BOOL bEnableIcon,  
   BOOL bLink   
);  
```  
  
#### Parameters  
 *fmt*  
 Reference to the data type to add.  
  
 `lpszFormat`  
 String that describes the format to the user.  
  
 *lpszResult*  
 String that describes the result if this format is chosen in the dialog box.  
  
 `flags`  
 The different linking and embedding options available for this format. This flag is a bitwise combination of one or more of the different values in the **OLEUIPASTEFLAG** enumerated type.  
  
 `cf`  
 The clipboard format to add.  
  
 *tymed*  
 The types of media available in this format. This is a bitwise combination of one or more of the values in the **TYMED** enumerated type.  
  
 `nFormatID`  
 The ID of the string that identifies this format. The format of this string is two separate strings separated by a '\n' character. The first string is the same that would be passed in the *lpstrFormat* parameter, and the second is the same as the *lpstrResult* parameter.  
  
 *bEnableIcon*  
 Flag that determines whether the Display As Icon check box is enabled when this format is chosen in the list box.  
  
 *bLink*  
 Flag that determines whether the Paste Link radio button is enabled when this format is chosen in the list box.  
  
## Remarks  
 This function can be called to add either standard formats such as **CF_TEXT** or **CF_TIFF** or custom formats that your application has registered with the system. For more information about pasting data objects into your application, see the article [Data Objects and Data Sources: Manipulation](../vs140/Data-Objects-and-Data-Sources--Manipulation.md).  
  
 For more information, see the [TYMED](http://msdn.microsoft.com/library/windows/desktop/ms691227) enumeration type and the [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 For more information, see the [OLEUIPASTEFLAG](http://msdn.microsoft.com/library/windows/desktop/ms682172) enumerated type in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COlePasteSpecialDialog Class](../vs140/COlePasteSpecialDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COlePasteSpecialDialog::AddStandardFormats](../vs140/COlePasteSpecialDialog--AddStandardFormats.md)