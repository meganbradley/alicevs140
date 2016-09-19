---
title: "CONNECTION_PART"
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
ms.topic: article
ms.assetid: c0ee38b4-29af-4833-a0cd-8f25d9d5d588
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CONNECTION_PART
Maps a connection point for your OLE control to a specific interface ID.  
  
## Syntax  
  
```  
  
CONNECTION_PART(  
theClass  
,   
iid  
,   
localClass )  
```  
  
#### Parameters  
 `theClass`  
 Specifies the name of the control class whose connection point this is.  
  
 `iid`  
 The interface ID of the interface called by the connection point.  
  
 *localClass*  
 Specifies the name of the local class that implements the connection point.  
  
## Remarks  
 For example:  
  
 [!CODE [NVC_MFCConnectionPoints#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCConnectionPoints#2)]  
  
 implements a connection map, with a connection point, that calls the `IID_ISinkInterface` interface .  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [BEGIN_CONNECTION_PART](../vs140/BEGIN_CONNECTION_PART.md)   
 [DECLARE_CONNECTION_MAP](../vs140/DECLARE_CONNECTION_MAP.md)   
 [BEGIN_CONNECTION_MAP](../vs140/BEGIN_CONNECTION_MAP.md)   
 [CONNECTION_IID](../vs140/CONNECTION_IID.md)