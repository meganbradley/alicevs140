---
title: "IAxWinHostWindow::QueryControl"
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
ms.assetid: 8bd6e411-52f3-41af-a67e-12d6a31fc5e8
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAxWinHostWindow::QueryControl
Returns the specified interface pointer provided by the hosted control.  
  
## Syntax  
  
```  
  
      STDMETHOD( QueryControl )(  
   REFIID riid,  
   void** ppvObject   
);  
```  
  
#### Parameters  
 `riid`  
 [in] The ID of an interface on the control being requested.  
  
 `ppvObject`  
 [out] The address of a pointer that will receive the specified interface of the created control.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Requirements  
 **Header:** atliface.h  
  
## See Also  
 [IAxWinHostWindow Interface](../vs140/IAxWinHostWindow-Interface.md)   
 [CAxWindow::QueryControl](../vs140/CAxWindow--QueryControl.md)   
 [AtlAxGetControl](../vs140/AtlAxGetControl.md)