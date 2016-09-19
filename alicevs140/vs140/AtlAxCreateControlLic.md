---
title: "AtlAxCreateControlLic"
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
ms.assetid: b409bd0e-28c9-4d9a-80a4-8df77a3aff88
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlAxCreateControlLic
Creates a licensed ActiveX control, initializes it, and hosts it in the specified window.  
  
> [!IMPORTANT]
>  This function cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
      ATLAPI AtlAxCreateControlLic(  
LPCOLESTR lpszName,   
HWND hWnd,   
IStream* pStream,   
IUnknown** ppUnkContainer,   
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
  
 `bstrLic`  
 The BSTR containing the license for the control.  
  
## Return Value  
 One of the standard HRESULT values.  
  
## Example  
 See [Hosting ActiveX Controls Using ATL AXHost](../vs140/Hosting-ActiveX-Controls-Using-ATL-AXHost.md) for a sample of how to use `AtlAxCreateControlLic`.  
  
## Requirements  
 **Header:** atlhost.h  
  
## See Also  
 [Composite Control Global Functions](../vs140/Composite-Control-Global-Functions.md)   
 [Composite Control Fundamentals](../vs140/ATL-Composite-Control-Fundamentals.md)   
 [AtlAxCreateControl](../vs140/AtlAxCreateControl.md)   
 [CAxWindow2T::CreateControlLic](../vs140/CAxWindow2T--CreateControlLic.md)