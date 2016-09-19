---
title: "IAxWinHostWindow::AttachControl"
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
ms.assetid: e657ab5a-b598-437d-888f-3c30def1f60f
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAxWinHostWindow::AttachControl
Attaches an existing (and previously initialized) control to the host object using the window identified by `hWnd`.  
  
## Syntax  
  
```  
  
      STDMETHOD( AttachControl )(  
   IUnknown* pUnkControl,  
   HWND hWnd   
);  
```  
  
#### Parameters  
 *pUnkControl*  
 [in] A pointer to the **IUnknown** interface of the control to be attached to the host object.  
  
 `hWnd`  
 [in] A handle to the window to be used for hosting.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Requirements  
 **Header:** atliface.h  
  
## See Also  
 [IAxWinHostWindow Interface](../vs140/IAxWinHostWindow-Interface.md)   
 [IAxWinHostWindow::CreateControl](../vs140/IAxWinHostWindow--CreateControl.md)   
 [IAxWinHostWindow::CreateControlEx](../vs140/IAxWinHostWindow--CreateControlEx.md)   
 [CAxWindow::AttachControl](../vs140/CAxWindow--AttachControl.md)   
 [AtlAxAttachControl](../vs140/AtlAxAttachControl.md)