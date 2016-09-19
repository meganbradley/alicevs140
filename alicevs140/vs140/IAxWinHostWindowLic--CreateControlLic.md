---
title: "IAxWinHostWindowLic::CreateControlLic"
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
ms.assetid: 8b19695b-f7e1-4bea-9679-f2f93311b386
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAxWinHostWindowLic::CreateControlLic
Creates a licensed control, initializes it, and hosts it in the window identified by `hWnd`.  
  
## Syntax  
  
```  
  
      STDMETHOD( CreateControlLic )(  
   LPCOLESTR lpTricsData,  
   HWND hWnd,  
   IStream* pStream,  
   BSTR bstrLic  
);  
```  
  
#### Parameters  
 `bstrLic`  
 [in] The BSTR that contains the license key for the control.  
  
## Remarks  
 See [IAxWinHostWindow::CreateControl](../vs140/IAxWinHostWindow--CreateControl.md) for a description of the remaining parameters and return value.  
  
 Calling this method is equivalent to calling [IAxWinHostWindowLic::CreateControlLicEx](../vs140/IAxWinHostWindowLic--CreateControlLicEx.md)  
  
## Example  
 See [Hosting ActiveX Controls Using ATL AXHost](../vs140/Hosting-ActiveX-Controls-Using-ATL-AXHost.md) for a sample that uses `IAxWinHostWindowLic::CreateControlLic`.  
  
## Requirements  
 **Header:** atliface.h  
  
## See Also  
 [IAxWinHostWindowLic Interface](../vs140/IAxWinHostWindowLic-Interface.md)