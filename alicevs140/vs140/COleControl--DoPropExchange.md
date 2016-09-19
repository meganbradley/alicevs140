---
title: "COleControl::DoPropExchange"
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
ms.assetid: 8059a3ef-2692-49ae-bb3d-0ae37468f8f1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::DoPropExchange
Called by the framework when loading or storing a control from a persistent storage representation, such as a stream or property set.  
  
## Syntax  
  
```  
  
      virtual void DoPropExchange(  
   CPropExchange* pPX   
);  
```  
  
#### Parameters  
 `pPX`  
 A pointer to a `CPropExchange` object. The framework supplies this object to establish the context of the property exchange, including its direction.  
  
## Remarks  
 This function normally makes calls to the **PX_** family of functions to load or store specific user-defined properties of an OLE control.  
  
 If Control Wizard has been used to create the OLE control project, the overridden version of this function will serialize the stock properties supported by `COleControl` with a call to the base class function, `COleControl::DoPropExchange`. As you add user-defined properties to your OLE control you will need to modify this function to serialize your new properties. For more information on serialization, see the article [ActiveX Controls: Serializing](../vs140/MFC-ActiveX-Controls--Serializing.md).  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [PX_Bool](../vs140/PX_Bool.md)   
 [PX_Short](../vs140/PX_Short.md)