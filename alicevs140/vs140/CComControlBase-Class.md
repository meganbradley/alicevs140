---
title: "CComControlBase Class"
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
ms.assetid: 3d1bf022-acf2-4092-8283-ff8cee6332f3
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase Class
This class provides methods for creating and managing ATL controls.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
  
class ATL_NO_VTABLE CComControlBase  
  
```  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|[CComControlBase::AppearanceType](../vs140/CComControlBase--AppearanceType.md)|Override if your `m_nAppearance` stock property isn't of type `short`.|  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CComControlBase::CComControlBase](../vs140/CComControlBase--CComControlBase.md)|The constructor.|  
|[CComControlBase::~CComControlBase](../vs140/CComControlBase--~CComControlBase.md)|The destructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CComControlBase::ControlQueryInterface](../vs140/CComControlBase--ControlQueryInterface.md)|Retrieves a pointer to the requested interface.|  
|[CComControlBase::DoesVerbActivate](../vs140/CComControlBase--DoesVerbActivate.md)|Checks that the `iVerb` parameter used by `IOleObjectImpl::DoVerb` either activates the control's user interface ( `iVerb` equals `OLEIVERB_UIACTIVATE`), defines the action taken when the user double-clicks the control ( `iVerb` equals `OLEIVERB_PRIMARY`), displays the control ( `iVerb` equals `OLEIVERB_SHOW`), or activates the control ( `iVerb` equals **OLEIVERB_INPLACEACTIVATE**).|  
|[CComControlBase::DoesVerbUIActivate](../vs140/CComControlBase--DoesVerbUIActivate.md)|Checks that the `iVerb` parameter used by `IOleObjectImpl::DoVerb` causes the control's user interface to activate and returns **TRUE**.|  
|[CComControlBase::DoVerbProperties](../vs140/CComControlBase--DoVerbProperties.md)|Displays the control's property pages.|  
|[CComControlBase::FireViewChange](../vs140/CComControlBase--FireViewChange.md)|Call this method to tell the container to redraw the control, or notify the registered advise sinks that the control's view has changed.|  
|[CComControlBase::GetAmbientAppearance](../vs140/CComControlBase--GetAmbientAppearance.md)|Retrieves **DISPID_AMBIENT_APPEARANCE**, the current appearance setting for the control: 0 for flat and 1 for 3D.|  
|[CComControlBase::GetAmbientAutoClip](../vs140/CComControlBase--GetAmbientAutoClip.md)|Retrieves **DISPID_AMBIENT_AUTOCLIP**, a flag indicating whether the container supports automatic clipping of the control display area.|  
|[CComControlBase::GetAmbientBackColor](../vs140/CComControlBase--GetAmbientBackColor.md)|Retrieves **DISPID_AMBIENT_BACKCOLOR**, the ambient background color for all controls, defined by the container.|  
|[CComControlBase::GetAmbientCharSet](../vs140/CComControlBase--GetAmbientCharSet.md)|Retrieves **DISPID_AMBIENT_CHARSET**, the ambient character set for all controls, defined by the container.|  
|[CComControlBase::GetAmbientCodePage](../vs140/CComControlBase--GetAmbientCodePage.md)|Retrieves **DISPID_AMBIENT_CODEPAGE**, the ambient character set for all controls, defined by the container.|  
|[CComControlBase::GetAmbientDisplayAsDefault](../vs140/CComControlBase--GetAmbientDisplayAsDefault.md)|Retrieves **DISPID_AMBIENT_DISPLAYASDEFAULT**, a flag that is **TRUE** if the container has marked the control in this site to be a default button, and therefore a button control should draw itself with a thicker frame.|  
|[CComControlBase::GetAmbientDisplayName](../vs140/CComControlBase--GetAmbientDisplayName.md)|Retrieves **DISPID_AMBIENT_DISPLAYNAME**, the name the container has supplied to the control.|  
|[CComControlBase::GetAmbientFont](../vs140/CComControlBase--GetAmbientFont.md)|Retrieves a pointer to the container's ambient `IFont` interface.|  
|[CComControlBase::GetAmbientFontDisp](../vs140/CComControlBase--GetAmbientFontDisp.md)|Retrieves a pointer to the container's ambient **IFontDisp** dispatch interface.|  
|[CComControlBase::GetAmbientForeColor](../vs140/CComControlBase--GetAmbientForeColor.md)|Retrieves **DISPID_AMBIENT_FORECOLOR**, the ambient foreground color for all controls, defined by the container.|  
|[CComControlBase::GetAmbientLocaleID](../vs140/CComControlBase--GetAmbientLocaleID.md)|Retrieves **DISPID_AMBIENT_LOCALEID**, the identifier of the language used by the container.|  
|[CComControlBase::GetAmbientMessageReflect](../vs140/CComControlBase--GetAmbientMessageReflect.md)|Retrieves **DISPID_AMBIENT_MESSAGEREFLECT**, a flag indicating whether the container wants to receive window messages (such as `WM_DRAWITEM`) as events.|  
|[CComControlBase::GetAmbientPalette](../vs140/CComControlBase--GetAmbientPalette.md)|Retrieves **DISPID_AMBIENT_PALETTE**, used to access the container's `HPALETTE`.|  
|[CComControlBase::GetAmbientProperty](../vs140/CComControlBase--GetAmbientProperty.md)|Retrieves the container property specified by `id`.|  
|[CComControlBase::GetAmbientRightToLeft](../vs140/CComControlBase--GetAmbientRightToLeft.md)|Retrieves **DISPID_AMBIENT_RIGHTTOLEFT**, the direction in which content is displayed by the container.|  
|[CComControlBase::GetAmbientScaleUnits](../vs140/CComControlBase--GetAmbientScaleUnits.md)|Retrieves **DISPID_AMBIENT_SCALEUNITS**, the container's ambient units (such as inches or centimeters) for labeling displays.|  
|[CComControlBase::GetAmbientShowGrabHandles](../vs140/CComControlBase--GetAmbientShowGrabHandles.md)|Retrieves **DISPID_AMBIENT_SHOWGRABHANDLES**, a flag indicating whether the container allows the control to display grab handles for itself when active.|  
|[CComControlBase::GetAmbientShowHatching](../vs140/CComControlBase--GetAmbientShowHatching.md)|Retrieves **DISPID_AMBIENT_SHOWHATCHING**, a flag indicating whether the container allows the control to display itself with a hatched pattern when the UI is active.|  
|[CComControlBase::GetAmbientSupportsMnemonics](../vs140/CComControlBase--GetAmbientSupportsMnemonics.md)|Retrieves **DISPID_AMBIENT_SUPPORTSMNEMONICS**, a flag indicating whether the container supports keyboard mnemonics.|  
|[CComControlBase::GetAmbientTextAlign](../vs140/CComControlBase--GetAmbientTextAlign.md)|Retrieves **DISPID_AMBIENT_TEXTALIGN**, the text alignment preferred by the container: 0 for general alignment (numbers right, text left), 1 for left alignment, 2 for center alignment, and 3 for right alignment.|  
|[CComControlBase::GetAmbientTopToBottom](../vs140/CComControlBase--GetAmbientTopToBottom.md)|Retrieves **DISPID_AMBIENT_TOPTOBOTTOM**, the direction in which content is displayed by the container.|  
|[CComControlBase::GetAmbientUIDead](../vs140/CComControlBase--GetAmbientUIDead.md)|Retrieves **DISPID_AMBIENT_UIDEAD**, a flag indicating whether the container wants the control to respond to user-interface actions.|  
|[CComControlBase::GetAmbientUserMode](../vs140/CComControlBase--GetAmbientUserMode.md)|Retrieves **DISPID_AMBIENT_USERMODE**, a flag indicating whether the container is in run-mode (                                        **TRUE**) or design-mode (                                        **FALSE**).|  
|[CComControlBase::GetDirty](../vs140/CComControlBase--GetDirty.md)|Returns the value of data member `m_bRequiresSave`.|  
|[CComControlBase::GetZoomInfo](../vs140/CComControlBase--GetZoomInfo.md)|Retrieves the x and y values of the numerator and denominator of the zoom factor for a control activated for in-place editing.|  
|[CComControlBase::InPlaceActivate](../vs140/CComControlBase--InPlaceActivate.md)|Causes the control to transition from the inactive state to whatever state the verb in `iVerb` indicates.|  
|[CComControlBase::InternalGetSite](../vs140/CComControlBase--InternalGetSite.md)|Call this method to query the control site for a pointer to the identified interface.|  
|[CComControlBase::OnDraw](../vs140/CComControlBase--OnDraw.md)|Override this method to draw your control.|  
|[CComControlBase::OnDrawAdvanced](../vs140/CComControlBase--OnDrawAdvanced.md)|The default **OnDrawAdvanced** prepares a normalized device context for drawing, then calls your control class's `OnDraw` method.|  
|[CComControlBase::OnKillFocus](../vs140/CComControlBase--OnKillFocus.md)|Checks that the control is in-place active and has a valid control site, then informs the container that the control has lost focus.|  
|[CComControlBase::OnMouseActivate](../vs140/CComControlBase--OnMouseActivate.md)|Checks that the UI is in user mode, then activates the control.|  
|[CComControlBase::OnPaint](../vs140/CComControlBase--OnPaint.md)|Prepares the container for painting, gets the control's client area, then calls the control class's `OnDraw` method.|  
|[CComControlBase::OnSetFocus](../vs140/CComControlBase--OnSetFocus.md)|Checks that the control is in-place active and has a valid control site, then informs the container the control has gained focus.|  
|[CComControlBase::PreTranslateAccelerator](../vs140/CComControlBase--PreTranslateAccelerator.md)|Override this method to provide your own keyboard accelerator handlers.|  
|[CComControlBase::SendOnClose](../vs140/CComControlBase--SendOnClose.md)|Notifies all advisory sinks registered with the advise holder that the control has been closed.|  
|[CComControlBase::SendOnDataChange](../vs140/CComControlBase--SendOnDataChange.md)|Notifies all advisory sinks registered with the advise holder that the control data has changed.|  
|[CComControlBase::SendOnRename](../vs140/CComControlBase--SendOnRename.md)|Notifies all advisory sinks registered with the advise holder that the control has a new moniker.|  
|[CComControlBase::SendOnSave](../vs140/CComControlBase--SendOnSave.md)|Notifies all advisory sinks registered with the advise holder that the control has been saved.|  
|[CComControlBase::SendOnViewChange](../vs140/CComControlBase--SendOnViewChange.md)|Notifies all registered advisory sinks that the control's view has changed.|  
|[CComControlBase::SetControlFocus](../vs140/CComControlBase--SetControlFocus.md)|Sets or removes the keyboard focus to or from the control.|  
|[CComControlBase::SetDirty](../vs140/CComControlBase--SetDirty.md)|Sets the data member `m_bRequiresSave` to the value in `bDirty`.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CComControlBase::m_bAutoSize](../vs140/CComControlBase--m_bAutoSize.md)|Flag indicating the control cannot be any other size.|  
|[CComControlBase::m_bDrawFromNatural](../vs140/CComControlBase--m_bDrawFromNatural.md)|Flag indicating that `IDataObjectImpl::GetData` and `CComControlBase::GetZoomInfo` should set the control size from `m_sizeNatural` rather than from `m_sizeExtent`.|  
|[CComControlBase::m_bDrawGetDataInHimetric](../vs140/CComControlBase--m_bDrawGetDataInHimetric.md)|Flag indicating that `IDataObjectImpl::GetData` should use HIMETRIC units and not pixels when drawing.|  
|[CComControlBase::m_bInPlaceActive](../vs140/CComControlBase--m_bInPlaceActive.md)|Flag indicating the control is in-place active.|  
|[CComControlBase::m_bInPlaceSiteEx](../vs140/CComControlBase--m_bInPlaceSiteEx.md)|Flag indicating the container supports the **IOleInPlaceSiteEx** interface and OCX96 control features, such as windowless and flicker-free controls.|  
|[CComControlBase::m_bNegotiatedWnd](../vs140/CComControlBase--m_bNegotiatedWnd.md)|Flag indicating whether or not the control has negotiated with the container about support for OCX96 control features (such as flicker-free and windowless controls), and whether the control is windowed or windowless.|  
|[CComControlBase::m_bRecomposeOnResize](../vs140/CComControlBase--m_bRecomposeOnResize.md)|Flag indicating the control wants to recompose its presentation when the container changes the control's display size.|  
|[CComControlBase::m_bRequiresSave](../vs140/CComControlBase--m_bRequiresSave.md)|Flag indicating the control has changed since it was last saved.|  
|[CComControlBase::m_bResizeNatural](../vs140/CComControlBase--m_bResizeNatural.md)|Flag indicating the control wants to resize its natural extent (its unscaled physical size) when the container changes the control's display size.|  
|[CComControlBase::m_bUIActive](../vs140/CComControlBase--m_bUIActive.md)|Flag indicating the control's user interface, such as menus and toolbars, is active.|  
|[CComControlBase::m_bUsingWindowRgn](../vs140/CComControlBase--m_bUsingWindowRgn.md)|Flag indicating the control is using the container-supplied window region.|  
|[CComControlBase::m_bWasOnceWindowless](../vs140/CComControlBase--m_bWasOnceWindowless.md)|Flag indicating the control has been windowless, but may or may not be windowless now.|  
|[CComControlBase::m_bWindowOnly](../vs140/CComControlBase--m_bWindowOnly.md)|Flag indicating the control should be windowed, even if the container supports windowless controls.|  
|[CComControlBase::m_bWndLess](../vs140/CComControlBase--m_bWndLess.md)|Flag indicating the control is windowless.|  
|[CComControlBase::m_hWndCD](../vs140/CComControlBase--m_hWndCD.md)|Contains a reference to the window handle associated with the control.|  
|[CComControlBase::m_nFreezeEvents](../vs140/CComControlBase--m_nFreezeEvents.md)|A count of the number of times the container has frozen events (refused to accept events) without an intervening thaw of events (acceptance of events).|  
|[CComControlBase::m_rcPos](../vs140/CComControlBase--m_rcPos.md)|The position in pixels of the control, expressed in the coordinates of the container.|  
|[CComControlBase::m_sizeExtent](../vs140/CComControlBase--m_sizeExtent.md)|The extent of the control in HIMETRIC units (each unit is 0.01 millimeters) for a particular display.|  
|[CComControlBase::m_sizeNatural](../vs140/CComControlBase--m_sizeNatural.md)|The physical size of the control in HIMETRIC units (each unit is 0.01 millimeters).|  
|[CComControlBase::m_spAdviseSink](../vs140/CComControlBase--m_spAdviseSink.md)|A direct pointer to the advisory connection on the container (the container's [IAdviseSink](http://msdn.microsoft.com/library/windows/desktop/ms692513)).|  
|[CComControlBase::m_spAmbientDispatch](../vs140/CComControlBase--m_spAmbientDispatch.md)|A `CComDispatchDriver` object that lets you retrieve and set the container's properties through an `IDispatch` pointer.|  
|[CComControlBase::m_spClientSite](../vs140/CComControlBase--m_spClientSite.md)|A pointer to the control's client site within the container.|  
|[CComControlBase::m_spDataAdviseHolder](../vs140/CComControlBase--m_spDataAdviseHolder.md)|Provides a standard means to hold advisory connections between data objects and advise sinks.|  
|[CComControlBase::m_spInPlaceSite](../vs140/CComControlBase--m_spInPlaceSite.md)|A pointer to the container's [IOleInPlaceSite](http://msdn.microsoft.com/library/windows/desktop/ms686586), [IOleInPlaceSiteEx](http://msdn.microsoft.com/library/windows/desktop/ms693461), or [IOleInPlaceSiteWindowless](http://msdn.microsoft.com/library/windows/desktop/ms682300) interface pointer.|  
|[CComControlBase::m_spOleAdviseHolder](../vs140/CComControlBase--m_spOleAdviseHolder.md)|Provides a standard implementation of a way to hold advisory connections.|  
  
## Remarks  
 This class provides methods for creating and managing ATL controls. [CComControl Class](../vs140/CComControl-Class.md) derives from `CComControlBase`. When you create a Standard Control or DHTML control using the ATL Control Wizard, the wizard will automatically derive your class from `CComControlBase`.  
  
 For more information about creating a control, see the [ATL Tutorial](../vs140/Active-Template-Library--ATL--Tutorial.md). For more information about the ATL Project Wizard, see the article [Creating an ATL Project](../vs140/Creating-an-ATL-Project.md).  
  
## Requirements  
 **Header:** atlctl.h  
  
##  <a name="ccomcontrolbase__appearancetype"></a>  CComControlBase::AppearanceType  
 Override if your **m_nAppearance** stock property isn't of type **short**.  
  
```  
  
