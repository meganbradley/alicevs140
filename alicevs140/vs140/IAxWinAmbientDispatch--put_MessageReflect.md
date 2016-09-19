---
title: "IAxWinAmbientDispatch::put_MessageReflect"
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
ms.assetid: 6a4367ad-a3d8-482f-9e2f-92e014fd8899
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAxWinAmbientDispatch::put_MessageReflect
The **MessageReflect** ambient property specifies whether the container will reflect messages to the hosted control.  
  
## Syntax  
  
```  
  
      STDMETHOD( put_MessageReflect )(  
   VARIANT_BOOL bMessageReflect   
);  
```  
  
#### Parameters  
 `bMessageReflect`  
 [in] The new value of this property.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 The ATL host object implementation uses `VARIANT_TRUE` as the default value of this property.  
  
## Requirements  
 **Header:** atliface.h  
  
## See Also  
 [IAxWinAmbientDispatch Interface](../vs140/IAxWinAmbientDispatch-Interface.md)