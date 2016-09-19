---
title: "IAxWinAmbientDispatch::put_DocHostDoubleClickFlags"
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
ms.assetid: f6246053-45c9-47f2-b56c-dadee749fb5f
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAxWinAmbientDispatch::put_DocHostDoubleClickFlags
The **DocHostDoubleClickFlags** property specifies the operation that should take place in response to a double-click.  
  
## Syntax  
  
```  
  
      STDMETHOD( put_DocHostDoubleClickFlags )(  
   DWORD dwDocHostDoubleClickFlags   
);  
```  
  
#### Parameters  
 *dwDocHostDoubleClickFlags*  
 [in] The new value of this property.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 The ATL host object implementation uses **DOCHOSTUIDBLCLK_DEFAULT** as the default value of this property.  
  
## Requirements  
 **Header:** atliface.h  
  
## See Also  
 [IAxWinAmbientDispatch Interface](../vs140/IAxWinAmbientDispatch-Interface.md)   
 [IDocHostUIHandler::GetHostInfo](https://msdn.microsoft.com/en-us/library/aa753257.aspx)