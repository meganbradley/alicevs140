---
title: "CColorDialog Class"
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
ms.assetid: d013dc25-9290-4b5d-a97e-95ad7208e13b
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CColorDialog Class
Allows you to incorporate a color-selection dialog box into your application.  
  
## Syntax  
  
```  
class CColorDialog : public CCommonDialog  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CColorDialog::CColorDialog](#ccolordialog__ccolordialog)|Constructs a `CColorDialog` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CColorDialog::DoModal](#ccolordialog__domodal)|Displays a color dialog box and allows the user to make a selection.|  
|[CColorDialog::GetColor](#ccolordialog__getcolor)|Returns a **COLORREF** structure containing the values of the selected color.|  
|[CColorDialog::GetSavedCustomColors](#ccolordialog__getsavedcustomcolors)|Retrieves custom colors created by the user.|  
|[CColorDialog::SetCurrentColor](#ccolordialog__setcurrentcolor)|Forces the current color selection to the specified color.|  
  
### Protected Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CColorDialog::OnColorOK](#ccolordialog__oncolorok)|Override to validate the color entered into the dialog box.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CColorDialog::m_cc](#ccolordialog__m_cc)|A structure used to customize the settings of the dialog box.|  
  
## Remarks  
 A `CColorDialog` object is a dialog box with a list of colors that are defined for the display system. The user can select or create a particular color from the list, which is then reported back to the application when the dialog box exits.  
  
 To construct a `CColorDialog` object, use the provided constructor or derive a new class and use your own custom constructor.  
  
 Once the dialog box has been constructed, you can set or modify any values in the [m_cc](#ccolordialog__m_cc) structure to initialize the values of the dialog box's controls. The `m_cc` structure is of type                 [CHOOSECOLOR](http://msdn.microsoft.com/library/windows/desktop/ms646830).  
  
 After initializing the dialog box's controls, call the `DoModal` member function to display the dialog box and allow the user to select a color. `DoModal` returns the user's selection of either the dialog box's OK ( **IDOK**) or Cancel ( **IDCANCEL**) button.  
  
 If `DoModal` returns **IDOK**, you can use one of `CColorDialog`'s member functions to retrieve the information input by the user.  
  
 You can use the Windows                 [CommDlgExtendedError](http://msdn.microsoft.com/library/windows/desktop/ms646916) function to determine whether an error occurred during initialization of the dialog box and to learn more about the error.  
  
 `CColorDialog` relies on the COMMDLG.DLL file that ships with Windows versions 3.1 and later.  
  
 To customize the dialog box, derive a class from `CColorDialog`, provide a custom dialog template, and add a message map to process the notification messages from the extended controls. Any unprocessed messages should be passed to the base class.  
  
 Customizing the hook function is not required.  
  
> [!NOTE]
>  On some installations the `CColorDialog` object will not display with a gray background if you have used the framework to make other `CDialog` objects gray.  
  
 For more information on using `CColorDialog`, see [Common Dialog Classes](../vs140/Common-Dialog-Classes.md)  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CCmdTarget](../vs140/CCmdTarget-Class.md)  
  
 [CWnd](../vs140/CWnd-Class.md)  
  
 [CDialog](../vs140/CDialog-Class.md)  
  
 [CCommonDialog](../vs140/CCommonDialog-Class.md)  
  
 `CColorDialog`  
  
## Requirements  
 **Header:** afxdlgs.h  
  
##  <a name="ccolordialog__ccolordialog"></a>  CColorDialog::CColorDialog  
 Constructs a `CColorDialog` object.  
  
```  
CColorDialog(    COLORREF clrInit = 0,    DWORD dwFlags = 0,    CWnd* pParentWnd = NULL );  
  
```  
  
### Parameters  
 *clrInit*  
 The default color selection. If no value is specified, the default is RGB(0,0,0) (black).  
  
 `dwFlags`  
 A set of flags that customize the function and appearance of the dialog box. For more information, see the                                 [CHOOSECOLOR](http://msdn.microsoft.com/library/windows/desktop/ms646830) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `pParentWnd`  
 A pointer to the dialog box's parent or owner window.  
  
### Example  
 [!CODE [NVC_MFCDocView#49](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#49)]  
  
##  <a name="ccolordialog__domodal"></a>  CColorDialog::DoModal  
 Call this function to display the Windows common color dialog box and allow the user to select a color.  
  
```  
virtual INT_PTR DoModal( );  
  
