---
title: "CFindReplaceDialog Class"
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
ms.assetid: 610f0b5d-b398-4ef6-8c05-e9d6641e50a8
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFindReplaceDialog Class
Allows you to implement standard string Find/Replace dialog boxes in your application.  
  
## Syntax  
  
```  
class CFindReplaceDialog : public CCommonDialog  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CFindReplaceDialog::CFindReplaceDialog](#cfindreplacedialog__cfindreplacedialog)|Call this function to construct a `CFindReplaceDialog` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CFindReplaceDialog::Create](#cfindreplacedialog__create)|Creates and displays a `CFindReplaceDialog` dialog box.|  
|[CFindReplaceDialog::FindNext](#cfindreplacedialog__findnext)|Call this function to determine whether the user wants to find the next occurrence of the find string.|  
|[CFindReplaceDialog::GetFindString](#cfindreplacedialog__getfindstring)|Call this function to retrieve the current find string.|  
|[CFindReplaceDialog::GetNotifier](#cfindreplacedialog__getnotifier)|Call this function to retrieve the **FINDREPLACE** structure in your registered message handler.|  
|[CFindReplaceDialog::GetReplaceString](#cfindreplacedialog__getreplacestring)|Call this function to retrieve the current replace string.|  
|[CFindReplaceDialog::IsTerminating](#cfindreplacedialog__isterminating)|Call this function to determine whether the dialog box is terminating.|  
|[CFindReplaceDialog::MatchCase](#cfindreplacedialog__matchcase)|Call this function to determine whether the user wants to match the case of the find string exactly.|  
|[CFindReplaceDialog::MatchWholeWord](#cfindreplacedialog__matchwholeword)|Call this function to determine whether the user wants to match entire words only.|  
|[CFindReplaceDialog::ReplaceAll](#cfindreplacedialog__replaceall)|Call this function to determine whether the user wants all occurrences of the string to be replaced.|  
|[CFindReplaceDialog::ReplaceCurrent](#cfindreplacedialog__replacecurrent)|Call this function to determine whether the user wants the current word to be replaced.|  
|[CFindReplaceDialog::SearchDown](#cfindreplacedialog__searchdown)|Call this function to determine whether the user wants the search to proceed in a downward direction.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CFindReplaceDialog::m_fr](#cfindreplacedialog__m_fr)|A structure used to customize a `CFindReplaceDialog` object.|  
  
## Remarks  
 Unlike the other Windows common dialog boxes, `CFindReplaceDialog` objects are modeless, allowing users to interact with other windows while they are on screen. There are two kinds of `CFindReplaceDialog` objects: Find dialog boxes and Find/Replace dialog boxes. Although the dialog boxes allow the user to input search and search/replace strings, they do not perform any of the searching or replacing functions. You must add these to the application.  
  
 To construct a `CFindReplaceDialog` object, use the provided constructor (which has no arguments). Since this is a modeless dialog box, allocate the object on the heap using the **new** operator, rather than on the stack.  
  
 Once a `CFindReplaceDialog` object has been constructed, you must call the [Create](#cfindreplacedialog__create) member function to create and display the dialog box.  
  
 Use the [m_fr](#cfindreplacedialog__m_fr) structure to initialize the dialog box before calling **Create**. The `m_fr` structure is of type                 [FINDREPLACE](http://msdn.microsoft.com/library/windows/desktop/ms646835). For more information on this structure, see the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 In order for the parent window to be notified of find/replace requests, you must use the Windows                 [RegisterWindowMessage](http://msdn.microsoft.com/library/windows/desktop/ms644947) function and use the [ON_REGISTERED_MESSAGE](../vs140/ON_REGISTERED_MESSAGE.md) message-map macro in your frame window that handles this registered message.  
  
 You can determine whether the user has decided to terminate the dialog box with the `IsTerminating` member function.  
  
 `CFindReplaceDialog` relies on the COMMDLG.DLL file that ships with Windows versions 3.1 and later.  
  
 To customize the dialog box, derive a class from `CFindReplaceDialog`, provide a custom dialog template, and add a message map to process the notification messages from the extended controls. Any unprocessed messages should be passed to the base class.  
  
 Customizing the hook function is not required.  
  
 For more information on using `CFindReplaceDialog`, see [Common Dialog Classes](../vs140/Common-Dialog-Classes.md).  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CCmdTarget](../vs140/CCmdTarget-Class.md)  
  
 [CWnd](../vs140/CWnd-Class.md)  
  
 [CDialog](../vs140/CDialog-Class.md)  
  
 [CCommonDialog](../vs140/CCommonDialog-Class.md)  
  
 `CFindReplaceDialog`  
  
## Requirements  
 **Header:** afxdlgs.h  
  
##  <a name="cfindreplacedialog__cfindreplacedialog"></a>  CFindReplaceDialog::CFindReplaceDialog  
 Constructs a `CFindReplaceDialog` object.  
  
```  
CFindReplaceDialog();  
  
