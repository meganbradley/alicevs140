---
title: "AtlAxCreateControlLicEx"
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
ms.assetid: abcbef3f-fcb0-4c87-8524-bff31e31e1b2
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlAxCreateControlLicEx
Creates a licensed ActiveX control, initializes it, and hosts it in the specified window. An interface pointer and event sink for the new control can also be created.  
  
> [!IMPORTANT]
>  This function cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
      ATLAPI AtlAxCreateControlLicEx(  
LPCOLESTR lpszName,   
HWND hWnd,   
IStream* pStream,  
IUnknown** ppUnkContainer,   
IUnknown** ppUnkControl,  
REFIID iidSink = IID_NULL,   
IUnknown* punkSink = NULL,   
BSTR bstrLic= NULL  
);  
```  
  
#### Parameters  
 `lpszName`  
 A pointer to a string to be passed to the control. Must be formatted in one of the following ways:  
  
-   A ProgID such as "MSCAL.Calendar.7"  
  
-   A CLSID such as "{8E27C92B-1264-101C-8A2F-040224009C02}"  
  
-   A URL such as "http://www.microsoft.com"  
  
-   A reference to an Active document such as "file://\\\Documents\MyDoc.doc"  
  
-   A fragment of HTML such as "MSHTML:<HTML\><BODY\>This is a line of text</BODY\></HTML\>"  
  
    > [!NOTE]
    >  "MSHTML:" must precede the HTML fragment so that it is designated as being an MSHTML stream.  
  
 `hWnd`  
 Handle to the window that the control will be attached to.  
  
 `pStream`  
 A pointer to a stream that is used to initialize the properties of the control. Can be **NULL**.  
  
 `ppUnkContainer`  
 The address of a pointer that will receive the **IUnknown** of the container. Can be **NULL**.  
  
 `ppUnkControl`  
 [out] The address of a pointer that will receive the **IUnknown** of the created control. Can be **NULL**.  
  
 `iidSink`  
 The interface identifier of an outgoing interface on the contained object.  
  
 *punkSink*  
 A pointer to the **IUnknown** interface of the sink object to be connected to the connection point specified by `iidSink` on the contained object after the contained object has been successfully created.  
  
 `bstrLic`  
 The BSTR containing the license for the control.  
  
## Return Value  
 One of the standard HRESULT values.  
  
## Remarks  
 `AtlAxCreateControlLicEx` is similar to [AtlAxCreateControlLic](../vs140/AtlAxCreateControlLic.md) but also allows you to receive an interface pointer to the newly created control and set up an event sink to receive events fired by the control.  
  
## Example  
 See [Hosting ActiveX Controls Using ATL AXHost](../vs140/Hosting-ActiveX-Controls-Using-ATL-AXHost.md) for a sample of how to use `AtlAxCreateControlLicEx`.  
  
## Requirements  
 **Header:** atlhost.h  
  
## See Also  
 [Composite Control Global Functions](../vs140/Composite-Control-Global-Functions.md)   
 [Composite Control Fundamentals](../vs140/ATL-Composite-Control-Fundamentals.md)   
 [AtlAxCreateControl](../vs140/AtlAxCreateControl.md)   
 [CAxWindow2T::CreateControlLicEx](../vs140/CAxWindow2T--CreateControlLicEx.md)