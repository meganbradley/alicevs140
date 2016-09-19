---
title: "IAxWinAmbientDispatch::get_AllowShowUI"
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
ms.assetid: 311e83f9-2f98-4017-ad56-52dce0685e96
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAxWinAmbientDispatch::get_AllowShowUI
The **AllowShowUI** property specifies whether the hosted control is allowed to display its own user interface.  
  
## Syntax  
  
```  
  
      STDMETHOD( get_AllowShowUI )(  
   VARIANT_BOOL* pbAllowShowUI   
);  
```  
  
#### Parameters  
 *pbAllowShowUI*  
 [out] The address of a variable to receive the current value of this property.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 The ATL host object implementation uses **VARIANT_FALSE** as the default value of this property.  
  
## Requirements  
 **Header:** atliface.h  
  
## See Also  
 [IAxWinAmbientDispatch Interface](../vs140/IAxWinAmbientDispatch-Interface.md)   
 [IDocHostUIHandler::ShowUI](https://msdn.microsoft.com/en-us/library/aa753265.aspx)