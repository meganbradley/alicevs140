---
title: "CWinFormsControl Class"
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
ms.assetid: 6406dd7b-fb89-4a18-ac3a-c010d6b6289a
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinFormsControl Class
Provides the basic functionality for hosting of a Windows Forms control.  
  
## Syntax  
  
```  
template<class TManagedControl>  
class CWinFormsControl : public CWnd  
```  
  
#### Parameters  
 `TManagedControl`  
 A .NET Framework Windows Forms control to be displayed in the MFC application.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CWinFormsControl::CWinFormsControl](#cwinformscontrol__cwinformscontrol)|Constructs an MFC Windows Forms control wrapper object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CWinFormsControl::CreateManagedControl](#cwinformscontrol__createmanagedcontrol)|Creates a Windows Forms control in an MFC container.|  
|[CWinFormsControl::GetControl](#cwinformscontrol__getcontrol)|Retrieves a pointer to the Windows Forms control.|  
|[CWinFormsControl::GetControlHandle](#cwinformscontrol__getcontrolhandle)|Retrieves a handle to the Windows Forms control.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[CWinFormsControl::operator -&gt;](#cwinformscontrol__operator_-_gt_)|Replaces [GetControl](#cwinformscontrol__getcontrol) in expressions.|  
|[CWinFormsControl::operator TManagedControl^](#cwinformscontrol__operator_tmanagedcontrol^)|Casts a type as a pointer to a Windows Forms control.|  
  
## Remarks  
 The `CWinFormsControl` class provides the basic functionality for hosting of a Windows Forms control.  
  
 For more information on using Windows Forms, see [Using Windows Forms in MFC](../vs140/Using-a-Windows-Form-User-Control-in-MFC.md).  
  
 Your MFC code should not cache Window handles (usually stored in `m_hWnd`). Some Windows Forms control properties require that the underlying Win32 `Window` be destroyed and recreated using `DestroyWindow` and `CreateWindow`. The MFC Windows Forms implementation handles the `Destroy` and `Create` events of the controls to update the `m_hWnd` member.  
  
> [!NOTE]
>  MFC Windows Forms integration works only in projects which link dynamically with MFC (in which AFXDLL is defined).  
  
## Requirements  
 **Header:** afxwinforms.h  
  
##  <a name="cwinformscontrol__createmanagedcontrol"></a>  CWinFormsControl::CreateManagedControl  
 Creates a Windows Forms control in an MFC container.  
  
```  
inline BOOL CreateManagedControl(  
   System::Type^ pType,  
   DWORD dwStyle,  
   const RECT& rect,  
   CWnd* pParentWnd,  
   int nID  
)  
inline BOOL CreateManagedControl(  
   DWORD dwStyle,  
   const RECT& rect,  
   CWnd* pParentWnd,  
   int nID  
);  
inline BOOL CreateManagedControl(  
   DWORD dwStyle,  
   int nPlaceHolderID,  
   CWnd* pParentWnd  
);  
inline BOOL CreateManagedControl(  
   typename TManagedControl^ pControl,  
   DWORD dwStyle,  
   const RECT& rect,  
   CWnd* pParentWnd,  
   int nID  
);  
```  
  
### Parameters  
 `pType`  
 The data type of the control to be created. Must be a <xref:System.Type?qualifyHint=True> data type.  
  
 `dwStyle`  
 The window style to apply to the control. Specify a combination of [Window Styles](../vs140/Window-Styles.md). Currently, only the following styles are supported: WS_TABSTOP, WS_VISIBLE, WS_DISABLED and WS_GROUP.  
  
 `rect`  
 A [RECT Structure](../vs140/RECT-Structure.md) that defines the coordinates of the upper-left and lower-right corners of the control (first overload only).  
  
 `nPlaceHolderID`  
 The handle of the static place holder control placed in the Resource Editor. The newly created Windows Forms control replaces the static control, assuming its position, z-order, and styles (second overload only).  
  
 `pParentWnd`  
 A pointer to the parent window.  
  
 `nID`  
 The resource ID number to be assigned to the newly created control.  
  
 `pControl`  
 An instance of a Windows Forms control to be associated with the [CWinFormsControl](../vs140/CWinFormsControl-Class.md) object (fourth overload only).  
  
### Return Value  
 If successful, returns a nonzero value. If unsuccessful, returns zero.  
  
### Remarks  
 This method instantiates a .NET Framework Windows Forms control in an MFC container.  
  
 The first overload of the method accepts a .NET Framework data type `pType` so that MFC can instantiate a new object of this type. `pType` must be a <xref:System.Type?qualifyHint=True> data type.  
  
 The second overload of the method creates a Windows Forms control based on the `TManagedControl` template parameter of the `CWinFormsControl` class. The size and position of the control is based on the `RECT` structure passed to the method. Only `dwStyle` matters for the styles.  
  
 The third overload of the method creates a Windows Forms control that replaces a static control, destroying it and assuming its position, z-order, and styles. The static control serves only as a placeholder for the Windows Forms control. When creating the control, this overload combines the styles from `dwStyle` with the static control's resource styles.  
  
 The fourth overload of the method allows you to pass in an already instantiated Windows Forms control `pControl` that MFC will wrap. It must be of the same type as the `TManagedControl` template parameter of the `CWinFormsControl` class.  
  
 See [Using a Windows Form User Control in MFC](../vs140/Using-a-Windows-Form-User-Control-in-MFC.md) for samples on using Windows Form controls.  
  
##  <a name="cwinformscontrol__cwinformscontrol"></a>  CWinFormsControl::CWinFormsControl  
 Constructs an MFC Windows Forms control wrapper object.  
  
```  
CWinFormsControl( );  
```  
  
### Remarks  
 The Windows Forms control is instantiated when you call [CreateManagedControl](#cwinformscontrol__createmanagedcontrol).  
  
##  <a name="cwinformscontrol__getcontrol"></a>  CWinFormsControl::GetControl  
 Retrieves a pointer to the Windows Forms control.  
  
```  
inline TManagedControl^ GetControl( ) const;  
```  
  
### Return Value  
 Returns a pointer to the Windows Forms control.  
  
### Example  
  See [CWinFormsControl::CreateManagedControl](#cwinformscontrol__createmanagedcontrol).  
  
##  <a name="cwinformscontrol__getcontrolhandle"></a>  CWinFormsControl::GetControlHandle  
 Retrieves a handle to the Windows Forms control.  
  
```  
inline HWND GetControlHandle( ) const;  
```  
  
### Return Value  
 Returns a handle to the Windows Forms control.  
  
### Remarks  
 `GetControlHandle` is a helper method that returns the window handle stored in the .NET Framework control properties. The window handle value is copied to [CWnd::m_hWnd](../vs140/CWnd-Class.md#cwnd__m_hwnd) during the call to [CWnd::Attach](../vs140/CWnd-Class.md#cwnd__attach).  
  
##  <a name="cwinformscontrol__operator_-_gt_"></a>  CWinFormsControl::operator -&gt;  
 Replaces [GetControl](#cwinformscontrol__getcontrol) in expressions.  
  
```  
inline TManagedControl^ operator->( ) const;  
```  
  
### Remarks  
 This operator provides a convenient syntax that replaces `GetControl` in expressions.  
  
 For more information on Windows Forms, see [Using a Windows Form User Control in MFC](../vs140/Using-a-Windows-Form-User-Control-in-MFC.md).  
  
##  <a name="cwinformscontrol__operator_tmanagedcontrol_xor"></a>  CWinFormsControl::operator TManagedControl^  
 Casts a type as a pointer to a Windows Forms control.  
  
```  
inline operator TManagedControl^( ) const;  
```  
  
### Remarks  
 This operator passes `CWinFormsControl<``TManagedControl``>` to functions that accept a pointer to a Windows Forms control.  
  
## See Also  
 [CWinFormsDialog Class](../Topic/CWinFormsDialog%20Class.md)   
 [CWinFormsView Class](../Topic/CWinFormsView%20Class.md)