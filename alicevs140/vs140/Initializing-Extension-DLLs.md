---
title: "Initializing Extension DLLs"
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
ms.assetid: 08ad0381-3808-4bea-a93c-c9ba62496543
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Initializing Extension DLLs
Because extension DLLs do not have a `CWinApp`-derived object (as do regular DLLs), you should add your initialization and termination code to the `DllMain` function that the MFC DLL Wizard generates.  
  
 The wizard provides the following code for extension DLLs. In the code, `PROJNAME` is a placeholder for the name of your project.  
  
```  
#include "stdafx.h"  
#include <afxdllx.h>  
  
#ifdef _DEBUG  
#define new DEBUG_NEW  
#undef THIS_FILE  
static char THIS_FILE[] = __FILE__;  
#endif  
static AFX_EXTENSION_MODULE PROJNAMEDLL = { NULL, NULL };  
  
extern "C" int APIENTRY  
DllMain(HINSTANCE hInstance, DWORD dwReason, LPVOID lpReserved)  
{  
   if (dwReason == DLL_PROCESS_ATTACH)  
   {  
      TRACE0("PROJNAME.DLL Initializing!\n");  
  
      // Extension DLL one-time initialization  
      AfxInitExtensionModule(PROJNAMEDLL,   
                                 hInstance);  
  
      // Insert this DLL into the resource chain  
      new CDynLinkLibrary(Dll3DLL);  
   }  
   else if (dwReason == DLL_PROCESS_DETACH)  
   {  
      TRACE0("PROJNAME.DLL Terminating!\n");  
   }  
   return 1;   // ok  
}  
```  
  
 Creating a new **CDynLinkLibrary** object during initialization allows the extension DLL to export `CRuntimeClass` objects or resources to the client application.  
  
 If you are going to use your extension DLL from one or more regular DLLs, you must export an initialization function that creates a **CDynLinkLibrary** object. That function must be called from each of the regular DLLs that use the extension DLL. An appropriate place to call this initialization function is in the `InitInstance` member function of the regular DLL's `CWinApp`-derived object before using any of the extension DLL's exported classes or functions.  
  
 In the `DllMain` that the MFC DLL Wizard generates, the call to `AfxInitExtensionModule` captures the module's run-time classes (`CRuntimeClass` structures) as well as its object factories (`COleObjectFactory` objects) for use when the **CDynLinkLibrary** object is created. You should check the return value of `AfxInitExtensionModule`; if a zero value is returned from `AfxInitExtensionModule`, return zero from your `DllMain` function.  
  
 If your extension DLL will be explicitly linked to an executable (meaning the executable calls `AfxLoadLibrary` to link to the DLL), you should add a call to `AfxTermExtensionModule` on **DLL_PROCESS_DETACH**. This function allows MFC to clean up the extension DLL when each process detaches from the extension DLL (which happens when the process exits or when the DLL is unloaded as a result of a `AfxFreeLibrary` call). If your extension DLL will be linked implicitly to the application, the call to `AfxTermExtensionModule` is not necessary.  
  
 Applications that explicitly link to extension DLLs must call **AfxTermExtensionModule** when freeing the DLL. They should also use `AfxLoadLibrary` and `AfxFreeLibrary` (instead of the Win32 functions **LoadLibrary** and **FreeLibrary**) if the application uses multiple threads. Using `AfxLoadLibrary` and `AfxFreeLibrary` ensures that the startup and shutdown code that executes when the extension DLL is loaded and unloaded does not corrupt the global MFC state.  
  
 Because the MFCx0.dll is fully initialized by the time `DllMain` is called, you can allocate memory and call MFC functions within `DllMain` (unlike the 16-bit version of MFC).  
  
 Extension DLLs can take care of multithreading by handling the **DLL_THREAD_ATTACH** and **DLL_THREAD_DETACH** cases in the `DllMain` function. These cases are passed to `DllMain` when threads attach and detach from the DLL. Calling [TlsAlloc](http://msdn.microsoft.com/library/windows/desktop/ms686801) when a DLL is attaching allows the DLL to maintain thread local storage (TLS) indexes for every thread attached to the DLL.  
  
 Note that the header file Afxdllx.h contains special definitions for structures used in extension DLLs, such as the definition for `AFX_EXTENSION_MODULE` and **CDynLinkLibrary**. You should include this header file in your extension DLL.  
  
> [!NOTE]
>  It is important that you neither define nor undefine any of the _AFX_NO_XXX macros in Stdafx.h. For more information, see the Knowledge Base article "PRB: Problems Occur When Defining _AFX_NO_XXX" (Q140751). You can find Knowledge Base articles in the MSDN Library or at [http://search.support.microsoft.com/](http://search.support.microsoft.com/).  
  
 A sample initialization function that handles multithreading is included in [Using Thread Local Storage in a Dynamic-Link Library](http://msdn.microsoft.com/library/windows/desktop/ms686997) in the [!INCLUDE[winsdkshort](../vs140/includes/winsdkshort_md.md)]. Note that the sample contains an entry-point function called **LibMain**, but you should name this function `DllMain` so that it works with the MFC and C run-time libraries.  
  
 The MFC sample [DLLHUSK](assetId:///dfcaa6ff-b8e2-4efd-8100-ee3650071f90) demonstrates the use of initialization functions.  
  
## What do you want to do?  
  
-   [Initialize regular DLLs](../vs140/Initializing-Regular-DLLs.md)  
  
-   [Initialize non-MFC DLLs](../vs140/Initializing-Non-MFC-DLLs.md)  
  
## What do you want to know more about?  
  
-   [The C run-time library behavior and _DllMainCRTStartup](../vs140/Run-Time-Library-Behavior.md)  
  
-   [Using Database, OLE, and Sockets Extension DLLs in Regular DLLs](../vs140/Using-Database--OLE--and-Sockets-Extension-DLLs-in-Regular-DLLs.md)  
  
-   [The function specification for DllMain (Windows SDK)](http://msdn.microsoft.com/library/windows/desktop/ms682583)  
  
-   [Dynamic-link library entry-point function (Windows SDK)](http://msdn.microsoft.com/library/windows/desktop/ms682596)  
  
## See Also  
 [Initializing a DLL](../vs140/Initializing-a-DLL.md)