---
title: "CONNECTION_IID"
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
ms.assetid: 4ad29be2-cdf2-4d98-907b-92e57f583c2a
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CONNECTION_IID
Use between the `BEGIN_CONNECTION_PART` and `END_CONNECTION_PART` macros to define an interface ID for a connection point supported by your OLE control.  
  
## Syntax  
  
```  
  
CONNECTION_IID(  
iid )  
```  
  
#### Parameters  
 `iid`  
 The interface ID of the interface called by the connection point.  
  
## Remarks  
 The `iid` argument is an interface ID used to identify the interface that the connection point will call on its connected sinks. For example:  
  
 [!CODE [NVC_MFCConnectionPoints#10](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCConnectionPoints#10)]  
  
 specifies a connection point that calls the `ISinkInterface` interface.  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [BEGIN_CONNECTION_PART](../vs140/BEGIN_CONNECTION_PART.md)   
 [DECLARE_CONNECTION_MAP](../vs140/DECLARE_CONNECTION_MAP.md)   
 [END_CONNECTION_PART](../vs140/END_CONNECTION_PART.md)