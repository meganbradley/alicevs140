---
title: "CComModule::RevokeClassObjects"
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
ms.assetid: a1dd3bc5-0c02-4031-bb95-f0fea2de513e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComModule::RevokeClassObjects
As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
## Syntax  
  
```  
  
HRESULT RevokeClassObjects( ) throw( );  
  
```  
  
## Return Value  
 A standard HRESULT value.  
  
## Remarks  
 Removes the class object. This methodis only available to EXEs.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComModule Class](../vs140/CComModule-Class.md)   
 [CComModule::RegisterClassObjects](../vs140/CComModule--RegisterClassObjects.md)