typedef short AppearanceType;  
  
```  
  
### Remarks  
 The ATL Control Wizard adds **m_nAppearance** stock property of type short. Override `AppearanceType` if you use a different data type.  
  
##  <a name="ccomcontrolbase__ccomcontrolbase"></a>  CComControlBase::CComControlBase  
 The constructor.  
  
```  
  
CComControlBase(  
      HWND&  h  
   );  
  
```  
  
### Parameters  
 `h`  
 The handle to the window associated with the control.  
  
### Remarks  
 Initializes the control size to 5080X5080 HIMETRIC units (2"X2") and initializes the `CComControlBase` data member values to **NULL** or **FALSE**.  
  
##  <a name="ccomcontrolbase___dtorccomcontrolbase"></a>  CComControlBase::~CComControlBase  
 The destructor.  
  
```  
  
~CComControlBase( );  
  
```  
  
### Remarks  
 If the control is windowed, `~CComControlBase` destroys it by calling [DestroyWindow](http://msdn.microsoft.com/library/windows/desktop/ms632682).  
  
##  <a name="ccomcontrolbase__controlqueryinterface"></a>  CComControlBase::ControlQueryInterface  
 Retrieves a pointer to the requested interface.  
  
```  
  
virtual HRESULT ControlQueryInterface(  
      const IID&  iid,  
   void**  ppv  
   );  
  
