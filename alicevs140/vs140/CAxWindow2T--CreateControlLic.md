---
title: "CAxWindow2T::CreateControlLic"
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
ms.assetid: 82894b6d-9504-45f2-818c-850af4b707f3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAxWindow2T::CreateControlLic
Creates a licensed ActiveX control, initializes it, and hosts it in the specified window.  
  
## Syntax  
  
```  
  
      HRESULT CreateControlLic(  
   DWORD dwResID,   
   IStream* pStream = NULL,   
   IUnknown** ppUnkContainer = NULL,   
   BSTR bstrLicKey = NULL  
);  
HRESULT CreateControlLic(  
   LPCOLESTR lpszName,   
   IStream* pStream = NULL,   
   IUnknown** ppUnkContainer = NULL,   
   BSTR bstrLicKey = NULL  
);  
```  
  
#### Parameters  
 `bstrLicKey`  
 The license key for the control; NULL if creating a nonlicensed control.  
  
## Remarks  
 See [CAxWindow::CreateControl](../vs140/CAxWindow--CreateControl.md) for a description of the remaining parameters and return value.  
  
## Example  
 See [Hosting ActiveX Controls Using ATL AXHost](../vs140/Hosting-ActiveX-Controls-Using-ATL-AXHost.md) for a sample that uses `CAxWindow2T::CreateControlLic`.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CAxWindow2T Class](../vs140/CAxWindow2T-Class.md)