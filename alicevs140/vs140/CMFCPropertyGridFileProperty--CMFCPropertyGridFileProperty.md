---
title: "CMFCPropertyGridFileProperty::CMFCPropertyGridFileProperty"
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
ms.assetid: 634445d5-97c5-485d-acef-9bcce8b628cd
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridFileProperty::CMFCPropertyGridFileProperty
Constructs a `CMFCPropertyGridFileProperty` object.  
  
## Syntax  
  
```  
CMFCPropertyGridFileProperty(  
   const CString& strName,  
   BOOL bOpenFileDialog,  
   const CString& strFileName,  
   LPCTSTR lpszDefExt=NULL,  
   DWORD dwFlags=OFN_HIDEREADONLY|OFN_OVERWRITEPROMPT,  
   LPCTSTR lpszFilter=NULL,  
   LPCTSTR lpszDescr=NULL,  
   DWORD_PTR dwData=0   
);  
```  
  
#### Parameters  
 [in] `strName`  
 The property name.  
  
 [in] `bOpenFileDialog`  
 `TRUE` to open an **Open File**dialog box; `FALSE` to open a **Save File** dialog box.  
  
 [in] `strFileName`  
 The initial file name.  
  
 [in] `lpszDefExt`  
 A string of one or more file name extensions. The default value is `NULL`.  
  
 [in] `dwFlags`  
 Dialog box flags. The default value is a bitwise combination (OR) of `OFN_HIDEREADONLY` and `OFN_OVERWRITEPROMPT`.  
  
 [in] `lpszFilter`  
 A string of one or more file filters. The default value is `NULL`.  
  
 [in] `lpszDescr`  
 The property item description. The default value is `NULL`.  
  
 [in] `dwData`  
 Application-specific data that is associated with the property item. For example, a 32-bit integer or a pointer to other data. The default value is 0.  
  
## Return Value  
  
## Remarks  
 For a full list of available flags, see [OPENFILENAME structure](https://msdn.microsoft.com/library/ms646839.aspx).  
  
## Example  
 The following example demonstrates how to create an object using the constructor of the `CMFCPropertyGridFileProperty` class. This example is part of the [Visual Studio Demo sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_VisualStudioDemo#22](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_VisualStudioDemo#22)]  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridFileProperty Class](../vs140/CMFCPropertyGridFileProperty-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)