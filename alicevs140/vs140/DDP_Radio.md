---
title: "DDP_Radio"
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
ms.assetid: b967ac34-92e8-44e7-8999-9b383511dc3c
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DDP_Radio
Call this function in your control's `DoPropExchange` function to synchronize the value of the property with the associated property page radio button control.  
  
## Syntax  
  
```  
  
      void AFXAPI DDP_Radio(  
   CDataExchange*pDX,  
   int id,  
   int &member,  
   LPCTSTR pszPropName   
);  
```  
  
#### Parameters  
 `pDX`  
 Pointer to a `CDataExchange` object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
 `id`  
 The resource ID of the radio button control associated with the control property specified by `pszPropName`.  
  
 `member`  
 The member variable associated with the property page control specified by `id` and the property specified by `pszPropName`.  
  
 `pszPropName`  
 The property name of the control property to be exchanged with the radio button control specified by `id`.  
  
## Remarks  
 This function should be called before the corresponding `DDX_Radio` function call.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DDP_Check](../vs140/DDP_Check.md)   
 [DDP_Text](../vs140/DDP_Text.md)   
 [COleControl::DoPropExchange](../vs140/COleControl--DoPropExchange.md)   
 [DDX_Radio](../vs140/DDX_Radio.md)