```  
  
### Parameters  
 `iid`  
 The GUID of the interface being requested.  
  
 `ppv`  
 A pointer to the interface pointer identified by `iid`, or **NULL** if the interface is not found.  
  
### Remarks  
 Only handles interfaces in the COM map table.  
  
### Example  
 [!CODE [NVC_ATL_COM#15](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#15)]  
  
##  <a name="ccomcontrolbase__doesverbactivate"></a>  CComControlBase::DoesVerbActivate  
 Checks that the `iVerb` parameter used by `IOleObjectImpl::DoVerb` either activates the control's user interface ( `iVerb` equals `OLEIVERB_UIACTIVATE`), defines the action taken when the user double-clicks the control ( `iVerb` equals `OLEIVERB_PRIMARY`), displays the control ( `iVerb` equals `OLEIVERB_SHOW`), or activates the control ( `iVerb` equals **OLEIVERB_INPLACEACTIVATE**).  
  
```  
  
BOOL DoesVerbActivate(  
      LONG  iVerb  
   );  
  
```  
  
### Parameters  
 `iVerb`  
 Value indicating the action to be performed by `DoVerb`.  
  
### Return Value  
 Returns **TRUE** if `iVerb` equals `OLEIVERB_UIACTIVATE`, `OLEIVERB_PRIMARY`, `OLEIVERB_SHOW`, or **OLEIVERB_INPLACEACTIVATE**; otherwise, returns **FALSE**.  
  
### Remarks  
 You can override this method to define your own activation verb.  
  
##  <a name="ccomcontrolbase__doesverbuiactivate"></a>  CComControlBase::DoesVerbUIActivate  
 Checks that the `iVerb` parameter used by `IOleObjectImpl::DoVerb` causes the control's user interface to activate and returns **TRUE**.  
  
```  
  
BOOL DoesVerbUIActivate(  
      LONG  iVerb  
   );  
  
```  
  
### Parameters  
 `iVerb`  
 Value indicating the action to be performed by `DoVerb`.  
  
### Return Value  
 Returns **TRUE** if `iVerb` equals `OLEIVERB_UIACTIVATE`, `OLEIVERB_PRIMARY`, `OLEIVERB_SHOW`, or **OLEIVERB_INPLACEACTIVATE**. Otherwise, the method returns **FALSE**.  
  
##  <a name="ccomcontrolbase__doverbproperties"></a>  CComControlBase::DoVerbProperties  
 Displays the control's property pages.  
  
```  
  
HRESULT DoVerbProperties(  
      LPCRECT /* prcPosRect */                ,  
      HWND  hwndParent  
   );  
  
```  
  
### Parameters  
 `prcPosRec`  
 Reserved.  
  
 *hwndParent*  
 Handle of the window containing the control.  
  
### Return Value  
 One of the standard HRESULT values.  
  
### Example  
 [!CODE [NVC_ATL_COM#19](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#19)]  
  
 [!CODE [NVC_ATL_COM#20](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#20)]  
  
##  <a name="ccomcontrolbase__fireviewchange"></a>  CComControlBase::FireViewChange  
 Call this method to tell the container to redraw the control, or notify the registered advise sinks that the control's view has changed.  
  
```  
  
HRESULT FireViewChange( );  
  
```  
  
### Return Value  
 One of the standard HRESULT values.  
  
### Remarks  
 If the control is active (the control class data member [CComControlBase::m_bInPlaceActive](../vs140/CComControlBase--m_bInPlaceActive.md) is **TRUE**), notifies the container that you want to redraw the entire control. If the control is inactive, notifies the control's registered advise sinks (through the control class data member [CComControlBase::m_spAdviseSink](../vs140/CComControlBase--m_spAdviseSink.md)) that the control's view has changed.  
  
### Example  
 [!CODE [NVC_ATL_COM#21](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#21)]  
  
##  <a name="ccomcontrolbase__getambientappearance"></a>  CComControlBase::GetAmbientAppearance  
 Retrieves **DISPID_AMBIENT_APPEARANCE**, the current appearance setting for the control: 0 for flat and 1 for 3D.  
  
```  
  
HRESULT GetAmbientAppearance(  
      short&  nAppearance  
   );  
  
```  
  
### Parameters  
 `nAppearance`  
 The property **DISPID_AMBIENT_APPEARANCE**.  
  
### Return Value  
 One of the standard HRESULT values.  
  
### Example  
 [!CODE [NVC_ATL_COM#22](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#22)]  
  
##  <a name="ccomcontrolbase__getambientautoclip"></a>  CComControlBase::GetAmbientAutoClip  
 Retrieves **DISPID_AMBIENT_AUTOCLIP**, a flag indicating whether the container supports automatic clipping of the control display area.  
  
```  
  
HRESULT GetAmbientAutoClip(  
      BOOL&  bAutoClip  
   );  
  
```  
  
### Parameters  
 *bAutoClip*  
 The property **DISPID_AMBIENT_AUTOCLIP**.  
  
### Return Value  
 One of the standard HRESULT values.  
  
##  <a name="ccomcontrolbase__getambientbackcolor"></a>  CComControlBase::GetAmbientBackColor  
 Retrieves **DISPID_AMBIENT_BACKCOLOR**, the ambient background color for all controls, defined by the container.  
  
```  
  
HRESULT GetAmbientBackColor(  
      OLE_COLOR&  BackColor  
   );  
  
```  
  
### Parameters  
 *BackColor*  
 The property **DISPID_AMBIENT_BACKCOLOR**.  
  
### Return Value  
 One of the standard HRESULT values.  
  
##  <a name="ccomcontrolbase__getambientcharset"></a>  CComControlBase::GetAmbientCharSet  
 Retrieves **DISPID_AMBIENT_CHARSET**, the ambient character set for all controls, defined by the container.  
  
```  
  
