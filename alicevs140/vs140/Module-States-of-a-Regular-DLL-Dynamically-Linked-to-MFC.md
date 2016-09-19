---
title: "Module States of a Regular DLL Dynamically Linked to MFC"
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
ms.assetid: b4493e79-d25e-4b7f-a565-60de5b32c723
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Module States of a Regular DLL Dynamically Linked to MFC
The ability to dynamically link a regular DLL to the MFC DLL allows some configurations that are very complicated. For example, a regular DLL and the executable that uses it can both dynamically link to the MFC DLL and to any extension DLLs.  
  
 This configuration poses a problem with regard to the MFC global data, such as the pointer to the current `CWinApp` object and handle maps.  
  
 Before MFC version 4.0, this global data resided in the MFC DLL itself and was shared by all the modules in the process. Because each process using a Win32 DLL gets its own copy of the DLL's data, this scheme provided an easy way to track per-process data. Also, because the AFXDLL model presumed that there would be only one `CWinApp` object and only one set of handle maps in the process, these items could be tracked in the MFC DLL itself.  
  
 But with the ability to dynamically link a regular DLL to the MFC DLL, it is now possible to have two or more `CWinApp` objects in a process — and also two or more sets of handle maps. How does MFC keep track of which ones it should be using?  
  
 The solution is to give each module (application or regular DLL) its own copy of this global state information. Thus, a call to **AfxGetApp** in the regular DLL returns a pointer to the `CWinApp` object in the DLL, not the one in the executable. This per-module copy of the MFC global data is known as a module state and is described in [MFC Tech Note 58](../vs140/TN058--MFC-Module-State-Implementation.md).  
  
 The MFC common window procedure automatically switches to the correct module state, so you do not need to worry about it in any message handlers implemented in your regular DLL. But when your executable calls into the regular DLL, you do need to explicitly set the current module state to the one for the DLL. To do this, use the **AFX_MANAGE_STATE** macro in every function exported from the DLL. This is done by adding the following line of code to the beginning of functions exported from the DLL:  
  
```  
AFX_MANAGE_STATE(AfxGetStaticModuleState( ))  
```  
  
## What do you want to know more about?  
  
-   [Managing the state data of MFC modules](../vs140/Managing-the-State-Data-of-MFC-Modules.md)  
  
-   [Regular DLLs dynamically linked to MFC](../vs140/Regular-DLLs-Dynamically-Linked-to-MFC.md)  
  
-   [Extension DLLs](../vs140/Extension-DLLs--Overview.md)  
  
## See Also  
 [DLLs in Visual C++](../vs140/DLLs-in-Visual-C--.md)