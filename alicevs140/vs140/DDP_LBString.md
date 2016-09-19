---
title: "DDP_LBString"
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
ms.assetid: 4a0dae7c-51dc-4658-89e7-524f19330d8c
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DDP_LBString
Call this function in your property page's `DoDataExchange` function to synchronize the value of a string property with the current selection in a list box on the property page.  
  
## Syntax  
  
```  
  
      void AFXAPI DDP_LBString(  
   CDataExchange* pDX,  
   int id,  
   CString& member,  
   LPCTSTR pszPropName   
);  
```  
  
#### Parameters  
 `pDX`  
 Pointer to a `CDataExchange` object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
 `id`  
 The resource ID of the list box control associated with the control property specified by `pszPropName`.  
  
 `member`  
 The member variable associated with the property page control specified by `id` and the property specified by `pszPropName`.  
  
 `pszPropName`  
 The property name of the control property to be exchanged with the list box string specified by `id`.  
  
## Remarks  
 This function should be called before the corresponding `DDX_LBString` function call.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DDP_LBStringExact](../vs140/DDP_LBStringExact.md)   
 [DDP_LBIndex](../vs140/DDP_LBIndex.md)   
 [COleControl::DoPropExchange](../vs140/COleControl--DoPropExchange.md)   
 [DDX_LBString](../vs140/DDX_LBString.md)