HRESULT GetAmbientCharSet(  
      BSTR&  bstrCharSet  
   );  
  
```  
  
### Parameters  
 *bstrCharSet*  
 The property **DISPID_AMBIENT_CHARSET**.  
  
### Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
##  <a name="ccomcontrolbase__getambientcodepage"></a>  CComControlBase::GetAmbientCodePage  
 Retrieves **DISPID_AMBIENT_CODEPAGE**, the ambient code page for all controls, defined by the container.  
  
```  
  
HRESULT GetAmbientCodePage(  
      ULONG&  ulCodePage  
   );  
  
```  
  
### Parameters  
 *ulCodePage*  
 The property **DISPID_AMBIENT_CODEPAGE**.  
  
### Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
##  <a name="ccomcontrolbase__getambientdisplayasdefault"></a>  CComControlBase::GetAmbientDisplayAsDefault  
 Retrieves **DISPID_AMBIENT_DISPLAYASDEFAULT**, a flag that is **TRUE** if the container has marked the control in this site to be a default button, and therefore a button control should draw itself with a thicker frame.  
  
```  
  
HRESULT GetAmbientDisplayAsDefault(  
      BOOL&  bDisplayAsDefault  
   );  
  
```  
  
### Parameters  
 `bDisplayAsDefault`  
 The property **DISPID_AMBIENT_DISPLAYASDEFAULT**.  
  
### Return Value  
 One of the standard HRESULT values.  
  
##  <a name="ccomcontrolbase__getambientdisplayname"></a>  CComControlBase::GetAmbientDisplayName  
 Retrieves **DISPID_AMBIENT_DISPLAYNAME**, the name the container has supplied to the control.  
  
```  
  
HRESULT GetAmbientDisplayName(  
      BSTR&  bstrDisplayName  
   );  
  
```  
  
### Parameters  
 *bstrDisplayName*  
 The property **DISPID_AMBIENT_DISPLAYNAME**.  
  
### Return Value  
 One of the standard HRESULT values.  
  
##  <a name="ccomcontrolbase__getambientfont"></a>  CComControlBase::GetAmbientFont  
 Retrieves a pointer to the container's ambient `IFont` interface.  
  
```  
  
HRESULT GetAmbientFont(  
      IFont**  ppFont  
   );  
  
```  
  
### Parameters  
 `ppFont`  
 A pointer to the container's ambient [IFont](http://msdn.microsoft.com/library/windows/desktop/ms680673) interface.  
  
### Return Value  
 One of the standard HRESULT values.  
  
### Remarks  
 If the property is **NULL**, the pointer is **NULL**. If the pointer is not **NULL**, the caller must release the pointer.  
  
##  <a name="ccomcontrolbase__getambientfontdisp"></a>  CComControlBase::GetAmbientFontDisp  
 Retrieves a pointer to the container's ambient **IFontDisp** dispatch interface.  
  
```  
  
HRESULT GetAmbientFontDisp(  
      IFontDisp**  ppFont  
   );  
  
```  
  
### Parameters  
 `ppFont`  
 A pointer to the container's ambient [IFontDisp](http://msdn.microsoft.com/library/windows/desktop/ms692695) dispatch interface.  
  
### Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
### Remarks  
 If the property is **NULL**, the pointer is **NULL**. If the pointer is not **NULL**, the caller must release the pointer.  
  
##  <a name="ccomcontrolbase__getambientforecolor"></a>  CComControlBase::GetAmbientForeColor  
 Retrieves **DISPID_AMBIENT_FORECOLOR**, the ambient foreground color for all controls, defined by the container.  
  
```  
  
HRESULT GetAmbientForeColor(  
      OLE_COLOR&  ForeColor  
   );  
  
```  
  
### Parameters  
 *ForeColor*  
 The property **DISPID_AMBIENT_FORECOLOR**.  
  
### Return Value  
 One of the standard HRESULT values.  
  
##  <a name="ccomcontrolbase__getambientlocaleid"></a>  CComControlBase::GetAmbientLocaleID  
 Retrieves **DISPID_AMBIENT_LOCALEID**, the identifier of the language used by the container.  
  
```  
  
HRESULT GetAmbientLocaleID(  
      LCID&  lcid  
   );  
  
```  
  
### Parameters  
 `lcid`  
 The property **DISPID_AMBIENT_LOCALEID**.  
  
### Return Value  
 One of the standard HRESULT values.  
  
### Remarks  
 The control can use this identifier to adapt its user interface to different languages.  
  
##  <a name="ccomcontrolbase__getambientmessagereflect"></a>  CComControlBase::GetAmbientMessageReflect  
 Retrieves **DISPID_AMBIENT_MESSAGEREFLECT**, a flag indicating whether the container wants to receive window messages (such as `WM_DRAWITEM`) as events.  
  
```  
  
HRESULT GetAmbientMessageReflect(  
      BOOL&  bMessageReflect  
   );  
  
```  
  
### Parameters  
 `bMessageReflect`  
 The property **DISPID_AMBIENT_MESSAGEREFLECT**.  
  
### Return Value  
 One of the standard HRESULT values.  
  
##  <a name="ccomcontrolbase__getambientpalette"></a>  CComControlBase::GetAmbientPalette  
 Retrieves **DISPID_AMBIENT_PALETTE**, used to access the container's `HPALETTE`.  
  
```  
  
HRESULT GetAmbientPalette(  
      HPALETTE&  hPalette  
   );  
  
```  
  
### Parameters  
 `hPalette`  
 The property **DISPID_AMBIENT_PALETTE**.  
  
### Return Value  
 One of the standard HRESULT values.  
  
##  <a name="ccomcontrolbase__getambientproperty"></a>  CComControlBase::GetAmbientProperty  
 Retrieves the container property specified by `dispid`.  
  
```  
  
HRESULT GetAmbientProperty(  
      DISPID dispid,  
      VARIANT& var  
   );  
  
```  
  
### Parameters  
 `dispid`  
 Identifier of the container property to be retrieved.  
  
 `var`  
 Variable to receive the property.  
  
### Return Value  
 One of the standard HRESULT values.  
  
### Remarks  
 ATL has provided a set of helper functions to retrieve specific properties, for example, [CComControlBase::GetAmbientBackColor](../vs140/CComControlBase--GetAmbientBackColor.md). If there is no suitable method available, use `GetAmbientProperty`.  
  
##  <a name="ccomcontrolbase__getambientrighttoleft"></a>  CComControlBase::GetAmbientRightToLeft  
 Retrieves **DISPID_AMBIENT_RIGHTTOLEFT**, the direction in which content is displayed by the container.  
  
```  
  
HRESULT GetAmbientRightToLeft(  
      BOOL&  bRightToLeft  
   );  
  
```  
  
### Parameters  
 *bRightToLeft*  
 The property **DISPID_AMBIENT_RIGHTTOLEFT**. Set to **TRUE** if content is displayed right to left,                                 **FALSE** if it is displayed left to right.  
  
### Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
##  <a name="ccomcontrolbase__getambientscaleunits"></a>  CComControlBase::GetAmbientScaleUnits  
 Retrieves **DISPID_AMBIENT_SCALEUNITS**, the container's ambient units (such as inches or centimeters) for labeling displays.  
  
```  
  
HRESULT GetAmbientScaleUnits(  
      BSTR&  bstrScaleUnits  
   );  
  
```  
  
### Parameters  
 *bstrScaleUnits*  
 The property **DISPID_AMBIENT_SCALEUNITS**.  
  
### Return Value  
 One of the standard HRESULT values.  
  
##  <a name="ccomcontrolbase__getambientshowgrabhandles"></a>  CComControlBase::GetAmbientShowGrabHandles  
 Retrieves **DISPID_AMBIENT_SHOWGRABHANDLES**, a flag indicating whether the container allows the control to display grab handles for itself when active.  
  
```  
  
HRESULT GetAmbientShowGrabHandles(  
      BOOL&  bShowGrabHandles  
   );  
  
