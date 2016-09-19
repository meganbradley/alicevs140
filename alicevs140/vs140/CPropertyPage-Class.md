---
title: "CPropertyPage Class"
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
ms.assetid: d9000a21-aa81-4530-85d9-f43432afb4dc
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropertyPage Class
Represents individual pages of a property sheet, otherwise known as a tab dialog box.  
  
## Syntax  
  
```  
class CPropertyPage : public CDialog  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CPropertyPage::CPropertyPage](#cpropertypage__cpropertypage)|Constructs a `CPropertyPage` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CPropertyPage::CancelToClose](#cpropertypage__canceltoclose)|Changes the OK button to read Close, and disables the Cancel button, after an unrecoverable change in the page of a modal property sheet.|  
|[CPropertyPage::Construct](#cpropertypage__construct)|Constructs a `CPropertyPage` object. Use `Construct` if you want to specify your parameters at run time, or if you are using arrays.|  
|[CPropertyPage::GetPSP](#cpropertypage__getpsp)|Retrieves the Windows                                         [PROPSHEETPAGE](http://msdn.microsoft.com/library/windows/desktop/bb774548) structure associated with the `CPropertyPage` object.|  
|[CPropertyPage::OnApply](#cpropertypage__onapply)|Called by the framework when the Apply Now button is clicked.|  
|[CPropertyPage::OnCancel](#cpropertypage__oncancel)|Called by the framework when the Cancel button is clicked.|  
|[CPropertyPage::OnKillActive](#cpropertypage__onkillactive)|Called by the framework when the current page is no longer the active page. Perform data validation here.|  
|[CPropertyPage::OnOK](#cpropertypage__onok)|Called by the framework when the OK, Apply Now, or Close button is clicked.|  
|[CPropertyPage::OnQueryCancel](#cpropertypage__onquerycancel)|Called by the framework when the Cancel button is clicked, and before the cancel has taken place.|  
|[CPropertyPage::OnReset](#cpropertypage__onreset)|Called by the framework when the Cancel button is clicked.|  
|[CPropertyPage::OnSetActive](#cpropertypage__onsetactive)|Called by the framework when the page is made the active page.|  
|[CPropertyPage::OnWizardBack](#cpropertypage__onwizardback)|Called by the framework when the Back button is clicked while using a wizard-type property sheet.|  
|[CPropertyPage::OnWizardFinish](#cpropertypage__onwizardfinish)|Called by the framework when the Finish button is clicked while using a wizard-type property sheet.|  
|[CPropertyPage::OnWizardNext](#cpropertypage__onwizardnext)|Called by the framework when the Next button is clicked while using a wizard-type property sheet.|  
|[CPropertyPage::QuerySiblings](#cpropertypage__querysiblings)|Forwards the message to each page of the property sheet.|  
|[CPropertyPage::SetModified](#cpropertypage__setmodified)|Call to activate or deactivate the Apply Now button.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CPropertyPage::m_psp](#cpropertypage__m_psp)|The Windows                                         [PROPSHEETPAGE](http://msdn.microsoft.com/library/windows/desktop/bb774548) structure. Provides access to basic property page parameters.|  
  
## Remarks  
 As with standard dialog boxes, you derive a class from `CPropertyPage` for each page in your property sheet. To use `CPropertyPage`-derived objects, first create a [CPropertySheet](../vs140/CPropertySheet-Class.md) object, and then create an object for each page that goes in the property sheet. Call [CPropertySheet::AddPage](../vs140/CPropertySheet-Class.md#cpropertysheet__addpage) for each page in the sheet, and then display the property sheet by calling [CPropertySheet::DoModal](../vs140/CPropertySheet-Class.md#cpropertysheet__domodal) for a modal property sheet, or [CPropertySheet::Create](../vs140/CPropertySheet-Class.md#cpropertysheet__create) for a modeless property sheet.  
  
 You can create a type of tab dialog box called a wizard, which consists of a property sheet with a sequence of property pages that guide the user through the steps of an operation, such as setting up a device or creating a newsletter. In a wizard-type tab dialog box, the property pages do not have tabs, and only one property page is visible at a time. Also, instead of having OK and Apply Now buttons, a wizard-type tab dialog box has a Back button, a Next or Finish button, and a Cancel button.  
  
 For more information on establishing a property sheet as a wizard, see [CPropertySheet::SetWizardMode](../vs140/CPropertySheet-Class.md#cpropertysheet__setwizardmode). For more information on using `CPropertyPage` objects, see the article [Property Sheets and Property Pages](../vs140/Property-Sheets-and-Property-Pages-in-MFC.md).  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CCmdTarget](../vs140/CCmdTarget-Class.md)  
  
 [CWnd](../vs140/CWnd-Class.md)  
  
 [CDialog](../vs140/CDialog-Class.md)  
  
 `CPropertyPage`  
  
## Requirements  
 **Header:** afxdlgs.h  
  
##  <a name="cpropertypage__canceltoclose"></a>  CPropertyPage::CancelToClose  
 Call this function after an unrecoverable change has been made to the data in a page of a modal property sheet.  
  
```  
void CancelToClose( );  
  
