---
title: "DDP_Check"
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
ms.assetid: fe8b35e5-fce7-42ab-b56b-405ae3bb9ab1
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DDP_Check
Call this function in your property page's `DoDataExchange` function to synchronize the value of the property with the associated property page check box control.  
  
## Syntax  
  
```  
  
      void AFXAPI DDP_Check(  
   CDataExchange*pDX,  
   int id,  
   int &member,  
   LPCSTR pszPropName   
);  
```  
  
#### Parameters  
 `pDX`  
 Pointer to a `CDataExchange` object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
 `id`  
 The resource ID of the check box control associated with the control property specified by `pszPropName`.  
  
 `member`  
 The member variable associated with the property page control specified by `id` and the property specified by `pszPropName`.  
  
 `pszPropName`  
 The property name of the control property to be exchanged with the check box control specified by `id`.  
  
## Remarks  
 This function should be called before the corresponding `DDX_Check` function call.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DDP_Radio](../vs140/DDP_Radio.md)   
 [DDP_Text](../vs140/DDP_Text.md)   
 [COleControl::DoPropExchange](../vs140/COleControl--DoPropExchange.md)   
 [DDX_Check](../vs140/DDX_Check.md)