```  
  
### Remarks  
 Because the `CFindReplaceDialog` object is a modeless dialog box, you must construct it on the heap by using the `new` operator.  
  
 During destruction, the framework tries to perform a `delete this` on the pointer to the dialog box. If you created the dialog box on the stack, the `this` pointer does not exist and undefined behavior may result.  
  
 For more information on the construction of `CFindReplaceDialog` objects, see the [CFindReplaceDialog](../vs140/CFindReplaceDialog-Class.md) overview. Use the [Create](#cfindreplacedialog__create) member function to display the dialog box.  
  
### Example  
 [!CODE [NVC_MFCDocView#170](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#170)]  
  
##  <a name="cfindreplacedialog__create"></a>  CFindReplaceDialog::Create  
 Creates and displays either a Find or Find/Replace dialog box object, depending on the value of `bFindDialogOnly`.  
  
```  
virtual BOOL Create(    BOOL bFindDialogOnly ,    LPCTSTR lpszFindWhat ,    LPCTSTR lpszReplaceWith = NULL,    DWORD dwFlags = FR_DOWN,    CWnd* pParentWnd = NULL );  
  
```  
  
### Parameters  
 `bFindDialogOnly`  
 Set this parameter to `TRUE` to display a **Find** dialog box. Set it to `FALSE` to display a **Find/Replace** dialog box.  
  
 `lpszFindWhat`  
 Pointer to the default search string when the dialog box appears. If `NULL`, the dialog box does not contain a default search string.  
  
 `lpszReplaceWith`  
 Pointer to the default replacement string when the dialog box appears. If `NULL`, the dialog box does not contain a default replacement string.  
  
 `dwFlags`  
 One or more flags you can use to customize the settings of the dialog box, combined using the bitwise OR operator. The default value is `FR_DOWN`, which specifies that the search is to proceed in a downward direction. See the                                 [FINDREPLACE](http://msdn.microsoft.com/library/windows/desktop/ms646835) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for more information on these flags.  
  
 `pParentWnd`  
 A pointer to the dialog box's parent or owner window. This is the window that will receive the special message indicating that a find/replace action is requested. If `NULL`, the main window of the application is used.  
  
### Return Value  
 Nonzero if the dialog box object was successfully created; otherwise 0.  
  
### Remarks  
 In order for the parent window to be notified of find/replace requests, you must use the Windows                         [RegisterWindowMessage](http://msdn.microsoft.com/library/windows/desktop/ms644947) function whose return value is a message number unique to the application's instance. Your frame window should have a message map entry that declares the callback function ( `OnFindReplace` in the example that follows) that handles this registered message. The following code fragment is an example of how to do this for a frame window class named `CMyRichEditView`:  
  
 [!CODE [NVC_MFCDocView#171](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#171)]  
  
 [!CODE [NVC_MFCDocView#172](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#172)]  
  
 [!CODE [NVC_MFCDocView#173](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#173)]  
  
 Within your `OnFindReplace` function, you interpret the intentions of the user by using the [FindNext](#cfindreplacedialog__findnext) and [IsTerminating](#cfindreplacedialog__isterminating) methods and you create the code for the find/replace operations.  
  
### Example  
  See the example for [CFindReplaceDialog::CFindReplaceDialog](#cfindreplacedialog__cfindreplacedialog).  
  
##  <a name="cfindreplacedialog__findnext"></a>  CFindReplaceDialog::FindNext  
 Call this function from your callback function to determine whether the user wants to find the next occurrence of the search string.  
  
```  
BOOL FindNext( ) const;  
  
```  
  
### Return Value  
 Nonzero if the user wants to find the next occurrence of the search string; otherwise 0.  
  
##  <a name="cfindreplacedialog__getfindstring"></a>  CFindReplaceDialog::GetFindString  
 Call this function from your callback function to retrieve the default string to find.  
  
```  
CString GetFindString( ) const;  
  
```  
  
### Return Value  
 The default string to find.  
  
### Example  
 [!CODE [NVC_MFCDocView#69](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#69)]  
  
##  <a name="cfindreplacedialog__getnotifier"></a>  CFindReplaceDialog::GetNotifier  
 Call this function to retrieve a pointer to the current Find Replace dialog box.  
  
```  
static CFindReplaceDialog* PASCAL GetNotifier(    LPARAM lParam );  
  
