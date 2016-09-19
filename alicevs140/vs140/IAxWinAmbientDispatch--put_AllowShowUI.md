---
title: "IAxWinAmbientDispatch::put_AllowShowUI"
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
ms.assetid: 315ea288-891c-4c3f-b03e-b39a3f9f51a6
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAxWinAmbientDispatch::put_AllowShowUI
The **AllowShowUI** property specifies whether the hosted control is allowed to display its own user interface.  
  
## Syntax  
  
```  
  
      STDMETHOD( put_AllowShowUI )(  
   VARIANT_BOOL bAllowShowUI   
);  
```  
  
#### Parameters  
 *bAllowShowUI*  
 [in] The new value of this property.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 The ATL host object implementation uses **VARIANT_FALSE** as the default value of this property.  
  
## Requirements  
 **Header:** atliface.h  
  
## See Also  
 [IAxWinAmbientDispatch Interface](../vs140/IAxWinAmbientDispatch-Interface.md)