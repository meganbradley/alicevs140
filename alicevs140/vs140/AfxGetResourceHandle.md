---
title: "AfxGetResourceHandle"
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
ms.assetid: d0eff6c4-f566-471a-96b7-a5a70a751a92
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxGetResourceHandle
Use the `HINSTANCE` handle returned by this function to access the application's resources directly, for example, in calls to the Windows function **FindResource**.  
  
## Syntax  
  
```  
  
extern HINSTANCE AfxGetResourceHandle( );  
```  
  
## Return Value  
 An `HINSTANCE` handle where the default resources of the application are loaded.  
  
## Example  
 [!CODE [NVC_MFCWindowing#130](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#130)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [AfxGetInstanceHandle](../vs140/AfxGetInstanceHandle.md)   
 [AfxSetResourceHandle](../vs140/AfxSetResourceHandle.md)   
 [AfxFindResourceHandle](../vs140/AfxFindResourceHandle.md)