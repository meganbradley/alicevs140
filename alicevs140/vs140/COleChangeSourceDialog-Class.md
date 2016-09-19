---
title: "COleChangeSourceDialog Class"
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
ms.assetid: d0e08be7-21ef-45e1-97af-fe27d99e3bac
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleChangeSourceDialog Class
Used for the OLE Change Source dialog box.  
  
## Syntax  
  
```  
class COleChangeSourceDialog : public COleDialog  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[COleChangeSourceDialog::COleChangeSourceDialog](#colechangesourcedialog__colechangesourcedialog)|Constructs a `COleChangeSourceDialog` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[COleChangeSourceDialog::DoModal](#colechangesourcedialog__domodal)|Displays the OLE Change Source dialog box.|  
|[COleChangeSourceDialog::GetDisplayName](#colechangesourcedialog__getdisplayname)|Gets the complete source display name.|  
|[COleChangeSourceDialog::GetFileName](#colechangesourcedialog__getfilename)|Gets the filename from the source name.|  
|[COleChangeSourceDialog::GetFromPrefix](#colechangesourcedialog__getfromprefix)|Gets the prefix of the previous source.|  
|[COleChangeSourceDialog::GetItemName](#colechangesourcedialog__getitemname)|Gets the item name from the source name.|  
|[COleChangeSourceDialog::GetToPrefix](#colechangesourcedialog__gettoprefix)|Gets the prefix of the new source|  
|[COleChangeSourceDialog::IsValidSource](#colechangesourcedialog__isvalidsource)|Indicates if the source is valid.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[COleChangeSourceDialog::m_cs](#colechangesourcedialog__m_cs)|A structure that controls the behavior of the dialog box.|  
  
## Remarks  
 Create an object of class `COleChangeSourceDialog` when you want to call this dialog box. After a `COleChangeSourceDialog` object has been constructed, you can use the [m_cs](#colechangesourcedialog__m_cs) structure to initialize the values or states of controls in the dialog box. The `m_cs` structure is of type                 [OLEUICHANGESOURCE](http://msdn.microsoft.com/library/windows/desktop/ms682160). For more information about using this dialog class, see the [DoModal](#colechangesourcedialog__domodal) member function.  
  
 For more information, see the                 [OLEUICHANGESOURCE](http://msdn.microsoft.com/library/windows/desktop/ms682160) structure in [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 For more information about OLE-specific dialog boxes, see the article [Dialog Boxes in OLE](../vs140/Dialog-Boxes-in-OLE.md).  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CCmdTarget](../vs140/CCmdTarget-Class.md)  
  
 [CWnd](../vs140/CWnd-Class.md)  
  
 [CDialog](../vs140/CDialog-Class.md)  
  
 [CCommonDialog](../vs140/CCommonDialog-Class.md)  
  
 [COleDialog](../vs140/COleDialog-Class.md)  
  
 `COleChangeSourceDialog`  
  
## Requirements  
 **Header:** afxodlgs.h  
  
##  <a name="colechangesourcedialog__colechangesourcedialog"></a>  COleChangeSourceDialog::COleChangeSourceDialog  
 This function constructs a `COleChangeSourceDialog` object.  
  
```  
explicit COleChangeSourceDialog(    COleClientItem*  pItem ,    CWnd*  pParentWnd  = NULL  );  
  
```  
  
### Parameters  
 `pItem`  
 Pointer to the linked [COleClientItem](../vs140/COleClientItem-Class.md) whose source is to be updated.  
  
 `pParentWnd`  
 Points to the parent or owner window object (of type `CWnd`) to which the dialog object belongs. If it is **NULL**, the parent window of the dialog box will be set to the main application window.  
  
### Remarks  
 To display the dialog box, call the [DoModal](#colechangesourcedialog__domodal) function.  
  
 For more information, see the                         [OLEUICHANGESOURCE](http://msdn.microsoft.com/library/windows/desktop/ms682160) structure and                         [OleUIChangeSource](http://msdn.microsoft.com/library/windows/desktop/ms682497) function in [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="colechangesourcedialog__domodal"></a>  COleChangeSourceDialog::DoModal  
 Call this function to display the OLE Change Source dialog box.  
  
```  
virtual INT_PTR DoModal( );  
  