```  
  
### Parameters  
 *bShowGrabHandles*  
 The property **DISPID_AMBIENT_SHOWGRABHANDLES**.  
  
### Return Value  
 One of the standard HRESULT values.  
  
##  <a name="ccomcontrolbase__getambientshowhatching"></a>  CComControlBase::GetAmbientShowHatching  
 Retrieves **DISPID_AMBIENT_SHOWHATCHING**, a flag indicating whether the container allows the control to display itself with a hatched pattern when the control's user interface is active.  
  
```  
  
HRESULT GetAmbientShowHatching(  
      BOOL&  bShowHatching  
   );  
  
```  
  
### Parameters  
 *bShowHatching*  
 The property **DISPID_AMBIENT_SHOWHATCHING**.  
  
### Return Value  
 One of the standard HRESULT values.  
  
##  <a name="ccomcontrolbase__getambientsupportsmnemonics"></a>  CComControlBase::GetAmbientSupportsMnemonics  
 Retrieves **DISPID_AMBIENT_SUPPORTSMNEMONICS**, a flag indicating whether the container supports keyboard mnemonics.  
  
```  
  
HRESULT GetAmbientSupportsMnemonics(  
      BOOL&  bSupportsMnemonics  
   );  
  
```  
  
### Parameters  
 *bSupportsMnemonics*  
 The property **DISPID_AMBIENT_SUPPORTSMNEMONICS**.  
  
### Return Value  
 One of the standard HRESULT values.  
  
##  <a name="ccomcontrolbase__getambienttextalign"></a>  CComControlBase::GetAmbientTextAlign  
 Retrieves **DISPID_AMBIENT_TEXTALIGN**, the text alignment preferred by the container: 0 for general alignment (numbers right, text left), 1 for left alignment, 2 for center alignment, and 3 for right alignment.  
  
```  
  
HRESULT GetAmbientTextAlign(  
      short&  nTextAlign  
   );  
  
```  
  
### Parameters  
 *nTextAlign*  
 The property **DISPID_AMBIENT_TEXTALIGN**.  
  
### Return Value  
 One of the standard HRESULT values.  
  
##  <a name="ccomcontrolbase__getambienttoptobottom"></a>  CComControlBase::GetAmbientTopToBottom  
 Retrieves **DISPID_AMBIENT_TOPTOBOTTOM**, the direction in which content is displayed by the container.  
  
```  
  
HRESULT GetAmbientTopToBottom(  
      BOOL&  bTopToBottom  
   );  
  
```  
  
### Parameters  
 *bTopToBottom*  
 The property **DISPID_AMBIENT_TOPTOBOTTOM**. Set to **TRUE** if text is displayed top to bottom,                                 **FALSE** if it is displayed bottom to top.  
  
### Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
##  <a name="ccomcontrolbase__getambientuidead"></a>  CComControlBase::GetAmbientUIDead  
 Retrieves **DISPID_AMBIENT_UIDEAD**, a flag indicating whether the container wants the control to respond to user-interface actions.  
  
```  
  
HRESULT GetAmbientUIDead(  
      BOOL&  bUIDead  
   );  
  
```  
  
### Parameters  
 *bUIDead*  
 The property **DISPID_AMBIENT_UIDEAD**.  
  
### Return Value  
 One of the standard HRESULT values.  
  
### Remarks  
 If **TRUE**, the control should not respond. This flag applies regardless of the **DISPID_AMBIENT_USERMODE** flag. See [CComControlBase::GetAmbientUserMode](../vs140/CComControlBase--GetAmbientUserMode.md).  
  
##  <a name="ccomcontrolbase__getambientusermode"></a>  CComControlBase::GetAmbientUserMode  
 Retrieves **DISPID_AMBIENT_USERMODE**, a flag indicating whether the container is in run-mode (                **TRUE**) or design-mode (                **FALSE**).  
  
```  
  
HRESULT GetAmbientUserMode(  
      BOOL&  bUserMode  
   );  
  
```  
  
### Parameters  
 `bUserMode`  
 The property **DISPID_AMBIENT_USERMODE**.  
  
### Return Value  
 One of the standard HRESULT values.  
  
##  <a name="ccomcontrolbase__getdirty"></a>  CComControlBase::GetDirty  
 Returns the value of data member `m_bRequiresSave`.  
  
```  
  
BOOL GetDirty( );  
  
```  
  
### Return Value  
 Returns the value of data member [m_bRequiresSave](../vs140/CComControlBase--m_bRequiresSave.md).  
  
### Remarks  
 This value is set using [CComControlBase::SetDirty](../vs140/CComControlBase--SetDirty.md).  
  
##  <a name="ccomcontrolbase__getzoominfo"></a>  CComControlBase::GetZoomInfo  
 Retrieves the x and y values of the numerator and denominator of the zoom factor for a control activated for in-place editing.  
  
```  
  
void GetZoomInfo(  
      ATL_DRAWINFO&  di  
   );  
  
```  
  
### Parameters  
 `di`  
 The structure that will hold the zoom factor's numerator and denominator. For more information, see [ATL_DRAWINFO](../vs140/ATL_DRAWINFO-Structure.md).  
  
### Remarks  
 The zoom factor is the proportion of the control's natural size to its current extent.  
  
##  <a name="ccomcontrolbase__inplaceactivate"></a>  CComControlBase::InPlaceActivate  
 Causes the control to transition from the inactive state to whatever state the verb in `iVerb` indicates.  
  
```  
  
HRESULT InPlaceActivate(  
      LONG  iVerb,  
      const RECT*  prcPosRect =                 NULL  
   );  
  
```  
  
### Parameters  
 `iVerb`  
 Value indicating the action to be performed by [IOleObjectImpl::DoVerb](../vs140/IOleObjectImpl--DoVerb.md).  
  
 *prcPosRect*  
 Pointer to the position of the in-place control.  
  
### Return Value  
 One of the standard HRESULT values.  
  
### Remarks  
 Before activation, this method checks that the control has a client site, checks how much of the control is visible, and gets the control's location in the parent window. After the control is activated, this method activates the control's user interface and tells the container to make the control visible.  
  
 This method also retrieves an `IOleInPlaceSite`,                         **IOleInPlaceSiteEx**, or **IOleInPlaceSiteWindowless** interface pointer for the control and stores it in the control class's data member [CComControlBase::m_spInPlaceSite](../vs140/CComControlBase--m_spInPlaceSite.md). The control class data members [CComControlBase::m_bInPlaceSiteEx](../vs140/CComControlBase--m_bInPlaceSiteEx.md), [CComControlBase::m_bWndLess](../vs140/CComControlBase--m_bWndLess.md), [CComControlBase::m_bWasOnceWindowless](../vs140/CComControlBase--m_bWasOnceWindowless.md), and [CComControlBase::m_bNegotiatedWnd](../vs140/CComControlBase--m_bNegotiatedWnd.md) are set to true as appropriate.  
  
##  <a name="ccomcontrolbase__internalgetsite"></a>  CComControlBase::InternalGetSite  
 Call this method to query the control site for a pointer to the identified interface.  
  
```  
  
HRESULT InternalGetSite(  
      REFIID  riid,  
      void**  ppUnkSite  
   );  
  
```  
  
### Parameters  
 `riid`  
 The IID of the interface pointer that should be returned in `ppUnkSite`.  
  
 `ppUnkSite`  
 Address of the pointer variable that receives the interface pointer requested in `riid`.  
  
### Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
### Remarks  
 If the site supports the interface requested in `riid`, the pointer is returned by means of `ppUnkSite`. Otherwise, `ppUnkSite` is set to NULL.  
  
##  <a name="ccomcontrolbase__m_bautosize"></a>  CComControlBase::m_bAutoSize  
 Flag indicating the control cannot be any other size.  
  
```  
  
unsigned  
   m_bAutoSize:1;  
  
