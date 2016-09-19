---
title: "CAxDialogImpl Class"
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
ms.assetid: 817df483-3fa8-44e7-8487-72ba0881cd27
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAxDialogImpl Class
This class implements a dialog box (modal or modeless) that hosts ActiveX controls.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
  
template <  
   class  T,  
   class  TBase  
   = CWindow>  
   class ATL_NO_VTABLE CAxDialogImpl :  
   public CDialogImplBaseT<  TBase>  
  
```  
  
#### Parameters  
 `T`  
 Your class, derived from `CAxDialogImpl`.  
  
 *TBase*  
 The base window class for **CDialogImplBaseT**.  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CAxDialogImpl::AdviseSinkMap](../vs140/CAxDialogImpl--AdviseSinkMap.md)|Call this method to advise or unadvise all entries in the object's sink map event map.|  
|[CAxDialogImpl::Create](../vs140/CAxDialogImpl--Create.md)|Call this method to create a modeless dialog box.|  
|[CAxDialogImpl::DestroyWindow](../vs140/CAxDialogImpl--DestroyWindow.md)|Call this method to destroy a modeless dialog box.|  
|[CAxDialogImpl::DoModal](../vs140/CAxDialogImpl--DoModal.md)|Call this method to create a modal dialog box.|  
|[CAxDialogImpl::EndDialog](../vs140/CAxDialogImpl--EndDialog.md)|Call this method to destroy a modal dialog box.|  
|[CAxDialogImpl::GetDialogProc](../vs140/CAxDialogImpl--GetDialogProc.md)|Call this method to get a pointer to the `DialogProc` callback function.|  
|[CAxDialogImpl::GetIDD](../vs140/CAxDialogImpl--GetIDD.md)|Call this method to get the dialog template resource ID|  
|[CAxDialogImpl::IsDialogMessage](../vs140/CAxDialogImpl--IsDialogMessage.md)|Call this method to determine whether a message is intended for this dialog box and, if it is, process the message.|  
  
### Protected Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CAxDialogImpl::m_bModal](../vs140/CAxDialogImpl--m_bModal.md)|A variable that exists only in debug builds and is set to true if the dialog box is modal.|  
  
## Remarks  
 `CAxDialogImpl` allows you to create a modal or modeless dialog box. `CAxDialogImpl` provides the dialog box procedure, which uses the default message map to direct messages to the appropriate handlers.  
  
 `CAxDialogImpl` derives from `CDialogImplBaseT`, which in turn derives from *TBase* (by default, `CWindow`) and `CMessageMap`.  
  
 Your class must define an IDD member that specifies the dialog template resource ID. For example, adding an ATL Dialog object using the **Add Class** dialog box automatically adds the following line to your class:  
  
 [!CODE [NVC_ATL_Windowing#41](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#41)]  
  
 where `MyDialog` is the **Short name** entered in the ATL Dialog Wizard.  
  
 See [Implementing a Dialog Box](../vs140/Implementing-a-Dialog-Box.md) for more information.  
  
 Note that an ActiveX control on a modal dialog box created with `CAxDialogImpl` will not support accelerator keys. To support accelerator keys on a dialog box created with `CAxDialogImpl`, create a modeless dialog box and, using your own message loop, use [CAxDialogImpl::IsDialogMessage](../vs140/CAxDialogImpl--IsDialogMessage.md) after getting a message from the queue to handle an accelerator key.  
  
 For more information on `CAxDialogImpl`, see [ATL Control Containment FAQ](../vs140/ATL-Control-Containment-FAQ.md).  
  
## Inheritance Hierarchy  
 [CMessageMap](../vs140/CMessageMap-Class.md)  
  
 `TBase`  
  
 `CWindowImplRoot`  
  
 `CDialogImplBaseT`  
  
 `CAxDialogImpl`  
  
## Requirements  
 **Header:** atlwin.h  
  
##  <a name="caxdialogimpl__advisesinkmap"></a>  CAxDialogImpl::AdviseSinkMap  
 Call this method to advise or unadvise all entries in the object's sink map event map.  
  
```  
  
HRESULT AdviseSinkMap(  
      bool  bAdvise  
   );  
  
```  
  
### Parameters  
 `bAdvise`  
 Set to true if all sink entries are to be advised; false if all sink entries are to be unadvised.  
  
### Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
##  <a name="caxdialogimpl__create"></a>  CAxDialogImpl::Create  
 Call this method to create a modeless dialog box.  
  
```  
  
HWND Create(  
      HWND  hWndParent,  
      LPARAM  dwInitParam  
    = NULL   
   );  
   HWND Create(  
      HWND  hWndParent,  
      RECT&,  
      LPARAM  dwInitParam  
    = NULL   
   );  
  