```  
  
### Return Value  
 Completion status for the dialog box. One of the following values:  
  
-   **IDOK** if the dialog box was successfully displayed.  
  
-   **IDCANCEL** if the user canceled the dialog box.  
  
-   **IDABORT** if an error occurred. If **IDABORT** is returned, call the [COleDialog::GetLastError](../vs140/COleDialog-Class.md#coledialog__getlasterror) member function to get more information about the type of error that occurred. For a listing of possible errors, see the                                 [OleUIChangeSource](http://msdn.microsoft.com/library/windows/desktop/ms682497) function in [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
### Remarks  
 If you want to initialize the various dialog box controls by setting members of the [m_cs](#colechangesourcedialog__m_cs) structure, you should do this before calling `DoModal`, but after the dialog object is constructed.  
  
 If `DoModal` returns **IDOK**, you can call member functions to retrieve user-entered settings or information from the dialog box. The following list names typical query functions:  
  
-   [GetFileName](#colechangesourcedialog__getfilename)  
  
-   [GetDisplayName](#colechangesourcedialog__getdisplayname)  
  
-   [GetItemName](#colechangesourcedialog__getitemname)  
  
##  <a name="colechangesourcedialog__getdisplayname"></a>  COleChangeSourceDialog::GetDisplayName  
 Call this function to retrieve the complete display name for the linked client item.  
  
```  
CString GetDisplayName( );  
  
```  
  
### Return Value  
 The complete source display name (moniker) for the [COleClientItem](../vs140/COleClientItem-Class.md) specified in the constructor.  
  
##  <a name="colechangesourcedialog__getfilename"></a>  COleChangeSourceDialog::GetFileName  
 Call this function to retrieve the file moniker portion of the display name for the linked client item.  
  
```  
CString GetFileName( );  
  
```  
  
### Return Value  
 The file moniker portion of the source display name for the [COleClientItem](../vs140/COleClientItem-Class.md) specified in the constructor.  
  
### Remarks  
 The file moniker together with the item moniker gives the complete display name.  
  
##  <a name="colechangesourcedialog__getfromprefix"></a>  COleChangeSourceDialog::GetFromPrefix  
 Call this function to get the previous prefix string for the source.  
  
```  
CString GetFromPrefix( );  
  
```  
  
### Return Value  
 The previous prefix string of the source.  
  
### Remarks  
 Call this function only after [DoModal](#colechangesourcedialog__domodal) returns **IDOK**.  
  
 This value comes directly from the **lpszFrom** member of the                         [OLEUICHANGESOURCE](http://msdn.microsoft.com/library/windows/desktop/ms682160) structure.  
  
 For more information, see the                         [OLEUICHANGESOURCE](http://msdn.microsoft.com/library/windows/desktop/ms682160) structure in [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="colechangesourcedialog__getitemname"></a>  COleChangeSourceDialog::GetItemName  
 Call this function to retrieve the item moniker portion of the display name for the linked client item.  
  
```  
CString GetItemName( );  
  
```  
  
### Return Value  
 The item moniker portion of the source display name for the [COleClientItem](../vs140/COleClientItem-Class.md) specified in the constructor.  
  
### Remarks  
 The file moniker together with the item moniker gives the complete display name.  
  
##  <a name="colechangesourcedialog__gettoprefix"></a>  COleChangeSourceDialog::GetToPrefix  
 Call this function to get the new prefix string for the source.  
  
```  
CString GetToPrefix( );  
  
```  
  
### Return Value  
 The new prefix string of the source.  
  
### Remarks  
 Call this function only after [DoModal](#colechangesourcedialog__domodal) returns **IDOK**.  
  
 This value comes directly from the **lpszTo** member of the                         [OLEUICHANGESOURCE](http://msdn.microsoft.com/library/windows/desktop/ms682160) structure.  
  
 For more information, see the                         [OLEUICHANGESOURCE](http://msdn.microsoft.com/library/windows/desktop/ms682160) structure in [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="colechangesourcedialog__m_cs"></a>  COleChangeSourceDialog::m_cs  
 This data member is a structure of type                 [OLEUICHANGESOURCE](http://msdn.microsoft.com/library/windows/desktop/ms682160).  
  
```  
OLEUICHANGESOURCE m_cs;  
  
```  
  
### Remarks  
 `OLEUICHANGESOURCE` is used to control the behavior of the OLE Change Source dialog box. Members of this structure can be modified directly.  
  
 For more information, see the                         [OLEUICHANGESOURCE](http://msdn.microsoft.com/library/windows/desktop/ms682160) structure in [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="colechangesourcedialog__isvalidsource"></a>  COleChangeSourceDialog::IsValidSource  
 Call this function to determine if the new source is valid.  
  
```  
BOOL IsValidSource( );  
  
```  
  
### Return Value  
 Nonzero if the new source is valid, otherwise 0.  
  
### Remarks  
 Call this function only after [DoModal](#colechangesourcedialog__domodal) returns **IDOK**.  
  
 For more information, see the                         [OLEUICHANGESOURCE](http://msdn.microsoft.com/library/windows/desktop/ms682160) structure in [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## See Also  
 [Base Class](../vs140/COleDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDialog](../vs140/COleDialog-Class.md)