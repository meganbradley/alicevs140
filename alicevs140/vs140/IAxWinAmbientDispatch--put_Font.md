---
title: "IAxWinAmbientDispatch::put_Font"
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
ms.assetid: 044c01c2-4088-4f7e-be14-984965103e8a
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAxWinAmbientDispatch::put_Font
The **Font** property specifies the ambient font of the container.  
  
## Syntax  
  
```  
  
      STDMETHOD( put_Font )(  
   IFontDisp* pFont   
);  
```  
  
#### Parameters  
 `pFont`  
 [in] The new value of this property.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 The ATL host object implementation uses the default GUI font or the system font as the default value of this property.  
  
## Requirements  
 **Header:** atliface.h  
  
## See Also  
 [IAxWinAmbientDispatch Interface](../vs140/IAxWinAmbientDispatch-Interface.md)