```  
  
### Remarks  
 This function will change the OK button to Close and disable the Cancel button. This change alerts the user that a change is permanent and the modifications cannot be cancelled.  
  
 The `CancelToClose` member function does nothing in a modeless property sheet, because a modeless property sheet does not have a Cancel button by default.  
  
### Example  
  See the example for [CPropertyPage::QuerySiblings](#cpropertypage__querysiblings).  
  
##  <a name="cpropertypage__construct"></a>  CPropertyPage::Construct  
 Call this member function to construct a `CPropertyPage` object.  
  
```  
void Construct(    UINT  nIDTemplate ,    UINT  nIDCaption  = 0  ); void Construct(    LPCTSTR  lpszTemplateName ,    UINT  nIDCaption  = 0  ); void Construct(    UINT  nIDTemplate ,    UINT  nIDCaption ,    UINT  nIDHeaderTitle ,    UINT  nIDHeaderSubTitle  = 0  ); void Construct(    LPCTSTR  lpszTemplateName ,    UINT  nIDCaption ,    UINT  nIDHeaderTitle ,    UINT  nIDHeaderSubTitle  = 0  );  
  
```  
  
### Parameters  
 `nIDTemplate`  
 ID of the template used for this page.  
  
 `nIDCaption`  
 ID of the name to be placed in the tab for this page. If 0, the name will be taken from the dialog template for this page.  
  
 `lpszTemplateName`  
 Contains a null-terminated string that is the name of a template resource.  
  
 `nIDHeaderTitle`  
 ID of the name to be placed in the title location of the property page header. By default, 0.  
  
 `nIDHeaderSubTitle`  
 ID of the name to be placed in the subtitle location of the property page header. By default, 0.  
  
### Remarks  
 The object is displayed after all of the following conditions are met:  
  
-   The page has been added to a property sheet using [CPropertySheet::AddPage](../vs140/CPropertySheet-Class.md#cpropertysheet__addpage).  
  
-   The property sheet's [DoModal](../vs140/CPropertySheet-Class.md#cpropertysheet__domodal) or [Create](../vs140/CPropertySheet-Class.md#cpropertysheet__create) function has been called.  
  
-   The user has selected (tabbed to) this page.  
  
 Call **Construct** if one of the other class constructors has not been called. The `Construct` member function is flexible because you can leave the parameter statement blank and then specify multiple parameters and construction at any point in your code.  
  
 You must use `Construct` when you work with arrays, and you must call **Construct** for each member of the array so that the data members are assigned proper values.  
  
### Example  
 [!CODE [NVC_MFCDocView#112](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#112)]  
  
##  <a name="cpropertypage__cpropertypage"></a>  CPropertyPage::CPropertyPage  
 Constructs a `CPropertyPage` object.  
  
```  
CPropertyPage( ); explicit CPropertyPage(    UINT  nIDTemplate ,    UINT  nIDCaption  = 0,    DWORD  dwSize  = sizeof(PROPSHEETPAGE) ); explicit CPropertyPage(    LPCTSTR  lpszTemplateName ,    UINT  nIDCaption  = 0,    DWORD  dwSize  = sizeof(PROPSHEETPAGE) ); CPropertyPage(    UINT  nIDTemplate ,    UINT  nIDCaption ,    UINT  nIDHeaderTitle ,    UINT  nIDHeaderSubTitle  = 0,    DWORD  dwSize  = sizeof(PROPSHEETPAGE) ); CPropertyPage(    LPCTSTR  lpszTemplateName ,    UINT  nIDCaption ,    UINT  nIDHeaderTitle ,    UINT  nIDHeaderSubTitle  = 0,    DWORD  dwSize  = sizeof(PROPSHEETPAGE) );  
  
