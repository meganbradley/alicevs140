---
title: "AfxRegisterClass"
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
ms.assetid: 24254107-df3c-4d1a-a13b-25663b3e56ab
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxRegisterClass
Use this function to register window classes in a DLL that uses MFC.  
  
## Syntax  
  
```  
  
      BOOL AFXAPI AfxRegisterClass(  
   WNDCLASS* lpWndClass   
);  
```  
  
#### Parameters  
 *lpWndClass*  
 Pointer to a [WNDCLASS](http://msdn.microsoft.com/library/windows/desktop/ms633576) structure containing information about the window class to be registered. For more information on this structure, see the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 **TRUE** if the class is successfully registered; otherwise **FALSE**.  
  
## Remarks  
 If you use this function, the class is automatically unregistered when the DLL is unloaded.  
  
 In non-DLL builds, the `AfxRegisterClass` identifier is defined as a macro that maps to the Windows function **RegisterClass**, since classes registered in an application are automatically unregistered. If you use `AfxRegisterClass` instead of **RegisterClass**, your code can be used without change both in an application and in a DLL.  
  
## Example  
 [!CODE [NVC_MFC_DLL#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_DLL#3)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)