```  
  
### Parameters  
 `hWndParent`  
 [in] The handle to the owner window.  
  
 `dwInitParam`  
 [in] Specifies the value to pass to the dialog box in the `lParam` parameter of the **WM_INITDIALOG** message.  
  
 **RECT&**  
 This parameter is not used. This parameter is passed in by `CComControl`.  
  
### Return Value  
 The handle to the newly created dialog box.  
  
### Remarks  
 This dialog box is automatically attached to the `CAxDialogImpl` object. To create a modal dialog box, call [DoModal](../vs140/CAxDialogImpl--DoModal.md).  
  
 The second override is provided only so dialog boxes can be used with [CComControl](../vs140/CComControl-Class.md).  
  
##  <a name="caxdialogimpl__destroywindow"></a>  CAxDialogImpl::DestroyWindow  
 Call this method to destroy a modeless dialog box.  
  
```  
  
BOOL DestroyWindow( );  
  
```  
  
### Return Value  
 TRUE if the window is successfully destroyed; otherwise FALSE.  
  
### Remarks  
 Do not call `DestroyWindow` to destroy a modal dialog box. Call [EndDialog](../vs140/CAxDialogImpl--EndDialog.md) instead.  
  
##  <a name="caxdialogimpl__domodal"></a>  CAxDialogImpl::DoModal  
 Call this method to create a modal dialog box.  
  
```  
  
INT_PTR DoModal(  
      HWND  hWndParent  
    = ::GetActiveWindow( ),  
      LPARAM  dwInitParam  
    = NULL   
   );  
  
```  
  
### Parameters  
 `hWndParent`  
 [in] The handle to the owner window. The default value is the return value of the [GetActiveWindow](http://msdn.microsoft.com/library/windows/desktop/ms646292) Win32 function.  
  
 `dwInitParam`  
 [in] Specifies the value to pass to the dialog box in the `lParam` parameter of the **WM_INITDIALOG** message.  
  
### Return Value  
 If successful, the value of the `nRetCode` parameter specified in the call to [EndDialog](../vs140/CAxDialogImpl--EndDialog.md); otherwise, -1.  
  
### Remarks  
 This dialog box is automatically attached to the `CAxDialogImpl` object.  
  
 To create a modeless dialog box, call [Create](../vs140/CAxDialogImpl--Create.md).  
  
##  <a name="caxdialogimpl__enddialog"></a>  CAxDialogImpl::EndDialog  
 Call this method to destroy a modal dialog box.  
  
```  
  
BOOL EndDialog(  
      int  nRetCode   
   );  
  
```  
  
### Parameters  
 `nRetCode`  
 [in] The value to be returned by [DoModal](../vs140/CAxDialogImpl--DoModal.md).  
  
### Return Value  
 TRUE if the dialog box is destroyed; otherwise, FALSE.  
  
### Remarks  
 `EndDialog` must be called through the dialog box procedure. After the dialog box is destroyed, Windows uses the value of `nRetCode` as the return value for `DoModal`, which created the dialog box.  
  
> [!NOTE]
>  Do not call `EndDialog` to destroy a modeless dialog box. Call [DestroyWindow](../vs140/CAxDialogImpl--DestroyWindow.md) instead.  
  
##  <a name="caxdialogimpl__getdialogproc"></a>  CAxDialogImpl::GetDialogProc  
 Call this method to get a pointer to the `DialogProc` callback function.  
  
```  
  
virtual DLGPROC GetDialogProc( );  
  
```  
  
### Return Value  
 Returns a pointer to the `DialogProc` callback function.  
  
### Remarks  
 The `DialogProc` function is an application-defined callback function.  
  
##  <a name="caxdialogimpl__getidd"></a>  CAxDialogImpl::GetIDD  
 Call this method to get the dialog template resource ID.  
  
```  
  
int GetIDD( );  
  
```  
  
### Return Value  
 Returns the dialog template resource ID.  
  
##  <a name="caxdialogimpl__isdialogmessage"></a>  CAxDialogImpl::IsDialogMessage  
 Call this method to determine whether a message is intended for this dialog box and, if it is, process the message.  
  
```  
  
BOOL IsDialogMessage(  
      LPMSG  pMsg  
   );  
  
```  
  
### Parameters  
 `pMsg`  
 Pointer to a [MSG](http://msdn.microsoft.com/library/windows/desktop/ms644958) structure that contains the message to be checked.  
  
### Return Value  
 Returns TRUE if the message has been processed, FALSE otherwise.  
  
### Remarks  
 This method is intended to be called from within a message loop.  
  
##  <a name="caxdialogimpl__m_bmodal"></a>  CAxDialogImpl::m_bModal  
 A variable that exists only in debug builds and is set to true if the dialog box is modal.  
  
```  
  
bool m_bModal;  
  
```  
  
## See Also  
 [CDialogImpl Class](../vs140/CDialogImpl-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)