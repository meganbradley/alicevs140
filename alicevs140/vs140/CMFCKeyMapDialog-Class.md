---
title: "CMFCKeyMapDialog Class"
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
ms.assetid: 5feb4942-d636-462d-a162-0104dd320f4e
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCKeyMapDialog Class
The `CMFCKeyMapDialog` class supports a control that maps commands to keys on the keyboard.  
  
## Syntax  
  
```  
class CMFCKeyMapDialog : public CDialogEx  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CMFCKeyMapDialog::CMFCKeyMapDlg](#cmfckeymapdialog__cmfckeymapdialog)|Constructs a `CMFCKeyMapDialog` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CMFCKeyMapDialog::DoModal](#cmfckeymapdialog__domodal)|Displays a keyboard mapping dialog box.|  
  
### Protected Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CMFCKeyMapDialog::FormatItem](#cmfckeymapdialog__formatitem)|Called by the framework to build a string that describes a key mapping. By default, the string contains the command name, the shortcut keys used, and the shortcut key description.|  
|[CMFCKeyMapDialog::GetCommandKeys](#cmfckeymapdialog__getcommandkeys)|Retrieves a string that contains a list of shortcut keys associated with the specified command.|  
|[CMFCKeyMapDialog::OnInsertItem](#cmfckeymapdialog__oninsertitem)|Called by the framework before a new item is inserted into the internal list control that supports the keyboard mapping control.|  
|[CMFCKeyMapDialog::OnPrintHeader](#cmfckeymapdialog__onprintheader)|Called by the framework to print the header for the keyboard map on a new page.|  
|[CMFCKeyMapDialog::OnPrintItem](#cmfckeymapdialog__onprintitem)|Called by the framework to print a keyboard mapping item.|  
|[CMFCKeyMapDialog::OnSetColumns](#cmfckeymapdialog__onsetcolumns)|Called by the framework to set captions for the columns in the internal list control that supports the keyboard mapping control.|  
|[CMFCKeyMapDialog::PrintKeyMap](#cmfckeymapdialog__printkeymap)|Called by the framework when a user clicks the **Print** button.|  
|[CMFCKeyMapDialog::SetColumnsWidth](#cmfckeymapdialog__setcolumnswidth)|Called by the framework to set the width of the columns in the internal list control that supports the keyboard mapping control.|  
  
## Remarks  
 Use the `CMFCKeyMapDialog` class to implement a resizable keyboard mapping dialog box. The dialog box uses a list view control to display keyboard shortcuts and their associated commands.  
  
 To use the `CMFCKeyMapDialog` class in an application, pass in a pointer to the main frame window as a parameter to the `CMFCKeyMapDialog` constructor. Then call the `DoModal` method to start a modal dialog box.  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CCmdTarget](../vs140/CCmdTarget-Class.md)  
  
 [CWnd](../vs140/CWnd-Class.md)  
  
 [CDialog](../vs140/CDialog-Class.md)  
  
 [CDialogEx](../vs140/CDialogEx-Class.md)  
  
 [CMFCKeyMapDialog](../vs140/CMFCKeyMapDialog-Class.md)  
  
## Requirements  
 **Header:** afxkeymapdialog.h  
  
##  <a name="cmfckeymapdialog__cmfckeymapdialog"></a>  CMFCKeyMapDialog::CMFCKeyMapDialog  
 Constructs a `CMFCKeyMapDialog` object.  
  
```  
CMFCKeyMapDialog(  
   CFrameWnd* pWndParentFrame,  
   BOOL bEnablePrint=FALSE   
);  
```  
  
### Parameters  
 [in] `pWndParentFrame`  
 A pointer to the parent window of the `CMFCKeyMapDialog` object.  
  
 [in] `bEnablePrint`  
 `TRUE` if the list of accelerator keys can be printed; otherwise, `FALSE`. The default is `FALSE`.  
  
### Remarks  
  
### Example  
 The following example demonstrates how to construct an object of the `CMFCKeyMapDialog` class. This example is part of the [Visual Studio Demo sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_VisualStudioDemo#21](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_VisualStudioDemo#21)]  
  
##  <a name="cmfckeymapdialog__domodal"></a>  CMFCKeyMapDialog::DoModal  
 Displays a keyboard mapping dialog box.  
  
```  
virtual INT_PTR DoModal();  
```  
  
### Return Value  
 A signed integer, such as `IDOK` or `IDCANCEL`, that is passed to the [CDialog::EndDialog](../vs140/CDialog-Class.md#cdialog__enddialog) method. The method, in turn, closes the dialog box. For more information, see [CDialog::DoModal](../vs140/CDialog-Class.md#cdialog__domodal).  
  
### Remarks  
 The keyboard mapping dialog box enables you to select and assign accelerator keys to various categories of commands. In addition, you can copy the selected accelerator keys and their description to the clipboard.  
  
##  <a name="cmfckeymapdialog__formatitem"></a>  CMFCKeyMapDialog::FormatItem  
 Called by the framework to build a string that describes a key mapping. By default, the string contains the command name, the shortcut keys used, and the shortcut key description.  
  
```  
virtual CString FormatItem(  
   int nItem   
) const;  
```  
  
### Parameters  
 [in] `nItem`  
 The zero-based index of an item in the internal list of key mappings.  
  
### Return Value  
 A `CString` object that contains the formatted item text.  
  
### Remarks  
  
##  <a name="cmfckeymapdialog__getcommandkeys"></a>  CMFCKeyMapDialog::GetCommandKeys  
 Retrieves a string value. The string contains a list of shortcut keys that are associated with a specified command.  
  
```  
virtual CString GetCommandKeys(  
   UINT uiCmdID   
) const;  
```  
  
### Parameters  
 [in] `uiCmdID`  
 A command ID.  
  
### Return Value  
 A semicolon-delimited (';') list of shortcut keys that is associated with the specified command.  
  
### Remarks  
  
##  <a name="cmfckeymapdialog__oninsertitem"></a>  CMFCKeyMapDialog::OnInsertItem  
 Called by the framework before a new item is inserted into an internal list control that supports the keyboard mapping control.  
  
```  
virtual void OnInsertItem(  
   CMFCToolBarButton* pButton,  
   int nItem   
);  
```  
  
### Parameters  
 [in] `pButton`  
 A pointer to a toolbar button that is used to map a keyboard key combination to a command name and description. The key map item is stored in an internal list control.  
  
 [in] `nItem`  
 A zero-based index that specifies where to insert the new key map item in the internal list control.  
  
### Remarks  
  
##  <a name="cmfckeymapdialog__onprintheader"></a>  CMFCKeyMapDialog::OnPrintHeader  
 Called by the framework to print the header for the keyboard map on a new page.  
  
```  
virtual int OnPrintHeader(  
   CDC& dc,  
   int nPage,  
   int cx   
) const;  
```  
  
### Parameters  
 [in] `dc`  
 The device context for the printer.  
  
 [in] `nPage`  
 The page number to print.  
  
 [in] `cx`  
 The horizontal offset of the header, in pixels.  
  
### Return Value  
 If successful, the height of the printed text. For more information, see the Return Value section of [CDC::DrawText](../vs140/CDC-Class.md#cdc__drawtext).  
  
### Remarks  
 The framework uses this method to print the keyboard map. By default, this method prints the page number, application name, and dialog box title.  
  
##  <a name="cmfckeymapdialog__onprintitem"></a>  CMFCKeyMapDialog::OnPrintItem  
 Called by the framework to print a keyboard mapping item.  
  
```  
virtual int OnPrintItem(  
   CDC& dc,  
   int nItem,  
   int y,  
   int cx,  
   BOOL bCalcHeight   
) const;  
```  
  
### Parameters  
 [in] `dc`  
 The device context of the printer.  
  
 [in] `nItem`  
 The zero-based index of the item to print.  
  
 [in] `y`  
 The vertical offset between the top of the page and the position of the item.  
  
 [in] `cx`  
 The horizontal offset between the left of the page and the position of the item.  
  
 [in] `bCalcHeight`  
 `TRUE` to calculate the best height for the print item; `FALSE` to truncate the print item so that it fits the default space.  
  
### Return Value  
 The height of the printed item.  
  
### Remarks  
 The framework calls this method to print a key map dialog box item. By default, this method prints the item's command name, shortcut keys, and command description.  
  
##  <a name="cmfckeymapdialog__onsetcolumns"></a>  CMFCKeyMapDialog::OnSetColumns  
 Called by the framework to set captions for the columns in the internal list control that supports the keyboard mapping control.  
  
```  
virtual void OnSetColumns();  
```  
  
### Remarks  
 By default, this method obtains the captions for the columns from three resources. The command column caption is from IDS_AFXBARRES_COMMAND, the key column caption is from IDS_AFXBARRES_KEYS, and the description column caption is from IDS_AFXBARRES_DESCRIPTION.  
  
##  <a name="cmfckeymapdialog__printkeymap"></a>  CMFCKeyMapDialog::PrintKeyMap  
 Called by the framework when a user clicks the **Print** button.  
  
```  
virtual void PrintKeyMap();  
```  
  
### Remarks  
 The `PrintKeyMap` method prints the key map. It initiates a new print job and then repeatedly calls the [CMFCKeyMapDialog::OnPrintHeader](#cmfckeymapdialog__onprintheader) and [CMFCKeyMapDialog::OnPrintItem](#cmfckeymapdialog__onprintitem) methods until all the key mappings are printed.  
  
##  <a name="cmfckeymapdialog__setcolumnswidth"></a>  CMFCKeyMapDialog::SetColumnsWidth  
 Called by the framework to set the width of the columns in the internal list control that supports the keyboard mapping control.  
  
```  
virtual void SetColumnsWidth();  
```  
  
### Remarks  
 This method sets the internal list control's columns to default widths. First, the width of the shortcut keys column is calculated. Then one-third of the remaining width is allocated to the command column and the remaining two-thirds is allocated to the description column.  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Classes](../vs140/MFC-Classes.md)   
 [CMFCKeyboardManager](../vs140/CKeyboardManager-Class.md)