```  
  
### Remarks  
 This flag is checked by `IOleObjectImpl::SetExtent` and, if **TRUE**, causes the function to return **E_FAIL**.  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
 If you add the **Auto Size** option on the [Stock Properties](../vs140/Stock-Properties--ATL-Control-Wizard.md) tab of the ATL Control Wizard, the wizard automatically creates this data member in your control class, creates put and get methods for the property, and supports [IPropertyNotifySink](http://msdn.microsoft.com/library/windows/desktop/ms692638) to automatically notify the container when the property changes.  
  
##  <a name="ccomcontrolbase__m_bdrawfromnatural"></a>  CComControlBase::m_bDrawFromNatural  
 Flag indicating that `IDataObjectImpl::GetData` and `CComControlBase::GetZoomInfo` should set the control size from `m_sizeNatural` rather than from `m_sizeExtent`.  
  
```  
  
unsigned  
   m_bDrawFromNatural:1;  
  
```  
  
### Remarks  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
##  <a name="ccomcontrolbase__m_bdrawgetdatainhimetric"></a>  CComControlBase::m_bDrawGetDataInHimetric  
 Flag indicating that `IDataObjectImpl::GetData` should use HIMETRIC units and not pixels when drawing.  
  
```  
  
unsigned  
   m_bDrawGetDataInHimetric:1;  
  
```  
  
### Remarks  
 Each logical HIMETRIC unit is 0.01 millimeter.  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
##  <a name="ccomcontrolbase__m_binplaceactive"></a>  CComControlBase::m_bInPlaceActive  
 Flag indicating the control is in-place active.  
  
```  
  
unsigned  
   m_bInPlaceActive:1;  
  
```  
  
### Remarks  
 This means the control is visible and its window, if any, is visible, but its menus and toolbars may not be active. The `m_bUIActive` flag indicates the control's user interface, such as menus, is also active.  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
##  <a name="ccomcontrolbase__m_binplacesiteex"></a>  CComControlBase::m_bInPlaceSiteEx  
 Flag indicating the container supports the **IOleInPlaceSiteEx** interface and OCX96 control features, such as windowless and flicker-free controls.  
  
```  
  
unsigned  
   m_bInPlaceSiteEx:1;  
  
```  
  
### Remarks  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
 The data member `m_spInPlaceSite` points to an [IOleInPlaceSite](http://msdn.microsoft.com/library/windows/desktop/ms686586), [IOleInPlaceSiteEx](http://msdn.microsoft.com/library/windows/desktop/ms693461), or [IOleInPlaceSiteWindowless](http://msdn.microsoft.com/library/windows/desktop/ms682300) interface, depending on the value of the `m_bWndLess` and `m_bInPlaceSiteEx` flags. (The data member `m_bNegotiatedWnd` must be **TRUE** for the `m_spInPlaceSite` pointer to be valid.)  
  
 If `m_bWndLess` is **FALSE** and `m_bInPlaceSiteEx` is **TRUE**, `m_spInPlaceSite` is an **IOleInPlaceSiteEx** interface pointer. See [m_spInPlaceSite](../vs140/CComControlBase--m_spInPlaceSite.md) for a table showing the relationship among these three data members.  
  
##  <a name="ccomcontrolbase__m_bnegotiatedwnd"></a>  CComControlBase::m_bNegotiatedWnd  
 Flag indicating whether or not the control has negotiated with the container about support for OCX96 control features (such as flicker-free and windowless controls), and whether the control is windowed or windowless.  
  
```  
  
unsigned  
   m_bNegotiatedWnd:1;  
  
```  
  
### Remarks  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
 The `m_bNegotiatedWnd` flag must be **TRUE** for the `m_spInPlaceSite` pointer to be valid.  
  
##  <a name="ccomcontrolbase__m_brecomposeonresize"></a>  CComControlBase::m_bRecomposeOnResize  
 Flag indicating the control wants to recompose its presentation when the container changes the control's display size.  
  
```  
  
unsigned  
   m_bRecomposeOnResize:1;  
  
```  
  
### Remarks  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
 This flag is checked by [IOleObjectImpl::SetExtent](../vs140/IOleObjectImpl--SetExtent.md) and, if **TRUE**, `SetExtent` notifies the container of view changes. if this flag is set, the **OLEMISC_RECOMPOSEONRESIZE** bit in the [OLEMISC](http://msdn.microsoft.com/library/windows/desktop/ms678497) enumeration should also be set.  
  
##  <a name="ccomcontrolbase__m_brequiressave"></a>  CComControlBase::m_bRequiresSave  
 Flag indicating the control has changed since it was last saved.  
  
```  
  
unsigned  
   m_bRequiresSave:1;  
  
```  
  
### Remarks  
 The value of `m_bRequiresSave` can be set with [CComControlBase::SetDirty](../vs140/CComControlBase--SetDirty.md) and retrieved with [CComControlBase::GetDirty](../vs140/CComControlBase--GetDirty.md).  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
##  <a name="ccomcontrolbase__m_bresizenatural"></a>  CComControlBase::m_bResizeNatural  
 Flag indicating the control wants to resize its natural extent (its unscaled physical size) when the container changes the control's display size.  
  
```  
  
unsigned  
   m_bResizeNatural:1;  
  
```  
  
### Remarks  
 This flag is checked by `IOleObjectImpl::SetExtent` and, if **TRUE**, the size passed into `SetExtent` is assigned to `m_sizeNatural`.  
  
 The size passed into `SetExtent` is always assigned to `m_sizeExtent`, regardless of the value of `m_bResizeNatural`.  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
##  <a name="ccomcontrolbase__m_buiactive"></a>  CComControlBase::m_bUIActive  
 Flag indicating the control's user interface, such as menus and toolbars, is active.  
  
```  
  
unsigned  
   m_bUIActive:1;  
  
```  
  
### Remarks  
 The `m_bInPlaceActive` flag indicates that the control is active, but not that its user interface is active.  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
##  <a name="ccomcontrolbase__m_busingwindowrgn"></a>  CComControlBase::m_bUsingWindowRgn  
 Flag indicating the control is using the container-supplied window region.  
  
```  
  
unsigned  
   m_bUsingWindowRgn:1;  
  
```  
  
### Remarks  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
##  <a name="ccomcontrolbase__m_bwasoncewindowless"></a>  CComControlBase::m_bWasOnceWindowless  
 Flag indicating the control has been windowless, but may or may not be windowless now.  
  
```  
  
unsigned  
   m_bWasOnceWindowless:1;  
  
```  
  
### Remarks  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
##  <a name="ccomcontrolbase__m_bwindowonly"></a>  CComControlBase::m_bWindowOnly  
 Flag indicating the control should be windowed, even if the container supports windowless controls.  
  
```  
  
unsigned  
   m_bWindowOnly:1;  
  
```  
  
### Remarks  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
##  <a name="ccomcontrolbase__m_bwndless"></a>  CComControlBase::m_bWndLess  
 Flag indicating the control is windowless.  
  
```  
  
unsigned  
   m_bWndLess:1;  
  
```  
  
### Remarks  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
 The data member `m_spInPlaceSite` points to an [IOleInPlaceSite](http://msdn.microsoft.com/library/windows/desktop/ms686586), [IOleInPlaceSiteEx](http://msdn.microsoft.com/library/windows/desktop/ms693461), or [IOleInPlaceSiteWindowless](http://msdn.microsoft.com/library/windows/desktop/ms682300) interface, depending on the value of the `m_bWndLess` and [CComControlBase::m_bInPlaceSiteEx](../vs140/CComControlBase--m_bInPlaceSiteEx.md) flags. (The data member [CComControlBase::m_bNegotiatedWnd](../vs140/CComControlBase--m_bNegotiatedWnd.md) must be **TRUE** for the [CComControlBase::m_spInPlaceSite](../vs140/CComControlBase--m_spInPlaceSite.md) pointer to be valid.)  
  
 If `m_bWndLess` is **TRUE**, `m_spInPlaceSite` is an **IOleInPlaceSiteWindowless** interface pointer. See [CComControlBase::m_spInPlaceSite](../vs140/CComControlBase--m_spInPlaceSite.md) for a table showing the complete relationship between these data members.  
  
##  <a name="ccomcontrolbase__m_hwndcd"></a>  CComControlBase::m_hWndCD  
 Contains a reference to the window handle associated with the control.  
  
```  
  
