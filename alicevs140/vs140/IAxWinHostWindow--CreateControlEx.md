---
title: "IAxWinHostWindow::CreateControlEx"
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
ms.assetid: 53b135eb-b896-45b7-8aac-f83db6688db2
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAxWinHostWindow::CreateControlEx
Creates an ActiveX control, initializes it, and hosts it in the specified window, similar to [IAxWinHostWindow::CreateControl](../vs140/IAxWinHostWindow--CreateControl.md).  
  
## Syntax  
  
```  
  
      STDMETHOD( CreateControlEx )(  
   LPCOLESTR lpszTricsData,  
   HWND hWnd,  
   IStream* pStream,  
   IUnknown** ppUnk,  
   REFIID riidAdvise,  
   IUnknown* punkAdvise   
);  
```  
  
#### Parameters  
 `lpTricsData`  
 [in] A string identifying the control to create. Can be a CLSID (must include the braces), ProgID, URL, or raw HTML (prefixed with **MSHTML:**).  
  
 `hWnd`  
 [in] A handle to the window to be used for hosting.  
  
 `pStream`  
 [in] An interface pointer for a stream containing initialization data for the control. Can be **NULL**.  
  
 `ppUnk`  
 [out] The address of a pointer that will receive the **IUnknown** interface of the created control. Can be **NULL**.  
  
 *riidAdvise*  
 [in] The interface identifier of an outgoing interface on the contained object. Can be **IID_NULL**.  
  
 *punkAdvise*  
 [in] A pointer to the **IUnknown** interface of the sink object to be connected to the connection point on the contained object specified by `iidSink`.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 Unlike the `CreateControl` method, `CreateControlEx` also allows you to receive an interface pointer to the newly created control and set up an event sink to receive events fired by the control.  
  
 To create a licensed ActiveX control, see [IAxWinHostWindowLic::CreateControlLicEx](../vs140/IAxWinHostWindowLic--CreateControlLicEx.md).  
  
## Requirements  
 **Header:** atliface.h  
  
## See Also  
 [IAxWinHostWindow Interface](../vs140/IAxWinHostWindow-Interface.md)   
 [IAxWinHostWindow::CreateControl](../vs140/IAxWinHostWindow--CreateControl.md)   
 [IAxWinHostWindow::AttachControl](../vs140/IAxWinHostWindow--AttachControl.md)   
 [CAxWindow::CreateControlEx](../vs140/CAxWindow--CreateControlEx.md)   
 [AtlAxCreateControlEx](../vs140/AtlAxCreateControlEx.md)