```  
  
### Parameters  
 `nIDTemplate`  
 ID of the template used for this page.  
  
 `nIDCaption`  
 ID of the name to be placed in the tab for this page. If 0, the name will be taken from the dialog template for this page.  
  
 `dwSize`  
 `lpszTemplateName`  
 Points to a string containing the name of the template for this page. Cannot be **NULL**.  
  
 `nIDHeaderTitle`  
 ID of the name to be placed in the title location of the property page header.  
  
 `nIDHeaderSubTitle`  
 ID of the name to be placed in the subtitle location of the property page header.  
  
### Remarks  
 The object is displayed after all of the following conditions are met:  
  
-   The page has been added to a property sheet using [CPropertySheet::AddPage](../vs140/CPropertySheet-Class.md#cpropertysheet__addpage).  
  
-   The property sheet's [DoModal](../vs140/CPropertySheet-Class.md#cpropertysheet__domodal) or [Create](../vs140/CPropertySheet-Class.md#cpropertysheet__create) function has been called.  
  
-   The user has selected (tabbed to) this page.  
  
 If you have multiple parameters (for example, if you are using an array), use [CPropertySheet::Construct](../vs140/CPropertySheet-Class.md#cpropertysheet__construct) instead of `CPropertyPage`.  
  
### Example  
 [!CODE [NVC_MFCDocView#113](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#113)]  
  
##  <a name="cpropertypage__getpsp"></a>  CPropertyPage::GetPSP  
 Retrieves the Windows                 [PROPSHEETPAGE](http://msdn.microsoft.com/library/windows/desktop/bb774548) structure associated with the `CPropertyPage` object.  
  
```  
const PROPSHEETPAGE & GetPSP( ) const; PROPSHEETPAGE & GetPSP( );  
  
```  
  
### Return Value  
 A reference to the **PROPSHEETPAGE** structure.  
  
##  <a name="cpropertypage__m_psp"></a>  CPropertyPage::m_psp  
 `m_psp` is a structure whose members store the characteristics of                 [PROPSHEETPAGE](http://msdn.microsoft.com/library/windows/desktop/bb774548).  
  
```  
PROPSHEETPAGE m_psp;  
  
```  
  
### Remarks  
 Use this structure to initialize the appearance of a property page after it is constructed.  
  
 For more information on this structure, including a listing of its members, see **PROPSHEETPAGE** in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
### Example  
 [!CODE [NVC_MFCDocView#128](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#128)]  
  
##  <a name="cpropertypage__onapply"></a>  CPropertyPage::OnApply  
 This member function is called by the framework when the user chooses the OK or the Apply Now button.  
  
```  
virtual BOOL OnApply( );  
  
```  
  
### Return Value  
 Nonzero if the changes are accepted; otherwise 0.  
  
### Remarks  
 When the framework calls this function, changes made on all property pages in the property sheet are accepted, the property sheet retains focus, and `OnApply` returns **TRUE** (the value 1). Before `OnApply` can be called by the framework, you must have called [SetModified](#cpropertypage__setmodified) and set its parameter to **TRUE**. This will activate the Apply Now button as soon as the user makes a change on the property page.  
  
 Override this member function to specify what action your program takes when the user clicks the Apply Now button. When overriding, the function should return **TRUE** to accept changes and **FALSE** to prevent changes from taking effect.  
  
 The default implementation of `OnApply` calls `OnOK`.  
  
 For more information about notification messages sent when the user presses the Apply Now or OK button in a property sheet, see                         [PSN_APPLY](http://msdn.microsoft.com/library/windows/desktop/bb774552) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
### Example  
  See the example for [CPropertyPage::OnOK](#cpropertypage__onok).  
  
##  <a name="cpropertypage__oncancel"></a>  CPropertyPage::OnCancel  
 This member function is called by the framework when the Cancel button is selected.  
  
```  
virtual void OnCancel( );  
  
```  
  
### Remarks  
 Override this member function to perform Cancel button actions. The default negates any changes that have been made.  
  
### Example  
 [!CODE [NVC_MFCDocView#114](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#114)]  
  
##  <a name="cpropertypage__onkillactive"></a>  CPropertyPage::OnKillActive  
 This member function is called by the framework when the page is no longer the active page.  
  
```  
virtual BOOL OnKillActive( );  
  
