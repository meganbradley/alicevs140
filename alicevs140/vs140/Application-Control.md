---
title: "Application Control"
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
ms.assetid: c1f69f15-e0fe-4515-9f36-d63d31869deb
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Application Control
OLE requires substantial control over applications and their objects. The OLE system DLLs must be able to launch and release applications automatically, coordinate their production and modification of objects, and so on. The functions in this topic meet those requirements. In addition to being called by the OLE system DLLs, these functions must sometimes be called by applications as well.  
  
### Application Control  
  
|||  
|-|-|  
|[AfxOleCanExitApp](../vs140/AfxOleCanExitApp.md)|Indicates whether the application can terminate.|  
|[AfxOleGetMessageFilter](../vs140/AfxOleGetMessageFilter.md)|Retrieves the application's current message filter.|  
|[AfxOleGetUserCtrl](../vs140/AfxOleGetUserCtrl.md)|Retrieves the current user-control flag.|  
|[AfxOleSetUserCtrl](../vs140/AfxOleSetUserCtrl.md)|Sets or clears the user-control flag.|  
|[AfxOleLockApp](../vs140/AfxOleLockApp.md)|Increments the framework's global count of the number of active objects in an application.|  
|[AfxOleUnlockApp](../vs140/AfxOleUnlockApp.md)|Decrements the framework's count of the number of active objects in an application.|  
|[AfxOleRegisterServerClass](../vs140/AfxOleRegisterServerClass.md)|Registers a server in the OLE system registry.|  
|[AfxOleSetEditMenu](../vs140/AfxOleSetEditMenu.md)|Implements the user interface for the *typename* Object command.|  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)