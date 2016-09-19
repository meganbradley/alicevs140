---
title: "IAxWinAmbientDispatch::put_AllowWindowlessActivation"
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
ms.assetid: 849a7d11-8476-44df-a568-fb4ee106ee19
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAxWinAmbientDispatch::put_AllowWindowlessActivation
The **AllowWindowlessActivation** property specifies whether the container will allow windowless activation.  
  
## Syntax  
  
```  
  
      STDMETHOD( put_AllowWindowlessActivation )(  
   VARIANT_BOOL bAllowWindowless   
);  
```  
  
#### Parameters  
 *bAllowWindowless*  
 [in] The new value of this property.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 The ATL host object implementation uses `VARIANT_TRUE` as the default value of this property.  
  
## Requirements  
 **Header:** atliface.h  
  
## See Also  
 [IAxWinAmbientDispatch Interface](../vs140/IAxWinAmbientDispatch-Interface.md)