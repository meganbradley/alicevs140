---
title: "IAxWinAmbientDispatch::put_ForeColor"
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
ms.assetid: b83372a7-8320-4cd7-ae63-71515140b4c0
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAxWinAmbientDispatch::put_ForeColor
The `ForeColor` property specifies the ambient foreground color of the container.  
  
## Syntax  
  
```  
  
      STDMETHOD( put_ForeColor )(  
   OLE_COLOR clrForeground   
);  
```  
  
#### Parameters  
 *clrForeground*  
 [in] The new value of this property.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 The ATL host object implementation uses the system window text color as the default value of this property.  
  
## Requirements  
 **Header:** atliface.h  
  
## See Also  
 [IAxWinAmbientDispatch Interface](../vs140/IAxWinAmbientDispatch-Interface.md)