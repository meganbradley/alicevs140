---
title: "CComControlBase::ControlQueryInterface"
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
ms.assetid: ba37fcde-2c48-43f3-8cf1-89493db5af2b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::ControlQueryInterface
Retrieves a pointer to the requested interface.  
  
## Syntax  
  
```  
  
      virtual HRESULT ControlQueryInterface(  
   const IID& iid,  
   void** ppv   
);  
```  
  
#### Parameters  
 `iid`  
 The GUID of the interface being requested.  
  
 `ppv`  
 A pointer to the interface pointer identified by `iid`, or **NULL** if the interface is not found.  
  
## Remarks  
 Only handles interfaces in the COM map table.  
  
## Example  
 [!CODE [NVC_ATL_COM#15](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#15)]  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)   
 [CComObjectRootEx::InternalQueryInterface](../vs140/CComObjectRootEx--InternalQueryInterface.md)