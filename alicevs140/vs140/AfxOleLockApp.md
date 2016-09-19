---
title: "AfxOleLockApp"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a9284982-ce5a-4508-94c4-b673d3fb45ed
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxOleLockApp
Increments the framework's global count of the number of active objects in the application.  
  
## Syntax  
  
```  
  
void AFXAPI AfxOleLockApp( );  
```  
  
## Remarks  
 The framework keeps a count of the number of objects active in an application. The `AfxOleLockApp` and `AfxOleUnlockApp` functions, respectively, increment and decrement this count.  
  
 When the user attempts to close an application that has active objects — an application for which the count of active objects is nonzero — the framework hides the application from the user's view instead of completely shutting it down. The `AfxOleCanExitApp` function indicates whether the application can terminate.  
  
 Call `AfxOleLockApp` from any object that exposes OLE interfaces, if it would be undesirable for that object to be destroyed while still being used by a client application. Also call `AfxOleUnlockApp` in the destructor of any object that calls `AfxOleLockApp` in the constructor. By default, `COleDocument` (and derived classes) automatically lock and unlock the application.  
  
## Example  
 [!CODE [NVC_MFCAutomation#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCAutomation#5)]  
  
## Requirements  
 **Header:** <afxdisp.h>  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [AfxOleUnlockApp](../vs140/AfxOleUnlockApp.md)   
 [AfxOleCanExitApp](../vs140/AfxOleCanExitApp.md)   
 [COleDocument Class](../vs140/COleDocument-Class.md)