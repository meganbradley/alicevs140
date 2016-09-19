---
title: "CWnd::CreateControl"
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
ms.assetid: c992b8d3-d824-451f-a094-c71f5e50f622
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::CreateControl
Use this member function to create an ActiveX control that will be represented in the MFC program by a `CWnd` object.  
  
## Syntax  
  
```  
  
      BOOL CreateControl(  
   LPCTSTR pszClass,  
   LPCTSTR pszWindowName,  
   DWORD dwStyle,  
   const RECT& rect,  
   CWnd* pParentWnd,  
   UINT nID,  
   CFile* pPersist = NULL,  
   BOOL bStorage = FALSE,  
   BSTR bstrLicKey = NULL   
);  
BOOL CreateControl(  
   REFCLSID clsid,  
   LPCTSTR pszWindowName,  
   DWORD dwStyle,  
   const RECT& rect,  
   CWnd* pParentWnd,  
   UINT nID,  
   CFile* pPersist = NULL,  
   BOOL bStorage = FALSE,  
   BSTR bstrLicKey = NULL   
);  
BOOL CreateControl(  
   REFCLSID clsid,  
   LPCTSTR pszWindowName,  
   DWORD dwStyle,  
   const POINT* ppt,  
   const SIZE* psize,  
   CWnd* pParentWnd,  
   UINT nID,  
   CFile* pPersist = NULL,  
   BOOL bStorage = FALSE,  
    BSTR bstrLicKey = NULL  
);  
```  
  
#### Parameters  
 *pszClass*  
 This string may contain the OLE "short name" (ProgID) for the class, e.g., "CIRC3.Circ3Ctrl.1". The name needs to match the same name registered by the control. Alternatively, the string may contain the string form of a **CLSID**, contained in braces, e.g., "{9DBAFCCF-592F-101B-85CE-00608CEC297B}". In either case, `CreateControl` converts the string to the corresponding class ID.  
  
 *pszWindowName*  
 A pointer to the text to be displayed in the control. Sets the value of the control's Caption or Text property (if any). If **NULL**, the control's Caption or Text property is not changed.  
  
 `dwStyle`  
 Windows styles. The available styles are listed under Remarks.  
  
 `rect`  
 Specifies the control's size and position. It can be either a [CRect](../vs140/CRect-Class.md) object or a [RECT](../vs140/RECT-Structure.md) structure.  
  
 `ppt`  
 Points to a [POINT](../vs140/POINT-Structure.md) structure or `CPoint` object that contains the upper left corner of the control.  
  
 `pSize`  
 Points to a [SIZE](http://msdn.microsoft.com/library/windows/desktop/dd145106) structure or `CSize` object that contains the control's size  
  
 `pParentWnd`  
 Specifies the control's parent window. It must not be **NULL**.  
  
 `nID`  
 Specifies the control's ID.  
  
 `pPersist`  
 A pointer to a [CFile](../vs140/CFile-Class.md) containing the persistent state for the control. The default value is **NULL**, indicating that the control initializes itself without restoring its state from any persistent storage. If not **NULL**, it should be a pointer to a `CFile`-derived object which contains the control's persistent data, in the form of either a stream or a storage. This data could have been saved in a previous activation of the client. The `CFile` can contain other data, but must have its read-write pointer set to the first byte of persistent data at the time of the call to `CreateControl`.  
  
 `bStorage`  
 Indicates whether the data in `pPersist` should be interpreted as IStorage or IStream data. If the data in `pPersist` is a storage, `bStorage` should be **TRUE**. If the data in `pPersist` is a stream, `bStorage` should be **FALSE**. The default value is **FALSE**.  
  
 *bstrLicKe*y  
 Optional license key data. This data is needed only for creating controls that require a run-time license key. If the control supports licensing, you must provide a license key for the creation of the control to succeed. The default value is **NULL**.  
  
 `clsid`  
 The unique class ID of the control.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 `CreateControl` is a direct analog of the [CWnd::Create](../vs140/CWnd--Create.md) function, which creates the window for a `CWnd`. `CreateControl` creates an ActiveX control instead of an ordinary window.  
  
 Only a subset of the Windows `dwStyle` flags are supported for `CreateControl`:  
  
-   **WS_VISIBLE** Creates a window that is initially visible. Required if you want the control to be visible immediately, like ordinary windows.  
  
-   **WS_DISABLED** Creates a window that is initially disabled. A disabled window cannot receive input from the user. Can be set if the control has an Enabled property.  
  
-   `WS_BORDER` Creates a window with a thin-line border. Can be set if control has a BorderStyle property.  
  
-   **WS_GROUP** Specifies the first control of a group of controls. The user can change the keyboard focus from one control in the group to the next by using the direction keys. All controls defined with the **WS_GROUP** style after the first control belong to the same group. The next control with the **WS_GROUP** style ends the group and starts the next group.  
  
-   **WS_TABSTOP** Specifies a control that can receive the keyboard focus when the user presses the TAB key. Pressing the TAB key changes the keyboard focus to the next control of the **WS_TABSTOP** style.  
  
## Example  
 [!CODE [NVC_MFCWindowing#81](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#81)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [MFC ActiveX Controls](../vs140/MFC-ActiveX-Controls.md)