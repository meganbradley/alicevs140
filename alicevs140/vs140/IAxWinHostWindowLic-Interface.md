---
title: "IAxWinHostWindowLic Interface"
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
ms.assetid: 750f1520-6bce-428c-aca0-fccbe3f063c7
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAxWinHostWindowLic Interface
This interface provides methods for manipulating a licensed control and its host object.  
  
## Syntax  
  
```  
  
interface IAxWinHostWindowLic : IAxWinHostWindow  
  
```  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[CreateControlLic](../vs140/IAxWinHostWindowLic--CreateControlLic.md)|Creates a licensed control and attaches it to the host object.|  
|[CreateControlLicEx](../vs140/IAxWinHostWindowLic--CreateControlLicEx.md)|Creates a licensed control, attaches it to the host object, and optionally sets up an event handler.|  
  
## Remarks  
 `IAxWinHostWindowLic` inherits from [IAxWinHostWindow](../vs140/IAxWinHostWindow-Interface.md) and adds methods that support the creation of licensed controls.  
  
 See [Hosting ActiveX Controls Using ATL AXHost](../vs140/Hosting-ActiveX-Controls-Using-ATL-AXHost.md) for a sample that uses the members of this interface.  
  
## Requirements  
 The definition of this interface is available as IDL or C++, as shown below.  
  
|Definition type|File|  
|---------------------|----------|  
|IDL|ATLIFace.idl|  
|C++|ATLIFace.h (also included in ATLBase.h)|