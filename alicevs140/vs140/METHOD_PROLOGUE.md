---
title: "METHOD_PROLOGUE"
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
ms.assetid: e94c4939-64ea-42de-a501-55594c952828
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# METHOD_PROLOGUE
Maintains the proper global state when calling methods of an exported interface.  
  
## Syntax  
  
```  
  
METHOD_PROLOGUE(  
theClass  
,   
localClass )  
```  
  
#### Parameters  
 `theClass`  
 Specifies the name of the class whose interface map is being implemented.  
  
 *localClass*  
 Specifies the name of the local class that implements the interface map.  
  
## Remarks  
 Typically, member functions of interfaces implemented by `CCmdTarget`-derived objects already use this macro to provide automatic initialization of the `pThis` pointer. For example:  
  
 [!CODE [NVC_MFCConnectionPoints#11](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCConnectionPoints#11)]  
  
 [!CODE [NVC_MFCConnectionPoints#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCConnectionPoints#5)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [TN038: MFC/OLE IUnknown Implementation](../vs140/TN038--MFC-OLE-IUnknown-Implementation.md)   
 [Creating New Documents, Windows, and Views](../vs140/Creating-New-Documents--Windows--and-Views.md)