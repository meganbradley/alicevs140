---
title: "CComClassFactory2::GetLicInfo"
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
ms.assetid: 457d8d06-4fee-4521-bdf1-6571a08e10b2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComClassFactory2::GetLicInfo
Fills a [LICINFO](http://msdn.microsoft.com/library/windows/desktop/ms690590) structure with information that describes the class factory's licensing capabilities.  
  
## Syntax  
  
```  
  
      STDMETHOD(GetLicInfo)(  
   LICINFO* pLicInfo   
);  
```  
  
#### Parameters  
 *pLicInfo*  
 [out] Pointer to a **LICINFO** structure.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 The `fRuntimeKeyAvail` member of this structure indicates whether, given a license key, the class factory allows objects to be created on an unlicensed machine. The *fLicVerified* member indicates whether a full machine license exists.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComClassFactory2 Class](../vs140/CComClassFactory2-Class.md)   
 [CComClassFactory2::RequestLicKey](../vs140/CComClassFactory2--RequestLicKey.md)   
 [CComClassFactory2::CreateInstanceLic](../vs140/CComClassFactory2--CreateInstanceLic.md)