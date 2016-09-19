---
title: "CMFCToolBarFontComboBox::CMFCToolBarFontComboBox"
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
ms.assetid: b51c8e4e-7569-4aa1-92f9-9379c478aae5
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarFontComboBox::CMFCToolBarFontComboBox
Constructs a [CMFCToolBarFontComboBox](../vs140/CMFCToolBarFontComboBox-Class.md) object.  
  
## Syntax  
  
```  
public:  
CMFCToolBarFontComboBox(  
   UINT uiID,  
   int iImage,  
   int nFontType = DEVICE_FONTTYPE | RASTER_FONTTYPE | TRUETYPE_FONTTYPE,  
   BYTE nCharSet = DEFAULT_CHARSET,  
   DWORD dwStyle = CBS_DROPDOWN,  
   int iWidth = 0,  
   BYTE nPitchAndFamily = DEFAULT_PITCH  
);   
protected:  
CMFCToolBarFontComboBox(  
   CObList* pLstFontsExternal,  
   int nFontType,  
   BYTE nCharSet,  
   BYTE nPitchAndFamily   
);  
CMFCToolBarFontComboBox();  
```  
  
#### Parameters  
 [in] `uiID`  
 The command ID of the combo box.  
  
 [in] `iImage`  
 The zero-based index of a toolbar image. The image is located in the [CMFCToolBarImages](../vs140/CMFCToolBarImages-Class.md) object that [CMFCToolBar](../Topic/CMFCToolBar%20Class.md) class maintains.  
  
 [in] `nFontType`  
 The types of fonts that the combo box contains. This parameter can be a combination (boolean OR) of the following values:  
  
 DEVICE_FONTTYPE  
  
 RASTER_FONTTYPE  
  
 TRUETYPE_FONTTYPE  
  
 [in] `nCharSet`  
 If set to DEFAULT_CHARSET, the combo box contains all uniquely-named fonts in all character sets. (If there are two fonts with the same name, the combo box contains one of them.) If set to a valid character set value, the combo box contains only fonts in the specified character set. See [LOGFONT](http://msdn.microsoft.com/library/windows/desktop/dd145037) for a listing of possible character sets.  
  
 [in] `dwStyle`  
 The style of the combo box. (see [Combo-Box Styles](../vs140/Combo-Box-Styles.md))  
  
 [in] `iWidth`  
 The width in pixels of the edit control.  
  
 [in] `nPitchAndFamily`  
 If set to DEFAULT_PITCH, the combo box contains fonts regardless of pitch. If set to FIXED_PITCH or VARIABLE_PITCH, the combo box contains only fonts with that pitch type. Filtering based on font family is not currently supported.  
  
 [out] `pLstFontsExternal`  
 Pointer to a [CObList](../vs140/CObList-Class.md) object that stores the available fonts.  
  
## Remarks  
 Usually, `CMFCToolBarFontComboBox` objects store the list of available fonts in a single shared `CObList` object. If you use the second overload of the constructor and provide a valid pointer to `pLstFontsExternal`, that `CMFCToolBarFontComboBox` object will instead fill the `CObList` that `pLstFontsExternal` points to with available fonts.  
  
## Example  
 The following example demonstrates how to construct a `CMFCToolBarFontComboBox` object. This code snippet is part of the [Word Pad sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_WordPad#7](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_WordPad#7)]  
  
## Requirements  
 **Header:** afxtoolbarfontcombobox.h  
  
## See Also  
 [CMFCToolBarFontComboBox Class](../vs140/CMFCToolBarFontComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)