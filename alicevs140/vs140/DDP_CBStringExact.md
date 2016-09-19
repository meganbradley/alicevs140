---
title: "DDP_CBStringExact"
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
ms.assetid: 3fba7e64-ca8f-4a3b-925a-a7bd09baed1e
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DDP_CBStringExact
Call this function in your property page's `DoDataExchange` function to synchronize the value of a string property that exactly matches the current selection in a combo box on the property page.  
  
## Syntax  
  
```  
  
      void AFXAPI DDP_CBStringExact(  
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
 The resource ID of the combo box control associated with the control property specified by `pszPropName`.  
  
 `member`  
 The member variable associated with the property page control specified by `id` and the property specified by `pszPropName`.  
  
 `pszPropName`  
 The property name of the control property to be exchanged with the combo box string specified by `id`.  
  
## Remarks  
 This function should be called before the corresponding `DDX_CBStringExact` function call.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DDP_CBString](../vs140/DDP_CBString.md)   
 [DDP_CBIndex](../vs140/DDP_CBIndex.md)   
 [COleControl::DoPropExchange](../vs140/COleControl--DoPropExchange.md)   
 [DDX_CBStringExact](../vs140/DDX_CBStringExact.md)