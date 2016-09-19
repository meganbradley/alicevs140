---
title: "IAxWinAmbientDispatch::get_MessageReflect"
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
ms.assetid: 04ed4b4c-24ac-4111-b76e-a11e1ee4504a
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAxWinAmbientDispatch::get_MessageReflect
The **MessageReflect** ambient property specifies whether the container will reflect messages to the hosted control.  
  
## Syntax  
  
```  
  
      STDMETHOD( get_MessageReflect )(  
   VARIANT_BOOL* pbMessageReflect   
);  
```  
  
#### Parameters  
 *pbMessageReflect*  
 [out] The address of a variable to receive the current value of this property.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 The ATL host object implementation uses `VARIANT_TRUE` as the default value of this property.  
  
## Requirements  
 **Header:** atliface.h  
  
## See Also  
 [IAxWinAmbientDispatch Interface](../vs140/IAxWinAmbientDispatch-Interface.md)