```  
  
### Parameters  
 `lParam`  
 The **lparam** value passed to the frame window's **OnFindReplace** member function.  
  
### Return Value  
 A pointer to the current dialog box.  
  
### Remarks  
 It should be used within your callback function to access the current dialog box, call its member functions, and access the `m_fr` structure.  
  
### Example  
 See [CFindReplaceDialog::Create](#cfindreplacedialog__create) for an example of how to register the OnFindReplace handler to receive notifications from the Find Replace dialog box.  
  
 [!CODE [NVC_MFCDocView#69](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#69)]  
  
##  <a name="cfindreplacedialog__getreplacestring"></a>  CFindReplaceDialog::GetReplaceString  
 Call this function to retrieve the current replace string.  
  
```  
CString GetReplaceString( ) const;  
  
```  
  
### Return Value  
 The default string with which to replace found strings.  
  
### Example  
  See the example for [CFindReplaceDialog::GetFindString](#cfindreplacedialog__getfindstring).  
  
##  <a name="cfindreplacedialog__isterminating"></a>  CFindReplaceDialog::IsTerminating  
 Call this function within your callback function to determine whether the user has decided to terminate the dialog box.  
  
```  
BOOL IsTerminating( ) const;  
  
```  
  
### Return Value  
 Nonzero if the user has decided to terminate the dialog box; otherwise 0.  
  
### Remarks  
 If this function returns nonzero, you should call the `DestroyWindow` member function of the current dialog box and set any dialog box pointer variable to **NULL**. Optionally, you can also store the find/replace text last entered and use it to initialize the next find/replace dialog box.  
  
### Example  
  See the example for [CFindReplaceDialog::GetFindString](#cfindreplacedialog__getfindstring).  
  
##  <a name="cfindreplacedialog__m_fr"></a>  CFindReplaceDialog::m_fr  
 Used to customize a `CFindReplaceDialog` object.  
  
```  
FINDREPLACE m_fr;  
  
```  
  
### Remarks  
 `m_fr` is a structure of type                         [FINDREPLACE](http://msdn.microsoft.com/library/windows/desktop/ms646835). Its members store the characteristics of the dialog-box object. After constructing a `CFindReplaceDialog` object, you can use `m_fr` to modify various values in the dialog box.  
  
 For more information on this structure, see the **FINDREPLACE** structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
### Example  
  See the example for [CFindReplaceDialog::CFindReplaceDialog](#cfindreplacedialog__cfindreplacedialog).  
  
##  <a name="cfindreplacedialog__matchcase"></a>  CFindReplaceDialog::MatchCase  
 Call this function to determine whether the user wants to match the case of the find string exactly.  
  
```  
BOOL MatchCase( ) const;  
  
```  
  
### Return Value  
 Nonzero if the user wants to find occurrences of the search string that exactly match the case of the search string; otherwise 0.  
  
##  <a name="cfindreplacedialog__matchwholeword"></a>  CFindReplaceDialog::MatchWholeWord  
 Call this function to determine whether the user wants to match entire words only.  
  
```  
BOOL MatchWholeWord( ) const;  
  
```  
  
### Return Value  
 Nonzero if the user wants to match only the entire words of the search string; otherwise 0.  
  
##  <a name="cfindreplacedialog__replaceall"></a>  CFindReplaceDialog::ReplaceAll  
 Call this function to determine whether the user wants all occurrences of the string to be replaced.  
  
```  
BOOL ReplaceAll( ) const;  
  
```  
  
### Return Value  
 Nonzero if the user has requested that all strings matching the replace string be replaced; otherwise 0.  
  
##  <a name="cfindreplacedialog__replacecurrent"></a>  CFindReplaceDialog::ReplaceCurrent  
 Call this function to determine whether the user wants the current word to be replaced.  
  
```  
BOOL ReplaceCurrent( ) const;  
  
```  
  
### Return Value  
 Nonzero if the user has requested that the currently selected string be replaced with the replace string; otherwise 0.  
  
##  <a name="cfindreplacedialog__searchdown"></a>  CFindReplaceDialog::SearchDown  
 Call this function to determine whether the user wants the search to proceed in a downward direction.  
  
```  
BOOL SearchDown( ) const;  
  
```  
  
### Return Value  
 Nonzero if the user wants the search to proceed in a downward direction; 0 if the user wants the search to proceed in an upward direction.  
  
## See Also  
 [Base Class](../vs140/CCommonDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)