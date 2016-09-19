---
title: "COleControlSite::CreateControl"
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
ms.assetid: d62654ab-eec1-4e55-b13c-a103400de5f1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlSite::CreateControl
Creates an ActiveX control, hosted by the `COleControlSite` object.  
  
## Syntax  
  
```  
  
      virtual HRESULT CreateControl(  
   CWnd* pWndCtrl,  
   REFCLSID clsid,  
   LPCTSTR lpszWindowName,  
   DWORD dwStyle,  
   const RECT& rect,  
   UINT nID,  
   CFile* pPersist = NULL,  
   BOOL bStorage = FALSE,  
   BSTR bstrLicKey = NULL   
);  
virtual HRESULT CreateControl(  
   CWnd* pWndCtrl,  
   REFCLSID clsid,  
   LPCTSTR lpszWindowName,  
   DWORD dwStyle,  
   const POINT* ppt,  
   const SIZE* psize,  
   UINT nID,  
   CFile* pPersist = NULL,  
   BOOL bStorage = FALSE,  
   BSTR bstrLicKey = NULL   
);  
```  
  
#### Parameters  
 `pWndCtrl`  
 A pointer to the window object representing the control.  
  
 `clsid`  
 The unique class ID of the control.  
  
 `lpszWindowName`  
 A pointer to the text to be displayed in the control. Sets the value of the winodw's Caption or Text property (if any).  
  
 `dwStyle`  
 Windows styles. The available styles are listed under the **Remarks** section.  
  
 `rect`  
 Specifies the control's size and position. It can be either a `CRect` object or a `RECT` structure.  
  
 `nID`  
 Specifies the control's child window ID.  
  
 `pPersist`  
 A pointer to a `CFile` containing the persistent state for the control. The default value is **NULL**, indicating that the control initializes itself without restoring its state from any persistent storage. If not **NULL**, it should be a pointer to a `CFile`-derived object that contains the control's persistent data, in the form of either a stream or a storage. This data could have been saved in a previous activation of the client. The `CFile` can contain other data, but must have its read-write pointer set to the first byte of persistent data at the time of the call to `CreateControl`.  
  
 `bStorage`  
 Indicates whether the data in `pPersist` should be interpreted as `IStorage` or `IStream` data. If the data in `pPersist` is a storage, `bStorage` should be **TRUE**. If the data in `pPersist` is a stream, `bStorage` should be **FALSE**. The default value is **FALSE**.  
  
 `bstrLicKey`  
 Optional license key data. This data is needed only for creating controls that require a run-time license key. If the control supports licensing, you must provide a license key for the creation of the control to succeed. The default value is **NULL**.  
  
 `ppt`  
 A pointer to a **POINT** structure that contains the upper-left corner of the control. The size of the control is determined by the value of *psize*. The `ppt` and *psize* values are an optional method of specifying the size and position opf the control.  
  
 *psize*  
 A pointer to a **SIZE** structure that contains the size of the control. The upper-left corner is determined by the value of `ppt`. The `ppt` and *psize* values are an optional method of specifying the size and position opf the control.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 Only a subset of the Windows `dwStyle` flags are supported by `CreateControl`:  
  
-   **WS_VISIBLE** Creates a window that is initially visible. Required if you want the control to be visible immediately, like ordinary windows.  
  
-   **WS_DISABLED** Creates a window that is initially disabled. A disabled window cannot receive input from the user. Can be set if the control has an Enabled property.  
  
-   `WS_BORDER` Creates a window with a thin-line border. Can be set if control has a BorderStyle property.  
  
-   **WS_GROUP** Specifies the first control of a group of controls. The user can change the keyboard focus from one control in the group to the next by using the direction keys. All controls defined with the **WS_GROUP** style after the first control belong to the same group. The next control with the **WS_GROUP** style ends the group and starts the next group.  
  
-   **WS_TABSTOP** Specifies a control that can receive the keyboard focus when the user presses the TAB key. Pressing the TAB key changes the keyboard focus to the next control of the **WS_TABSTOP** style.  
  
 Use the second overload to create default-sized controls.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlSite Class](../vs140/COleControlSite-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControlContainer::CreateControl](../vs140/COleControlContainer--CreateControl.md)