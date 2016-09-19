---
title: "IAxWinAmbientDispatch::get_ShowHatching"
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
ms.assetid: 71ebea5b-7f4d-48bd-b474-574eb17c0319
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAxWinAmbientDispatch::get_ShowHatching
The **ShowHatching** ambient property allows the control to find out if it should draw itself hatched.  
  
## Syntax  
  
```  
  
      STDMETHOD( get_ShowHatching )(  
   VARIANT_BOOL* pbShowHatching   
);  
```  
  
#### Parameters  
 *pbShowHatching*  
 [out] The address of a variable to receive the current value of this property.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 The ATL host object implementation always returns **VARIANT_FALSE** as the value of this property.  
  
## Requirements  
 **Header:** atliface.h  
  
## See Also  
 [IAxWinAmbientDispatch Interface](../vs140/IAxWinAmbientDispatch-Interface.md)