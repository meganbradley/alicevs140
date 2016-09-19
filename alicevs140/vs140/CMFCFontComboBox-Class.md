---
title: "CMFCFontComboBox Class"
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
ms.assetid: 9a53fb0c-7b45-486d-8187-2a4c723d9fbb
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCFontComboBox Class
The `CMFCFontComboBox` class creates a combo box control that contains a list of fonts.  
  
## Syntax  
  
```  
class CMFCFontComboBox : public CComboBox  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CMFCFontComboBox::CMFCFontComboBox](#cmfcfontcombobox__cmfcfontcombobox)|Constructs a `CMFCFontComboBox` object.|  
|`CMFCFontComboBox::~CMFCFontComboBox`|Destructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|`CMFCFontComboBox::CompareItem`|Called by the framework to determine the relative position of a new item in the sorted list box of the current font combo box control. (Overrides [CComboBox::CompareItem](../vs140/CComboBox-Class.md#ccombobox__compareitem).)|  
|`CMFCFontComboBox::DrawItem`|Called by the framework to draw a specified item in the current font combo box control. (Overrides [CComboBox::DrawItem](../vs140/CComboBox-Class.md#ccombobox__drawitem).)|  
|[CMFCFontComboBox::GetSelFont](#cmfcfontcombobox__getselfont)|Retrieves information about the currently selected font.|  
|`CMFCFontComboBox::MeasureItem`|Called by the framework to inform Windows of the dimensions of the list box in the current font combo box control. (Overrides [CComboBox::MeasureItem](../vs140/CComboBox-Class.md#ccombobox__measureitem).)|  
|`CMFCFontComboBox::PreTranslateMessage`|Translates window messages before they are dispatched to the                                         [TranslateMessage](http://msdn.microsoft.com/library/windows/desktop/ms644955) and                                         [DispatchMessage](http://msdn.microsoft.com/library/windows/desktop/ms644934) Windows functions. (Overrides [CWnd::PreTranslateMessage](../vs140/CWnd-Class.md#cwnd__pretranslatemessage).)|  
|[CMFCFontComboBox::SelectFont](#cmfcfontcombobox__selectfont)|Selects the font that matches the specified criteria from the font combo box.|  
|[CMFCFontComboBox::Setup](#cmfcfontcombobox__setup)|Initializes the list of items in the font combo box.|  
  
### Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CMFCFontComboBox::m_bDrawUsingFont](#cmfcfontcombobox__m_bdrawusingfont)|Indicates to the framework which font to use to draw the item labels in the current font combo box.|  
  
## Remarks  
 To use a `CMFCFontComboBox` object in a dialog box, add a `CMFCFontComboBox` variable to the dialog box class. Then in the `OnInitDialog` method of the dialog box class, call the [CMFCFontComboBox::Setup](#cmfcfontcombobox__setup) method to initialize the list of items in the combo box control.  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CCmdTarget](../vs140/CCmdTarget-Class.md)  
  
 [CWnd](../vs140/CWnd-Class.md)  
  
 [CComboBox](../vs140/CComboBox-Class.md)  
  
 [CMFCFontComboBox](../vs140/CMFCFontComboBox-Class.md)  
  
## Requirements  
 **Header:** afxfontcombobox.h  
  
##  <a name="cmfcfontcombobox__cmfcfontcombobox"></a>  CMFCFontComboBox::CMFCFontComboBox  
 Constructs a `CMFCFontComboBox` object.  
  
```  
CMFCFontComboBox();  
```  
  
### Return Value  
  
### Remarks  
  
##  <a name="cmfcfontcombobox__getselfont"></a>  CMFCFontComboBox::GetSelFont  
 Retrieves information about the currently selected font.  
  
```  
CMFCFontInfo* GetSelFont() const;  
```  
  
### Return Value  
 A pointer to [CMFCFontInfo](../vs140/CMFCFontInfo-Class.md) object that describes a font. It can be `NULL` if no font is selected in the combo box.  
  
### Remarks  
  
##  <a name="cmfcfontcombobox__m_bdrawusingfont"></a>  CMFCFontComboBox::m_bDrawUsingFont  
 Indicates to the framework which font to use to draw the item labels in the current font combo box.  
  
```  
static BOOL m_bDrawUsingFont;  
```  
  
### Remarks  
 Set this member to `TRUE` to direct the framework to use the same font to draw each item label. Set this member to `FALSE` to direct the framework to draw each item label with the font whose name is the same as the label. The default value of this member is `FALSE`.  
  
##  <a name="cmfcfontcombobox__selectfont"></a>  CMFCFontComboBox::SelectFont  
 Selects the font that matches the specified criteria from the font combo box.  
  
```  
BOOL SelectFont(  
   CMFCFontInfo* pDesc   
);  
BOOL SelectFont(  
   LPCTSTR lpszName,  
   BYTE nCharSet=DEFAULT_CHARSET   
);  
```  
  
### Parameters  
 [in] `pDesc`  
 Points to a font description object.  
  
 [in] `lpszName`  
 Specifies a font name.  
  
 [in] `nCharSet`  
 Specifies a character set. The default value is DEFAULT_CHARSET. For more information, see the `lfCharSet` member of the                                 [LOGFONT](http://msdn.microsoft.com/library/windows/desktop/dd145037) structure.  
  
### Return Value  
 `TRUE` if an item in the font combo box matches the specified font description object or font name and charset; otherwise, `FALSE`.  
  
### Remarks  
 Use this method to select and scroll to the item in the font combo box that corresponds to the specified font.  
  
### Example  
 The following example demonstrates how to use the `SelectFont` method in the `CMFCFontComboBox` class. This example is part of the [New Controls sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_NewControls#34](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_NewControls#34)]  
[!CODE [NVC_MFC_NewControls#35](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_NewControls#35)]  
  
##  <a name="cmfcfontcombobox__setup"></a>  CMFCFontComboBox::Setup  
 Initializes the list of items in the font combo box.  
  
```  
BOOL Setup(  
   int nFontType=DEVICE_FONTTYPE|RASTER_FONTTYPE|TRUETYPE_FONTTYPE,  
   BYTE nCharSet=DEFAULT_CHARSET,  
   BYTE nPitchAndFamily=DEFAULT_PITCH   
);  
```  
  
### Parameters  
 [in] `nFontType`  
 Specifies the font type. The default value is the bitwise combination (OR) of DEVICE_FONTTYPE, RASTER_FONTTYPE, and TRUETYPE_FONTTYPE.  
  
 [in] `nCharSet`  
 Specifies the font character set. The default value is DEFAULT_CHARSET.  
  
 [in] `nPitchAndFamily`  
 Specifies the font pitch and family. The default value is DEFAULT_PITCH.  
  
### Return Value  
 `TRUE` if the font combo box was initialized successfully; otherwise, `FALSE`.  
  
### Remarks  
 This method initializes the font combo box by enumerating the currently installed fonts that match the specified parameters and inserting those font names in the font combo box.  
  
### Example  
 The following example demonstrates how to use the `Setup` method in the `CMFCFontComboBox` class. This example is part of the [New Controls sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_NewControls#34](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_NewControls#34)]  
[!CODE [NVC_MFC_NewControls#36](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_NewControls#36)]  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Classes](../vs140/MFC-Classes.md)   
 [CMFCToolbarFontComboBox](../vs140/CMFCToolBarFontComboBox-Class.md)   
 [CMFCFontInfo](../vs140/CMFCFontInfo-Class.md)