---
title: "AfxSetAmbientActCtx"
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
ms.assetid: 667211be-2cdb-4b6e-a8e2-d51416a097a7
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxSetAmbientActCtx
Use this function to set the per-module state flag, which affects the WinSxS behavior of MFC.  
  
## Syntax  
  
```  
  
      void AFXAPI AfxSetAmbientActCtx(  
BOOL bSet  
);  
```  
  
#### Parameters  
 `bSet`  
 New value of the module state flag.  
  
## Remarks  
 When the flag is set (which is the default) and a thread enters an MFC module (see [AFX_MANAGE_STATE](../vs140/AFX_MANAGE_STATE.md)), the context of the module is activated.  
  
 If the flag is not set, the context of the module is not activated on entry.  
  
 The context of a module is determined from its manifest, usually embedded in module resources.  
  
## Example  
 [!CODE [NVC_MFCListView#13](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCListView#13)]  
  
## Requirements  
 **Header:** afxcomctl32.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [AfxGetAmbientActCtx](../vs140/AfxGetAmbientActCtx.md)   
 [AFX_MANAGE_STATE](../vs140/AFX_MANAGE_STATE.md)   
 [Managing the State Data of MFC Modules](../vs140/Managing-the-State-Data-of-MFC-Modules.md)