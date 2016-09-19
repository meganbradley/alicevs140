---
title: "CAxWindow::CreateControlEx"
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
ms.assetid: c0149ef1-87d8-42c7-a89b-546ff22d6b6e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAxWindow::CreateControlEx
Creates an ActiveX control, initializes it, and hosts it in the specified window.  
  
## Syntax  
  
```  
  
      HRESULT CreateControlEx(  
   LPCOLESTR lpszName,  
   IStream* pStream = NULL,  
   IUnknown** ppUnkContainer = NULL,  
   IUnknown** ppUnkControl = NULL,  
   REFIID iidSink = IID_NULL,  
   IUnknown* punkSink = NULL   
);  
HRESULT CreateControlEx(  
   DWORD dwResID,  
   IStream* pStream = NULL,  
   IUnknown** ppUnkContainer = NULL,  
   IUnknown** ppUnkControl = NULL,  
   REFIID iidSink = IID_NULL,  
   IUnknown* punkSink = NULL   
);  
```  
  
#### Parameters  
 `lpszName`  
 A pointer to a string to create the control. Must be formatted in one of the following ways:  
  
-   A ProgID such as "MSCAL.Calendar.7"  
  
-   A CLSID such as "{8E27C92B-1264-101C-8A2F-040224009C02}"  
  
-   A URL such as "http://www.microsoft.com"  
  
-   A reference to an Active document such as "file://\\\Documents\MyDoc.doc"  
  
-   A fragment of HTML such as "MSHTML:<HTML\><BODY\>This is a line of text</BODY\></HTML\>"  
  
    > [!NOTE]
    >  "MSHTML:" must precede the HTML fragment so that it is designated as being an MSHTML stream. Only the ProgID and CLSID are supported in Windows Mobile platforms. Windows CE embedded platforms, other than Windows Mobile with support for CE IE support all types including ProgID, CLSID, URL, reference to active document, and fragment of HTML.  
  
 `pStream`  
 [in] A pointer to a stream that is used to initialize the properties of the control. Can be **NULL**.  
  
 `ppUnkContainer`  
 [out] The address of a pointer that will receive the **IUnknown** of the container. Can be **NULL**.  
  
 `ppUnkControl`  
 [out] The address of a pointer that will receive the **IUnknown** of the control. Can be **NULL**.  
  
 `iidSink`  
 [in] The interface identifier of an outgoing interface on the contained object. Can be **IID_NULL**.  
  
 *punkSink*  
 [in] A pointer to the **IUnknown** interface of the sink object to be connected to the connection point on the contained object specified by `iidSink`.  
  
 `dwResID`  
 [in] The resource ID of an HTML resource. The WebBrowser control will be created and loaded with the specified resource.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 This method is similar to [CAxWindow::CreateControl](../vs140/CAxWindow--CreateControl.md), but unlike that method, `CreateControlEx` also allows you to receive an interface pointer to the newly created control and set up an event sink to receive events fired by the control.  
  
 See [CAxWindow2T::CreateControlLicEx](../vs140/CAxWindow2T--CreateControlLicEx.md) to create, initialize, and host a licensed ActiveX control.  
  
## Example  
 See [Hosting ActiveX Controls Using ATL AXHost](../vs140/Hosting-ActiveX-Controls-Using-ATL-AXHost.md) for a sample that uses `CreateControlEx`.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CAxWindow Class](../vs140/CAxWindow-Class.md)   
 [AtlAxCreateControlEx](../vs140/AtlAxCreateControlEx.md)