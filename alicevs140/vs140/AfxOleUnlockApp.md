---
title: "AfxOleUnlockApp"
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
ms.assetid: 17ef1bb2-c355-4c2e-bdd8-a85cefcda4cf
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxOleUnlockApp
Decrements the framework's count of active objects in the application.  
  
## Syntax  
  
```  
  
void AFXAPI AfxOleUnlockApp( );  
```  
  
## Remarks  
 See `AfxOleLockApp` for further information.  
  
 When the number of active objects reaches zero, **AfxOleOnReleaseAllObjects** is called.  
  
## Example  
 See the example for [AfxOleLockApp](../vs140/AfxOleLockApp.md).  
  
## Requirements  
 **Header:** <afxdisp.h>  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [AfxOleLockApp](../vs140/AfxOleLockApp.md)   
 [CCmdTarget::OnFinalRelease](../vs140/CCmdTarget--OnFinalRelease.md)