```  
  
### Return Value  
 Nonzero if data was updated successfully, otherwise 0.  
  
### Remarks  
 Override this member function to perform special data validation tasks.  
  
 The default implementation of this member function copies settings from the controls in the property page to the member variables of the property page. If the data was not updated successfully due to a dialog data validation (DDV) error, the page retains focus.  
  
 After this member function returns successfully, the framework will call the page's [OnOK](#cpropertypage__onok) function.  
  
### Example  
 [!CODE [NVC_MFCDocView#115](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#115)]  
  
##  <a name="cpropertypage__onok"></a>  CPropertyPage::OnOK  
 This member function is called by the framework when the user chooses either the OK or the Apply Now button, immediately after the framework calls [OnKillActive](#cpropertypage__onkillactive).  
  
```  
virtual void OnOK( );  
  
```  
  
### Remarks  
 When the user chooses either the OK or the Apply Now button, the framework receives the                         [PSN_APPLY](http://msdn.microsoft.com/library/windows/desktop/bb774552) notification from the property page. The call to `OnOK` won't be made if you call [CPropertySheet::PressButton](../vs140/CPropertySheet-Class.md#cpropertysheet__pressbutton) because the property page does not send the notification in that case.  
  
 Override this member function to implement additional behavior specific to the currently active page when user dismisses the entire property sheet.  
  
 The default implementation of this member function marks the page as "clean" to reflect that the data was updated in the `OnKillActive` function.  
  
### Example  
 [!CODE [NVC_MFCDocView#116](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#116)]  
  
##  <a name="cpropertypage__onquerycancel"></a>  CPropertyPage::OnQueryCancel  
 This member function is called by the framework when the user clicks the Cancel button and before the cancel action has taken place.  
  
```  
virtual BOOL OnQueryCancel( );  
  
```  
  
### Return Value  
 Returns **FALSE** to prevent the cancel operation or TRUE to allow it.  
  
### Remarks  
 Override this member function to specify an action the program takes when the user clicks the Cancel button.  
  
 The default implementation of `OnQueryCancel` returns **TRUE**.  
  
### Example  
 [!CODE [NVC_MFCDocView#117](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#117)]  
  
##  <a name="cpropertypage__onreset"></a>  CPropertyPage::OnReset  
 This member function is called by the framework when the user chooses the Cancel button.  
  
```  
virtual void OnReset( );  
  
```  
  
### Remarks  
 When the framework calls this function, changes to all property pages that were made by the user previously choosing the Apply Now button are discarded, and the property sheet retains focus.  
  
 Override this member function to specify what action the program takes when the user clicks the Cancel button.  
  
 The default implementation of `OnReset` does nothing.  
  
### Example  
  See the example for [CPropertyPage::OnCancel](#cpropertypage__oncancel).  
  
##  <a name="cpropertypage__onsetactive"></a>  CPropertyPage::OnSetActive  
 This member function is called by the framework when the page is chosen by the user and becomes the active page.  
  
```  
virtual BOOL OnSetActive( );  
  
```  
  
### Return Value  
 Nonzero if the page was successfully set active; otherwise 0.  
  
### Remarks  
 Override this member function to perform tasks when a page is activated. Your override of this member function would typically call the default version after updating data members, to allow it to update the page controls with the new data.  
  
 The default implementation creates the window for the page, if not previously created, and makes it the active page.  
  
### Example  
  See the example for [CPropertySheet::SetFinishText](../vs140/CPropertySheet-Class.md#cpropertysheet__setfinishtext).  
  
##  <a name="cpropertypage__onwizardback"></a>  CPropertyPage::OnWizardBack  
 This member function is called by the framework when the user clicks on the Back button in a wizard.  
  
```  
virtual LRESULT OnWizardBack();  
  
```  
  
### Return Value  
 0 to automatically advance to the next page; –1 to prevent the page from changing. To jump to a page other than the next one, return the identifier of the dialog to be displayed.  
  
### Remarks  
 Override this member function to specify some action the user must take when the Back button is pressed.  
  
 For more information on how to make a wizard-type property sheet, see [CPropertySheet::SetWizardMode](../vs140/CPropertySheet-Class.md#cpropertysheet__setwizardmode).  
  
### Example  
 [!CODE [NVC_MFCDocView#118](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#118)]  
  
##  <a name="cpropertypage__onwizardfinish"></a>  CPropertyPage::OnWizardFinish  
 This member function is called by the framework when the user clicks on the Finish button in a wizard.  
  
```  
virtual BOOL OnWizardFinish( );  
  
