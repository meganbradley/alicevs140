---
title: "AfxGetAmbientActCtx"
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
ms.topic: article
ms.assetid: c29a30ee-b8a0-473c-a15d-fdef92e98bb0
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxGetAmbientActCtx
Use this function to get the current state of the per-module state flag, which affects the WinSxS behavior of MFC.  
  
## Syntax  
  
```  
BOOL AFXAPI AfxGetAmbientActCtx();   
```  
  
## Return Value  
 Module state flag current value.  
  
## Remarks  
 When the flag is set (which is the default) and a thread enters an MFC module (see [AFX_MANAGE_STATE](../vs140/AFX_MANAGE_STATE.md)), the context of the module is activated.  
  
 If the flag is not set, the context of the module is not activated on entry.  
  
 The context of a module is determined from its manifest, usually embedded in module resources.  
  
## Requirements  
 **Header:** afxcomctl32.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [AFX_MANAGE_STATE](../vs140/AFX_MANAGE_STATE.md)   
 [Managing the State Data of MFC Modules](../vs140/Managing-the-State-Data-of-MFC-Modules.md)   
 [AfxSetAmbientActCtx](../vs140/AfxSetAmbientActCtx.md)