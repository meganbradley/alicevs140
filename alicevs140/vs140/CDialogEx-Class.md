---
title: "CDialogEx Class"
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
ms.assetid: a6ed3b1f-aef8-4b66-ac78-2160faf63c13
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDialogEx Class
The `CDialogEx` class specifies the background color and background image of a dialog box.  
  
## Syntax  
  
```  
class CDialogEx : public CDialog  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CDialogEx::CDialogEx](#cdialogex__cdialogex)|Constructs a `CDialogEx` object.|  
|`CDialogEx::~CDialogEx`|Destructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CDialogEx::SetBackgroundColor](#cdialogex__setbackgroundcolor)|Sets the background color of the dialog box.|  
|[CDialogEx::SetBackgroundImage](#cdialogex__setbackgroundimage)|Sets the background image of the dialog box.|  
  
## Remarks  
 To use the `CDialogEx` class, derive your dialog box class from the `CDialogEx` class instead of the `CDialog` class.  
  
 Dialog box images are stored in a resource file. The framework automatically deletes any image that is loaded from the resource file. To programmatically delete the current background image, call the [SetBackgroundImage](#cdialogex__setbackgroundimage) method or implement an `OnDestroy` event handler. When you call the [SetBackgroundImage](#cdialogex__setbackgroundimage) method, pass in an `HBITMAP` parameter as the image handle. The `CDialogEx` object will take ownership of the image and delete it if the `m_bAutoDestroyBmp` flag is `TRUE`.  
  
 A `CDialogEx` object can be a parent of a [CMFCPopupMenu](../vs140/CMFCPopupMenu-Class.md) object. The [CMFCPopupMenu](../vs140/CMFCPopupMenu-Class.md) object calls the `CDialogEx::SetActiveMenu` method when the [CMFCPopupMenu](../vs140/CMFCPopupMenu-Class.md) object opens. Afterward, the `CDialogEx` object handles any menu event until the [CMFCPopupMenu](../vs140/CMFCPopupMenu-Class.md) object is closed.  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CCmdTarget](../vs140/CCmdTarget-Class.md)  
  
 [CWnd](../vs140/CWnd-Class.md)  
  
 [CDialog](../vs140/CDialog-Class.md)  
  
 [CDialogEx](../vs140/CDialogEx-Class.md)  
  
## Requirements  
 **Header:** afxdialogex.h  
  
##  <a name="cdialogex__cdialogex"></a>  CDialogEx::CDialogEx  
 Constructs a `CDialogEx` object.  
  
```  
CDialogEx(  
   UINT nIDTemplate,  
   CWnd* pParent=NULL   
);  
CDialogEx(  
   LPCTSTR lpszTemplateName,  
   CWnd* pParentWnd=NULL   
);  
```  
  
### Parameters  
 [in] `nIDTemplate`  
 The resource ID of a dialog box template.  
  
 [in] `lpszTemplateName`  
 The resource name of a dialog box template.  
  
 [in] `pParent`  
 A pointer to the parent window. The default value is `NULL`.  
  
 [in] `pParentWnd`  
 A pointer to the parent window. The default value is `NULL`.  
  
### Return Value  
  
### Remarks  
  
##  <a name="cdialogex__setbackgroundcolor"></a>  CDialogEx::SetBackgroundColor  
 Sets the background color of the dialog box.  
  
```  
void SetBackgroundColor(  
   COLORREF color,  
   BOOL bRepaint=TRUE   
);  
```  
  
### Parameters  
 [in] `color`  
 An RGB color value.  
  
 [in] `bRepaint`  
 `TRUE` to immediately update the screen; otherwise, `FALSE`. The default value is `TRUE`.  
  
### Remarks  
  
##  <a name="cdialogex__setbackgroundimage"></a>  CDialogEx::SetBackgroundImage  
 Sets the background image of the dialog box.  
  
```  
void SetBackgroundImage(  
   HBITMAP hBitmap,  
   BackgroundLocation location=BACKGR_TILE,  
   BOOL bAutoDestroy=TRUE,  
   BOOL bRepaint=TRUE   
);  
BOOL SetBackgroundImage(  
   UINT uiBmpResId,  
   BackgroundLocation location=BACKGR_TILE,  
   BOOL bRepaint=TRUE   
);  
```  
  
### Parameters  
 [in] `hBitmap`  
 A handle to the background image.  
  
 [in] `uiBmpResId`  
 The resource ID of the background image.  
  
 [in] `location`  
 One of the `CDialogEx::BackgroundLocation` values that specify the location of the image. Valid values include BACKGR_TILE, BACKGR_TOPLEFT, BACKGR_TOPRIGHT, BACKGR_BOTTOMLEFT, and BACKGR_BOTTOMRIGHT. The default value is BACKGR_TILE.  
  
 [in] `bAutoDestroy`  
 `TRUE` to automatically destroy the background image; otherwise, `FALSE`.  
  
 [in] `bRepaint`  
 `TRUE` to immediately redraw the dialog box; otherwise, `FALSE`.  
  
### Return Value  
 In the second method overload syntax, `TRUE` if the method is successful; otherwise, `FALSE`.  
  
### Remarks  
 The image that you specify is not stretched to fit the dialog box client area.  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Classes](../vs140/MFC-Classes.md)   
 [CMFCPopupMenu](../vs140/CMFCPopupMenu-Class.md)   
 [CMFCContextMenuManager](../vs140/CContextMenuManager-Class.md)