HWND& m_hWndCD;  
  
```  
  
### Remarks  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
##  <a name="ccomcontrolbase__m_nfreezeevents"></a>  CComControlBase::m_nFreezeEvents  
 A count of the number of times the container has frozen events (refused to accept events) without an intervening thaw of events (acceptance of events).  
  
```  
  
short  
   m_nFreezeEvents;  
  
```  
  
### Remarks  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
##  <a name="ccomcontrolbase__m_rcpos"></a>  CComControlBase::m_rcPos  
 The position in pixels of the control, expressed in the coordinates of the container.  
  
```  
  
RECT  
   m_rcPos;  
  
```  
  
### Remarks  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
##  <a name="ccomcontrolbase__m_sizeextent"></a>  CComControlBase::m_sizeExtent  
 The extent of the control in HIMETRIC units (each unit is 0.01 millimeters) for a particular display.  
  
```  
  
SIZE  
   m_sizeExtent;  
  
```  
  
### Remarks  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
 This size is scaled by the display. The control's physical size is specified in the `m_sizeNatural` data member and is fixed.  
  
 You can convert the size to pixels with the global function [AtlHiMetricToPixel](../vs140/AtlHiMetricToPixel.md).  
  
##  <a name="ccomcontrolbase__m_sizenatural"></a>  CComControlBase::m_sizeNatural  
 The physical size of the control in HIMETRIC units (each unit is 0.01 millimeters).  
  
```  
  
SIZE  
   m_sizeNatural;  
  
```  
  
### Remarks  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
 This size is fixed, while the size in `m_sizeExtent` is scaled by the display.  
  
 You can convert the size to pixels with the global function [AtlHiMetricToPixel](../vs140/AtlHiMetricToPixel.md).  
  
##  <a name="ccomcontrolbase__m_spadvisesink"></a>  CComControlBase::m_spAdviseSink  
 A direct pointer to the advisory connection on the container (the container's [IAdviseSink](http://msdn.microsoft.com/library/windows/desktop/ms692513)).  
  
```  
  
CComPtr<IAdviseSink>  
   m_spAdviseSink;  
  
```  
  
### Remarks  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
##  <a name="ccomcontrolbase__m_spambientdispatch"></a>  CComControlBase::m_spAmbientDispatch  
 A `CComDispatchDriver` object that lets you retrieve and set an object's properties through an `IDispatch` pointer.  
  
```  
  
CComDispatchDriver  
   m_spAmbientDispatch;  
  
```  
  
### Remarks  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
##  <a name="ccomcontrolbase__m_spclientsite"></a>  CComControlBase::m_spClientSite  
 A pointer to the control's client site within the container.  
  
```  
  
CComPtr<IOleClientSite>  
   m_spClientSite;  
  
```  
  
### Remarks  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
##  <a name="ccomcontrolbase__m_spdataadviseholder"></a>  CComControlBase::m_spDataAdviseHolder  
 Provides a standard means to hold advisory connections between data objects and advise sinks.  
  
```  
  
CComPtr<IDataAdviseHolder>  
   m_spDataAdviseHolder;  
  
```  
  
### Remarks  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
 A data object is a control that can transfer data and that implements [IDataObject](http://msdn.microsoft.com/library/windows/desktop/ms688421), whose methods specify the format and transfer medium of the data.  
  
 The interface `m_spDataAdviseHolder` implements the [IDataObject::DAdvise](http://msdn.microsoft.com/library/windows/desktop/ms692579) and [IDataObject::DUnadvise](http://msdn.microsoft.com/library/windows/desktop/ms692448) methods to establish and delete advisory connections to the container. The control's container must implement an advise sink by supporting the [IAdviseSink](http://msdn.microsoft.com/library/windows/desktop/ms692513) interface.  
  
##  <a name="ccomcontrolbase__m_spinplacesite"></a>  CComControlBase::m_spInPlaceSite  
 A pointer to the container's [IOleInPlaceSite](http://msdn.microsoft.com/library/windows/desktop/ms686586), [IOleInPlaceSiteEx](http://msdn.microsoft.com/library/windows/desktop/ms693461), or [IOleInPlaceSiteWindowless](http://msdn.microsoft.com/library/windows/desktop/ms682300) interface pointer.  
  
```  
  
CComPtr<IOleInPlaceSiteWindowless>  
   m_spInPlaceSite;  
  
```  
  
### Remarks  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
 The `m_spInPlaceSite` pointer is valid only if the [m_bNegotiatedWnd](../vs140/CComControlBase--m_bNegotiatedWnd.md) flag is **TRUE**.  
  
 The following table shows how the `m_spInPlaceSite` pointer type depends on the [m_bWndLess](../vs140/CComControlBase--m_bWndLess.md) and [m_bInPlaceSiteEx](../vs140/CComControlBase--m_bInPlaceSiteEx.md) data member flags:  
  
|m_spInPlaceSite Type|m_bWndLess Value|m_bInPlaceSiteEx Value|  
|---------------------------|-----------------------|-----------------------------|  
|**IOleInPlaceSiteWindowless**|**TRUE**|**TRUE** or **FALSE**|  
|**IOleInPlaceSiteEx**|**FALSE**|**TRUE**|  
|`IOleInPlaceSite`|**FALSE**|**FALSE**|  
  
##  <a name="ccomcontrolbase__m_spoleadviseholder"></a>  CComControlBase::m_spOleAdviseHolder  
 Provides a standard implementation of a way to hold advisory connections.  
  
```  
  
CComPtr<IOleAdviseHolder>  
   m_spOleAdviseHolder;  
  
```  
  
### Remarks  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
 The interface `m_spOleAdviseHolder` implements the [IOleObject::Advise](http://msdn.microsoft.com/library/windows/desktop/ms686573) and [IOleObject::Unadvise](http://msdn.microsoft.com/library/windows/desktop/ms693749) methods to establish and delete advisory connections to the container. The control's container must implement an advise sink by supporting the [IAdviseSink](http://msdn.microsoft.com/library/windows/desktop/ms692513) interface.  
  
##  <a name="ccomcontrolbase__ondraw"></a>  CComControlBase::OnDraw  
 Override this method to draw your control.  
  
```  
  
virtual HRESULT OnDraw(  
      ATL_DRAWINFO&  di  
   );  
  
```  
  
### Parameters  
 `di`  
 A reference to the [ATL_DRAWINFO](../vs140/ATL_DRAWINFO-Structure.md) structure that contains drawing information such as the draw aspect, the control bounds, and whether the drawing is optimized or not.  
  
### Return Value  
 A standard `HRESULT` value.  
  
### Remarks  
 The default `OnDraw` deletes or restores the device context or does nothing, depending on flags set in [CComControlBase::OnDrawAdvanced](../vs140/CComControlBase--OnDrawAdvanced.md).  
  
 An `OnDraw` method is automatically added to your control class when you create your control with the ATL Control Wizard. The wizard's default `OnDraw` draws a rectangle with the label "ATL 8.0".  
  
### Example  
 See the example for [CComControlBase::GetAmbientAppearance](../vs140/CComControlBase--GetAmbientAppearance.md).  
  
##  <a name="ccomcontrolbase__ondrawadvanced"></a>  CComControlBase::OnDrawAdvanced  
 The default `OnDrawAdvanced` prepares a normalized device context for drawing, then calls your control class's `OnDraw` method.  
  
```  
  
virtual HRESULT OnDrawAdvanced(  
      ATL_DRAWINFO&  di  
   );  
  
