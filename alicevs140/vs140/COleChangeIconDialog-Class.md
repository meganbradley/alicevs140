---
title: "COleChangeIconDialog Class"
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
ms.assetid: 8d6e131b-ddbb-4dff-a432-f239efda8e3d
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleChangeIconDialog Class
Used for the OLE Change Icon dialog box.  
  
## Syntax  
  
```  
class COleChangeIconDialog : public COleDialog  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[COleChangeIconDialog::COleChangeIconDialog](#colechangeicondialog__colechangeicondialog)|Constructs a `COleChangeIconDialog` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[COleChangeIconDialog::DoChangeIcon](#colechangeicondialog__dochangeicon)|Performs the change specified in the dialog box.|  
|[COleChangeIconDialog::DoModal](#colechangeicondialog__domodal)|Displays the OLE 2 Change Icon dialog box.|  
|[COleChangeIconDialog::GetIconicMetafile](#colechangeicondialog__geticonicmetafile)|Gets a handle to the metafile associated with the iconic form of this item.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[COleChangeIconDialog::m_ci](#colechangeicondialog__m_ci)|A structure that controls the behavior of the dialog box.|  
  
## Remarks  
 Create an object of class `COleChangeIconDialog` when you want to call this dialog box. After a `COleChangeIconDialog` object has been constructed, you can use the [m_ci](#colechangeicondialog__m_ci) structure to initialize the values or states of controls in the dialog box. The `m_ci` structure is of type **OLEUICHANGEICON**. For more information about using this dialog class, see the [DoModal](#colechangeicondialog__domodal) member function.  
  
 For more information, see the                 [OLEUICHANGEICON](http://msdn.microsoft.com/library/windows/desktop/ms680098) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 For more information about OLE-specific dialog boxes, see the article [Dialog Boxes in OLE](../vs140/Dialog-Boxes-in-OLE.md).  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CCmdTarget](../vs140/CCmdTarget-Class.md)  
  
 [CWnd](../vs140/CWnd-Class.md)  
  
 [CDialog](../vs140/CDialog-Class.md)  
  
 [CCommonDialog](../vs140/CCommonDialog-Class.md)  
  
 [COleDialog](../vs140/COleDialog-Class.md)  
  
 `COleChangeIconDialog`  
  
## Requirements  
 **Header:** afxodlgs.h  
  
##  <a name="colechangeicondialog__colechangeicondialog"></a>  COleChangeIconDialog::COleChangeIconDialog  
 This function constructs only a `COleChangeIconDialog` object.  
  
```  
explicit COleChangeIconDialog(    COleClientItem*  pItem ,    DWORD  dwFlags  = CIF_SELECTCURRENT,    CWnd*  pParentWnd  = NULL  );  
  
```  
  
### Parameters  
 `pItem`  
 Points to the item to be converted.  
  
 `dwFlags`  
 Creation flag, which contains any number of the following values combined using the bitwise-or operator:  
  
-   **CIF_SELECTCURRENT** Specifies that the Current radio button will be selected initially when the dialog box is called. This is the default.  
  
-   **CIF_SELECTDEFAULT** Specifies that the Default radio button will be selected initially when the dialog box is called.  
  
-   **CIF_SELECTFROMFILE** Specifies that the From File radio button will be selected initially when the dialog box is called.  
  
-   **CIF_SHOWHELP** Specifies that the Help button will be displayed when the dialog box is called.  
  
-   **CIF_USEICONEXE** Specifies that the icon should be extracted from the executable specified in the **szIconExe** field of [m_ci](#colechangeicondialog__m_ci) instead of retrieved from the type. This is useful for embedding or linking to non-OLE files.  
  
 `pParentWnd`  
 Points to the parent or owner window object (of type `CWnd`) to which the dialog object belongs. If it is **NULL**, the parent window of the dialog box will be set to the main application window.  
  
### Remarks  
 To display the dialog box, call the [DoModal](#colechangeicondialog__domodal) function.  
  
 For more information, see the                         [OLEUICHANGEICON](http://msdn.microsoft.com/library/windows/desktop/ms680098) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
##  <a name="colechangeicondialog__dochangeicon"></a>  COleChangeIconDialog::DoChangeIcon  
 Call this function to change the icon representing the item to the one selected in the dialog box after [DoModal](#colechangeicondialog__domodal) returns **IDOK**.  
  
```  
BOOL DoChangeIcon(    COleClientItem* pItem );  
  
```  
  
### Parameters  
 `pItem`  
 Points to the item whose icon is changing.  
  
### Return Value  
 Nonzero if change is successful; otherwise 0.  
  
##  <a name="colechangeicondialog__domodal"></a>  COleChangeIconDialog::DoModal  
 Call this function to display the OLE Change Icon dialog box.  
  
```  
virtual INT_PTR DoModal( );  
  
```  
  
### Return Value  
 Completion status for the dialog box. One of the following values:  
  
-   **IDOK** if the dialog box was successfully displayed.  
  
-   **IDCANCEL** if the user canceled the dialog box.  
  
-   **IDABORT** if an error occurred. If **IDABORT** is returned, call the `COleDialog::GetLastError` member function to get more information about the type of error that occurred. For a listing of possible errors, see the                                 [OleUIChangeIcon](http://msdn.microsoft.com/library/windows/desktop/ms688307) function in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
### Remarks  
 If you want to initialize the various dialog box controls by setting members of the [m_ci](#colechangeicondialog__m_ci) structure, you should do this before calling `DoModal`, but after the dialog object is constructed.  
  
 If `DoModal` returns **IDOK**, you can call other member functions to retrieve the settings or information that was input by the user into the dialog box.  
  
##  <a name="colechangeicondialog__geticonicmetafile"></a>  COleChangeIconDialog::GetIconicMetafile  
 Call this function to get a handle to the metafile that contains the iconic aspect of the selected item.  
  
```  
HGLOBAL GetIconicMetafile( ) const;  
  
```  
  
### Return Value  
 The handle to the metafile containing the iconic aspect of the new icon, if the dialog box was dismissed by choosing **OK**; otherwise, the icon as it was before the dialog was displayed.  
  
##  <a name="colechangeicondialog__m_ci"></a>  COleChangeIconDialog::m_ci  
 Structure of type **OLEUICHANGEICON** used to control the behavior of the Change Icon dialog box.  
  
```  
OLEUICHANGEICON m_ci;  
  
```  
  
### Remarks  
 Members of this structure can be modified either directly or through member functions.  
  
 For more information, see the                         [OLEUICHANGEICON](http://msdn.microsoft.com/library/windows/desktop/ms680098) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## See Also  
 [Base Class](../vs140/COleDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDialog](../vs140/COleDialog-Class.md)