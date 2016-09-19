---
title: "AfxSetResourceHandle"
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
ms.assetid: 4fa9b820-c64c-4db3-8dc0-de6dfeb8e65b
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxSetResourceHandle
Use this function to set the `HINSTANCE` handle that determines where the default resources of the application are loaded.  
  
## Syntax  
  
```  
  
      void AFXAPI AfxSetResourceHandle(  
   HINSTANCE hInstResource   
);   
```  
  
#### Parameters  
 `hInstResource`  
 The instance or module handle to an .EXE or DLL file from which the application's resources are loaded.  
  
## Example  
 [!CODE [NVC_MFCWindowing#135](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#135)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [AfxGetInstanceHandle](../vs140/AfxGetInstanceHandle.md)   
 [AfxGetResourceHandle](../vs140/AfxGetResourceHandle.md)