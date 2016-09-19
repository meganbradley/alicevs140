---
title: "IAxWinAmbientDispatch::get_UserMode"
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
ms.assetid: 3cea728b-8882-4d3d-b66f-b985d9739050
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAxWinAmbientDispatch::get_UserMode
The **UserMode** property specifies the ambient user mode of the container.  
  
## Syntax  
  
```  
  
      STDMETHOD( get_UserMode )(  
   VARIANT_BOOL* pbUserMode   
);  
```  
  
#### Parameters  
 *pbUserMode*  
 [out] The address of a variable to receive the current value of this property.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 The ATL host object implementation uses `VARIANT_TRUE` as the default value of this property.  
  
## Requirements  
 **Header:** atliface.h  
  
## See Also  
 [IAxWinAmbientDispatch Interface](../vs140/IAxWinAmbientDispatch-Interface.md)