```  
  
### Parameters  
 `di`  
 A reference to the [ATL_DRAWINFO](../vs140/ATL_DRAWINFO-Structure.md) structure that contains drawing information such as the draw aspect, the control bounds, and whether the drawing is optimized or not.  
  
### Return Value  
 A standard `HRESULT` value.  
  
### Remarks  
 Override this method if you want to accept the device context passed by the container without normalizing it.  
  
 See [CComControlBase::OnDraw](../vs140/CComControlBase--OnDraw.md) for more details.  
  
##  <a name="ccomcontrolbase__onkillfocus"></a>  CComControlBase::OnKillFocus  
 Checks that the control is in-place active and has a valid control site, then informs the container that the control has lost focus.  
  
```  
LRESULT OnKillFocus(  
   UINT /* nMsg */,  
   WPARAM /* wParam */,  
   LPARAM /* lParam */,  
   BOOL& bHandled   
);  
```  
  
### Parameters  
 `nMsg`  
 Reserved.  
  
 `wParam`  
 Reserved.  
  
 `lParam`  
 Reserved.  
  
 `bHandled`  
 Flag that indicates whether the window message was successfully handled. The default is `FALSE`.  
  
### Return Value  
 Always returns 1.  
  
##  <a name="ccomcontrolbase__onmouseactivate"></a>  CComControlBase::OnMouseActivate  
 Checks that the UI is in user mode, then activates the control.  
  
```  
LRESULT OnMouseActivate(  
   UINT /* nMsg */,  
   WPARAM /* wParam */,  
   LPARAM /* lParam */,  
   BOOL& bHandled   
);  
```  
  
### Parameters  
 `nMsg`  
 Reserved.  
  
 `wParam`  
 Reserved.  
  
 `lParam`  
 Reserved.  
  
 `bHandled`  
 Flag that indicates whether the window message was successfully handled. The default is `FALSE`.  
  
### Return Value  
 Always returns 1.  
  
##  <a name="ccomcontrolbase__onpaint"></a>  CComControlBase::OnPaint  
 Prepares the container for painting, gets the control's client area, then calls the control class's `OnDrawAdvanced` method.  
  
```  
  
LRESULT OnPaint(  
      UINT /* nMsg */                ,  
   WPARAM  wParam,  
   LPARAM /* lParam */                ,  
   BOOL& /* lResult */   
   );  
  
```  
  
### Parameters  
 `nMsg`  
 Reserved.  
  
 `wParam`  
 An existing HDC.  
  
 `lParam`  
 Reserved.  
  
 `lResult`  
 Reserved.  
  
### Return Value  
 Always returns zero.  
  
### Remarks  
 If `wParam` is not NULL, `OnPaint` assumes it contains a valid HDC and uses it instead of [CComControlBase::m_hWndCD](../vs140/CComControlBase--m_hWndCD.md).  
  
##  <a name="ccomcontrolbase__onsetfocus"></a>  CComControlBase::OnSetFocus  
 Checks that the control is in-place active and has a valid control site, then informs the container the control has gained focus.  
  
```  
LRESULT OnSetFocus(  
   UINT /* nMsg */,  
   WPARAM /* wParam */,  
   LPARAM /* lParam */,  
   BOOL& bHandled   
);  
```  
  
### Parameters  
 `nMsg`  
 Reserved.  
  
 `wParam`  
 Reserved.  
  
 `lParam`  
 Reserved.  
  
 `bHandled`  
 Flag that indicates whether the window message was successfully handled. The default is `FALSE`.  
  
### Return Value  
 Always returns 1.  
  
### Remarks  
 Sends a notification to the container that the control has received focus.  
  
##  <a name="ccomcontrolbase__pretranslateaccelerator"></a>  CComControlBase::PreTranslateAccelerator  
 Override this method to provide your own keyboard accelerator handlers.  
  
```  
  
BOOL PreTranslateAccelerator(  
      LPMSG /* pMsg */,  
      HRESULT& /* hRet */  
   );  
  
```  
  
### Parameters  
 `pMsg`  
 Reserved.  
  
 *hRet*  
 Reserved.  
  
### Return Value  
 By default returns **FALSE**.  
  
##  <a name="ccomcontrolbase__sendonclose"></a>  CComControlBase::SendOnClose  
 Notifies all advisory sinks registered with the advise holder that the control has been closed.  
  
```  
  
HRESULT SendOnClose( );  
  
```  
  
### Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
### Remarks  
 Sends a notification that the control has closed its advisory sinks.  
  
##  <a name="ccomcontrolbase__sendondatachange"></a>  CComControlBase::SendOnDataChange  
 Notifies all advisory sinks registered with the advise holder that the control data has changed.  
  
```  
  
HRESULT SendOnDataChange(  
      DWORD  advf  
    = 0  
   );  
  
```  
  
### Parameters  
 *advf*  
 Advise flags that specify how the call to [IAdviseSink::OnDataChange](http://msdn.microsoft.com/library/windows/desktop/ms687283) is made. Values are from the [ADVF](http://msdn.microsoft.com/library/windows/desktop/ms693742) enumeration.  
  
### Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
##  <a name="ccomcontrolbase__sendonrename"></a>  CComControlBase::SendOnRename  
 Notifies all advisory sinks registered with the advise holder that the control has a new moniker.  
  
```  
  
HRESULT SendOnRename(  
      IMoniker*  pmk  
   );  
  
```  
  
### Parameters  
 *pmk*  
 Pointer to the new moniker of the control.  
  
### Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
### Remarks  
 Sends a notification that the moniker for the control has changed.  
  
##  <a name="ccomcontrolbase__sendonsave"></a>  CComControlBase::SendOnSave  
 Notifies all advisory sinks registered with the advise holder that the control has been saved.  
  
```  
  
HRESULT SendOnSave( );  
  
```  
  
### Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
### Remarks  
 Sends a notification that the control has just saved its data.  
  
##  <a name="ccomcontrolbase__sendonviewchange"></a>  CComControlBase::SendOnViewChange  
 Notifies all registered advisory sinks that the control's view has changed.  
  
```  
  
HRESULT SendOnViewChange(  
      DWORD  dwAspect,  
      LONG  lindex  
    = -1  
   );  
  
```  
  
### Parameters  
 `dwAspect`  
 The aspect or view of the control.  
  
 *lindex*  
 The portion of the view that has changed. Only -1 is valid.  
  
### Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
### Remarks  
 `SendOnViewChange` calls [IAdviseSink::OnViewChange](http://msdn.microsoft.com/library/windows/desktop/ms694337). The only value of *lindex* currently supported is -1, which indicates that the entire view is of interest.  
  
##  <a name="ccomcontrolbase__setcontrolfocus"></a>  CComControlBase::SetControlFocus  
 Sets or removes the keyboard focus to or from the control.  
  
```  
  
BOOL SetControlFocus(  
      BOOL  bGrab  
   );  
  
```  
  
### Parameters  
 *bGrab*  
 If **TRUE**, sets the keyboard focus to the calling control. If **FALSE**, removes the keyboard focus from the calling control, provided it has the focus.  
  
### Return Value  
 Returns **TRUE** if the control successfully receives focus; otherwise,                         **FALSE**.  
  
### Remarks  
 For a windowed control, the Windows API function [SetFocus](http://msdn.microsoft.com/library/windows/desktop/ms646312) is called. For a windowless control, [IOleInPlaceSiteWindowless::SetFocus](http://msdn.microsoft.com/library/windows/desktop/ms679745) is called. Through this call, a windowless control obtains the keyboard focus and can respond to window messages.  
  
##  <a name="ccomcontrolbase__setdirty"></a>  CComControlBase::SetDirty  
 Sets the data member `m_bRequiresSave` to the value in `bDirty`.  
  
```  
  
void SetDirty(  
      BOOL  bDirty  
   );  
  
```  
  
### Parameters  
 `bDirty`  
 Value of the data member [CComControlBase::m_bRequiresSave](../vs140/CComControlBase--m_bRequiresSave.md).  
  
### Remarks  
 **SetDirty(TRUE)** should be called to flag that the control has changed since it was last saved. The value of `m_bRequiresSave` is retrieved with [CComControlBase::GetDirty](../vs140/CComControlBase--GetDirty.md).  
  
## See Also  
 [CComControl Class](../vs140/CComControl-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)