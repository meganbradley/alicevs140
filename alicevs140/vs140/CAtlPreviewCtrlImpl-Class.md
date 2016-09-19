---
title: "CAtlPreviewCtrlImpl Class"
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
ms.assetid: 39b3299e-07e4-4abc-9b6e-b54bfa3b0802
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlPreviewCtrlImpl Class
This class is an ATL implementation of a window that is placed on a host window provided by the Shell  for Rich Preview.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
class CAtlPreviewCtrlImpl : public CWindowImpl<CAtlPreviewCtrlImpl>, public IPreviewCtrl;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CAtlPreviewCtrlImpl::~CAtlPreviewCtrlImpl](../vs140/CAtlPreviewCtrlImpl--~CAtlPreviewCtrlImpl.md)|Destructs a preview control object.|  
|[CAtlPreviewCtrlImpl::CAtlPreviewCtrlImpl](../vs140/CAtlPreviewCtrlImpl--CAtlPreviewCtrlImpl.md)|Constructs a preview control object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CAtlPreviewCtrlImpl::Create](../vs140/CAtlPreviewCtrlImpl--Create.md)|Called by a Rich Preview handler to create the Windows window.|  
|[CAtlPreviewCtrlImpl::Destroy](../vs140/CAtlPreviewCtrlImpl--Destroy.md)|Called by a Rich Preview handler when it needs to destroy this control.|  
|[CAtlPreviewCtrlImpl::Focus](../vs140/CAtlPreviewCtrlImpl--Focus.md)|Sets input focus to this control.|  
|[CAtlPreviewCtrlImpl::OnPaint](../vs140/CAtlPreviewCtrlImpl--OnPaint.md)|Handles the WM_PAINT message.|  
|[CAtlPreviewCtrlImpl::Redraw](../vs140/CAtlPreviewCtrlImpl--Redraw.md)|Tells this control to redraw.|  
|[CAtlPreviewCtrlImpl::SetHost](../vs140/CAtlPreviewCtrlImpl--SetHost.md)|Sets a new parent for this control.|  
|[CAtlPreviewCtrlImpl::SetPreviewVisuals](../vs140/CAtlPreviewCtrlImpl--SetPreviewVisuals.md)|Called by a Rich Preview handler when it needs to set visuals of rich preview content.|  
|[CAtlPreviewCtrlImpl::SetRect](../vs140/CAtlPreviewCtrlImpl--SetRect.md)|Sets a new bounding rectangle for this control.|  
  
### Protected Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CAtlPreviewCtrlImpl::DoPaint](../vs140/CAtlPreviewCtrlImpl--DoPaint.md)|Called by the framework to render the preview.|  
  
### Protected Constants  
  
|Name|Description|  
|----------|-----------------|  
|[CAtlPreviewCtrlImpl::m_plf](../vs140/CAtlPreviewCtrlImpl--m_plf.md)|Font used to display text in the preview window.|  
  
### Protected Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CAtlPreviewCtrlImpl::m_clrBack](../vs140/CAtlPreviewCtrlImpl--m_clrBack.md)|Background color of the preview window.|  
|[CAtlPreviewCtrlImpl::m_clrText](../vs140/CAtlPreviewCtrlImpl--m_clrText.md)|Text color of preview window.|  
  
## Remarks  
  
## Inheritance Hierarchy  
 `TBase`  
  
 `ATL::CMessageMap`  
  
 `ATL::CWindowImplRoot<TBase>`  
  
 `ATL::CWindowImplBaseT<TBase,TWinTraits>`  
  
 [ATL::CWindowImpl<CAtlPreviewCtrlImpl\>](../vs140/CWindowImpl-Class.md)  
  
 `IPreviewCtrl`  
  
 `ATL::CAtlPreviewCtrlImpl`  
  
## Requirements  
 **Header:** atlpreviewctrlimpl.h  
  
##  <a name="catlpreviewctrlimpl__catlpreviewctrlimpl"></a>  CAtlPreviewCtrlImpl::CAtlPreviewCtrlImpl  
 Constructs a preview control object.  
  
```  
CAtlPreviewCtrlImpl(  
   void  
) : m_clrText(0), m_clrBack(RGB(255, 255, 255)), m_plf(NULL);  
```  
  
### Remarks  
  
##  <a name="catlpreviewctrlimpl___dtorcatlpreviewctrlimpl"></a>  CAtlPreviewCtrlImpl::~CAtlPreviewCtrlImpl  
 Destructs a preview control object.  
  
```  
virtual ~CAtlPreviewCtrlImpl(  
   void  
);  
```  
  
### Remarks  
  