```  
  
### Return Value  
 **IDOK** or **IDCANCEL**. If **IDCANCEL** is returned, call the Windows                         [CommDlgExtendedError](http://msdn.microsoft.com/library/windows/desktop/ms646916) function to determine whether an error occurred.  
  
 **IDOK** and **IDCANCEL** are constants that indicate whether the user selected the OK or Cancel button.  
  
### Remarks  
 If you want to initialize the various color dialog-box options by setting members of the [m_cc](#ccolordialog__m_cc) structure, you should do this before calling `DoModal` but after the dialog-box object is constructed.  
  
 After calling `DoModal`, you can call other member functions to retrieve the settings or information input by the user into the dialog box.  
  
### Example  
  See the example for [CColorDialog::CColorDialog](#ccolordialog__ccolordialog).  
  
##  <a name="ccolordialog__getcolor"></a>  CColorDialog::GetColor  
 Call this function after calling `DoModal` to retrieve the information about the color the user selected.  
  
```  
COLORREF GetColor( ) const;  
  
```  
  
### Return Value  
 A                         [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) value that contains the RGB information for the color selected in the color dialog box.  
  
### Example  
 [!CODE [NVC_MFCDocView#50](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#50)]  
  
##  <a name="ccolordialog__getsavedcustomcolors"></a>  CColorDialog::GetSavedCustomColors  
 `CColorDialog` objects permit the user, in addition to choosing colors, to define up to 16 custom colors.  
  
```  
static COLORREF * PASCAL GetSavedCustomColors( );  
  
```  
  
### Return Value  
 A pointer to an array of 16 RGB color values that stores custom colors created by the user.  
  
### Remarks  
 The `GetSavedCustomColors` member function provides access to these colors. These colors can be retrieved after [DoModal](#ccolordialog__domodal) returns **IDOK**.  
  
 Each of the 16 RGB values in the returned array is initialized to RGB(255,255,255) (white). The custom colors chosen by the user are saved only between dialog box invocations within the application. If you wish to save these colors between invocations of the application, you must save them in some other manner, such as in an initialization (.INI) file.  
  
### Example  
 [!CODE [NVC_MFCDocView#51](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#51)]  
  
##  <a name="ccolordialog__m_cc"></a>  CColorDialog::m_cc  
 A structure of type                 [CHOOSECOLOR](http://msdn.microsoft.com/library/windows/desktop/ms646830), whose members store the characteristics and values of the dialog box.  
  
```  
CHOOSECOLOR m_cc;  
  
```  
  
### Remarks  
 After constructing a `CColorDialog` object, you can use `m_cc` to set various aspects of the dialog box before calling the [DoModal](#ccolordialog__domodal) member function.  
  
### Example  
 [!CODE [NVC_MFCDocView#53](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#53)]  
  
##  <a name="ccolordialog__oncolorok"></a>  CColorDialog::OnColorOK  
 Override to validate the color entered into the dialog box.  
  
```  
virtual BOOL OnColorOK( );  
  
```  
  
### Return Value  
 Nonzero if the dialog box should not be dismissed; otherwise 0 to accept the color that was entered.  
  
### Remarks  
 Override this function only if you want to provide custom validation of the color the user selects in the color dialog box.  
  
 The user can select a color by one of the following two methods:  
  
-   Clicking a color on the color palette. The selected color's RGB values are then reflected in the appropriate RGB edit boxes.  
  
-   Entering values in the RGB edit boxes  
  
 Overriding `OnColorOK` allows you to reject a color the user enters into a common color dialog box for any application-specific reason.  
  
 Normally, you do not need to use this function because the framework provides default validation of colors and displays a message box if an invalid color is entered.  
  
 You can call [SetCurrentColor](#ccolordialog__setcurrentcolor) from within `OnColorOK` to force a color selection. Once `OnColorOK` has been fired (that is, the user clicks **OK** to accept the color change), you can call [GetColor](#ccolordialog__getcolor) to get the RGB value of the new color.  
  
### Example  
 [!CODE [NVC_MFCDocView#52](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#52)]  
  
##  <a name="ccolordialog__setcurrentcolor"></a>  CColorDialog::SetCurrentColor  
 Call this function after calling `DoModal` to force the current color selection to the color value specified in `clr`.  
  
```  
void SetCurrentColor(    COLORREF clr );  
  
```  
  
### Parameters  
 `clr`  
 An RGB color value.  
  
### Remarks  
 This function is called from within a message handler or `OnColorOK`. The dialog box will automatically update the user's selection based on the value of the `clr` parameter.  
  
### Example  
  See the example for [CColorDialog::OnColorOK](#ccolordialog__oncolorok).  
  
## See Also  
 [MFC Sample MDI](../vs140/Visual-C---Samples.md)   
 [MFC Sample DRAWCLI](../vs140/Visual-C---Samples.md)   
 [Base Class](../vs140/CCommonDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)