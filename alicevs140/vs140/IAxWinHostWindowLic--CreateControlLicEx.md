---
title: "IAxWinHostWindowLic::CreateControlLicEx"
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
ms.assetid: e26f139e-3121-4c9c-b714-80bcc4ad8331
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAxWinHostWindowLic::CreateControlLicEx
Creates a licensed ActiveX control, initializes it, and hosts it in the specified window, similar to [IAxWinHostWindow::CreateControl](../vs140/IAxWinHostWindow--CreateControl.md).  
  
## Syntax  
  
```  
  
      STDMETHOD( CreateControlLicEx )(  
   LPCOLESTR lpszTricsData,  
   HWND hWnd,  
   IStream* pStream,  
   IUnknown** ppUnk,  
   REFIID riidAdvise,  
   IUnknown* punkAdvise,   
   BSTR bstrLic  
);  
```  
  
#### Parameters  
 `bstrLic`  
 [in] The BSTR that contains the license key for the control.  
  
## Remarks  
 See [IAxWinHostWindow::CreateControlEx](../vs140/IAxWinHostWindow--CreateControlEx.md) for a description of the remaining parameters and return value.  
  
## Example  
 See [Hosting ActiveX Controls Using ATL AXHost](../vs140/Hosting-ActiveX-Controls-Using-ATL-AXHost.md) for a sample that uses `IAxWinHostWindowLic::CreateControlLicEx`.  
  
## Requirements  
 **Header:** atliface.h  
  
## See Also  
 [IAxWinHostWindowLic Interface](../vs140/IAxWinHostWindowLic-Interface.md)