##  <a name="catlpreviewctrlimpl__create"></a>  CAtlPreviewCtrlImpl::Create  
 Called by a Rich Preview handler to create the Windows window.  
  
```  
virtual BOOL Create(  
   HWND hWndParent,  
   const RECT* prc  
);  
```  
  
### Parameters  
 `hWndParent`  
 A handle to the host window supplied by the Shell for Rich Preview.  
  
 `prc`  
 Specifies the initial size and position of the window.  
  
### Return Value  
 `TRUE` if successful; otherwise `FALSE`.  
  
### Remarks  
  
##  <a name="catlpreviewctrlimpl__destroy"></a>  CAtlPreviewCtrlImpl::Destroy  
 Called by a Rich Preview handler when it needs to destroy this control.  
  
```  
virtual void Destroy();  
```  
  
### Remarks  
  
##  <a name="catlpreviewctrlimpl__dopaint"></a>  CAtlPreviewCtrlImpl::DoPaint  
 Called by the framework to render the preview.  
  
```  
virtual void DoPaint(  
   HDC hdc  
);  
```  
  
### Parameters  
 `hdc`  
 A handle to a device context for painting.  
  
### Remarks  
  
##  <a name="catlpreviewctrlimpl__focus"></a>  CAtlPreviewCtrlImpl::Focus  
 Sets input focus to this control.  
  
```  
virtual void Focus();  
```  
  
### Remarks  
  
##  <a name="catlpreviewctrlimpl__m_clrback"></a>  CAtlPreviewCtrlImpl::m_clrBack  
 Background color of the preview window.  
  
```  
COLORREF m_clrBack;  
```  
  
### Remarks  
  
##  <a name="catlpreviewctrlimpl__m_clrtext"></a>  CAtlPreviewCtrlImpl::m_clrText  
 Text color of the preview window.  
  
```  
COLORREF m_clrText;  
```  
  
### Remarks  
  
##  <a name="catlpreviewctrlimpl__m_plf"></a>  CAtlPreviewCtrlImpl::m_plf  
 Font used to display text in the preview window.  
  
```  
const LOGFONTW* m_plf;  
```  
  
### Remarks  
  
##  <a name="catlpreviewctrlimpl__onpaint"></a>  CAtlPreviewCtrlImpl::OnPaint  
 Handles the WM_PAINT message.  
  
```  
LRESULT OnPaint(  
   UINT nMsg,  
   WPARAM wParam,  
   LPARAM lParam,  
   BOOL& bHandled  
);  
```  
  
### Parameters  
 `nMsg`  
 Set to WM_PAINT.  
  
 `wParam`  
 This parameter is not used.  
  
 `lParam`  
 This parameter is not used.  
  
 `bHandled`  
 When this function returns, it contains `TRUE`.  
  
### Return Value  
 Always returns 0.  
  
### Remarks  
  
##  <a name="catlpreviewctrlimpl__redraw"></a>  CAtlPreviewCtrlImpl::Redraw  
 Tells this control to redraw.  
  
```  
virtual void Redraw();  
```  
  
### Remarks  
  
##  <a name="catlpreviewctrlimpl__sethost"></a>  CAtlPreviewCtrlImpl::SetHost  
 Sets a new parent for this control.  
  
```  
virtual void SetHost(  
   HWND hWndParent  
);  
```  
  
### Parameters  
 `hWndParent`  
 A handle to the new parent window.  
  
### Remarks  
  
##  <a name="catlpreviewctrlimpl__setpreviewvisuals"></a>  CAtlPreviewCtrlImpl::SetPreviewVisuals  
 Called by a Rich Preview handler when it needs to set visuals of rich preview content.  
  
```  
virtual void SetPreviewVisuals(  
   COLORREF clrBack,  
   COLORREF clrText,  
   const LOGFONTW * plf  
);  
```  
  
### Parameters  
 `clrBack`  
 Background color of the preview window.  
  
 `clrText`  
 Text color of the preview window.  
  
 `plf`  
 Font used to display text in the preview window.  
  
### Remarks  
  
##  <a name="catlpreviewctrlimpl__setrect"></a>  CAtlPreviewCtrlImpl::SetRect  
 Sets a new bounding rectangle for this control.  
  
```  
virtual void SetRect(  
   const RECT* prc,  
   BOOL bRedraw  
);  
```  
  
### Parameters  
 `prc`  
 Specifies the new size and position of the preview control.  
  
 `bRedraw`  
 Specifies whether the control should be redrawn.  
  
### Remarks  
  
## See Also  
 [ATL](../vs140/ATL-COM-Desktop-Components.md)