---
title: "Initializing Non-MFC DLLs"
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
ms.assetid: 2622b32a-28f9-4d61-9e46-6c19aaf8b7ad
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Initializing Non-MFC DLLs
To initialize non-MFC DLLs, your DLL source code must contain a function called `DllMain`. The following code presents a basic skeleton showing what the definition of `DllMain` might look like:  
  
```  
BOOL APIENTRY DllMain(HANDLE hModule,   
                      DWORD  ul_reason_for_call,   
                      LPVOID lpReserved)  
{  
    switch( ul_reason_for_call ) {  
    case DLL_PROCESS_ATTACH:  
    ...  
    case DLL_THREAD_ATTACH:  
    ...  
    case DLL_THREAD_DETACH:  
    ...  
    case DLL_PROCESS_DETACH:  
    ...  
    }  
    return TRUE;  
}  
```  
  
> [!NOTE]
>  The [!INCLUDE[winsdkshort](../vs140/includes/winsdkshort_md.md)] documentation for **DllEntryPoint** says that the actual name of the entry-point function must be specified on the linker command-line with the /ENTRY option. With Visual C++, you do not need to use the /ENTRY option if the name of your entry-point function is `DllMain`. In fact, if you do use the /ENTRY option and name your entry-point function something other than `DllMain`, the C run-time library will not get initialized properly.  
  
## What do you want to know more about?  
  
-   [The function specification for DllMain (Windows SDK)](http://msdn.microsoft.com/library/windows/desktop/ms682583)  
  
-   [Dynamic-link library entry-point function (Windows SDK)](http://msdn.microsoft.com/library/windows/desktop/ms682596)  
  
-   [The C run-time library behavior and _DllMainCRTStartup](../vs140/Run-Time-Library-Behavior.md)  
  
## See Also  
 [Initializing a DLL](../vs140/Initializing-a-DLL.md)