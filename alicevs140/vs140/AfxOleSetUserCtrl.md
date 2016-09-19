---
title: "AfxOleSetUserCtrl"
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
ms.assetid: ca1b4c67-a335-4dc0-b382-96bf7d9452f0
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxOleSetUserCtrl
Sets or clears the user-control flag, which is explained in the reference for `AfxOleGetUserCtrl`.  
  
## Syntax  
  
```  
  
      void AFXAPI AfxOleSetUserCtrl(  
   BOOL bUserCtrl   
);  
```  
  
#### Parameters  
 *bUserCtrl*  
 Specifies whether the user-control flag is to be set or cleared.  
  
## Remarks  
 The framework calls this function when the user creates or loads a document, but not when a document is loaded or created through an indirect action such as loading an embedded object from a container application.  
  
 Call this function if other actions in your application should put the user in control of the application.  
  
## Requirements  
 **Header:** <afxdisp.h>  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [AfxOleGetUserCtrl](../vs140/AfxOleGetUserCtrl.md)