```  
  
### Return Value  
 Nonzero if the property sheet is destroyed when the wizard finishes; otherwise zero.  
  
### Remarks  
 When a user clicks the **Finish** button in a wizard, the framework calls this function; when `OnWizardFinish` returns **TRUE** (a nonzero value), the property sheet is able to be destroyed (but is not actually destroyed). Call `DestroyWindow` to destroy the property sheet. Do not call `DestroyWindow` from `OnWizardFinish`; doing so will cause heap corruption or other errors.  
  
 You can override this member function to specify some action the user must take when the Finish button is pressed. When overriding this function, return **FALSE** to prevent the property sheet from being destroyed.  
  
 For more information about notification messages sent when the user presses the Finish button in a wizard property sheet, see                         [PSN_WIZFINISH](http://msdn.microsoft.com/library/windows/desktop/bb774571) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 For more information on how to make a wizard-type property sheet, see [CPropertySheet::SetWizardMode](../vs140/CPropertySheet-Class.md#cpropertysheet__setwizardmode).  
  
### Example  
 [!CODE [NVC_MFCDocView#119](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#119)]  
  
 [!CODE [NVC_MFCDocView#120](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#120)]  
  
 [!CODE [NVC_MFCDocView#121](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#121)]  
  
 [!CODE [NVC_MFCDocView#122](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#122)]  
  
##  <a name="cpropertypage__onwizardnext"></a>  CPropertyPage::OnWizardNext  
 This member function is called by the framework when the user clicks on the Next button in a wizard.  
  
```  
virtual LRESULT OnWizardNext();  
  
```  
  
### Return Value  
 0 to automatically advance to the next page; –1 to prevent the page from changing. To jump to a page other than the next one, return the identifier of the dialog to be displayed.  
  
### Remarks  
 Override this member function to specify some action the user must take when the Next button is pressed.  
  
 For more information on how to make a wizard-type property sheet, see [CPropertySheet::SetWizardMode](../vs140/CPropertySheet-Class.md#cpropertysheet__setwizardmode).  
  
### Example  
 [!CODE [NVC_MFCDocView#123](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#123)]  
  
##  <a name="cpropertypage__querysiblings"></a>  CPropertyPage::QuerySiblings  
 Call this member function to forward a message to each page in the property sheet.  
  
```  
LRESULT QuerySiblings(    WPARAM  wParam ,    LPARAM  lParam );  
  
```  
  
### Parameters  
 `wParam`  
 Specifies additional message-dependent information.  
  
 `lParam`  
 Specifies additional message-dependent information  
  
### Return Value  
 The nonzero value from a page in the property sheet, or 0 if all pages return a value of 0.  
  
### Remarks  
 If a page returns a nonzero value, the property sheet does not send the message to subsequent pages.  
  
### Example  
 [!CODE [NVC_MFCDocView#124](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#124)]  
  
 [!CODE [NVC_MFCDocView#125](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#125)]  
  
 [!CODE [NVC_MFCDocView#126](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#126)]  
  
##  <a name="cpropertypage__setmodified"></a>  CPropertyPage::SetModified  
 Call this member function to enable or disable the Apply Now button, based on whether the settings in the property page should be applied to the appropriate external object.  
  
```  
void SetModified(    BOOL bChanged = TRUE );  
  
```  
  
### Parameters  
 `bChanged`  
 **TRUE** to indicate that the property page settings have been modified since the last time they were applied; **FALSE** to indicate that the property page settings have been applied, or should be ignored.  
  
### Remarks  
 The framework keeps track of which pages are "dirty," that is, property pages for which you have called **SetModified( TRUE )**. The Apply Now button will always be enabled if you call **SetModified( TRUE )** for one of the pages. The Apply Now button will be disabled when you call **SetModified( FALSE )** for one of the pages, but only if none of the other pages is "dirty."  
  
### Example  
 [!CODE [NVC_MFCDocView#127](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#127)]  
  
## See Also  
 [MFC Sample CMNCTRL1](../vs140/Visual-C---Samples.md)   
 [MFC Sample CMNCTRL2](../vs140/Visual-C---Samples.md)   
 [MFC Sample PROPDLG](../vs140/Visual-C---Samples.md)   
 [MFC Sample SNAPVW](../vs140/Visual-C---Samples.md)   
 [Base Class](../vs140/CDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPropertySheet](../vs140/CPropertySheet-Class.md)   
 [CDialog](../vs140/CDialog-Class.md)   
 [CPropertySheet::SetWizardMode](../vs140/CPropertySheet-Class.md#cpropertysheet__setwizardmode)