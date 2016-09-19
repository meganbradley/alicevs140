---
title: "AfxWinInit"
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
ms.assetid: 7ae6d68d-c200-433c-88f7-ece5b7cfbe7d
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxWinInit
This function is called by the MFC-supplied `WinMain` function, as part of the [CWinApp](../vs140/CWinApp-Class.md) initialization of a GUI-based application, to initialize MFC.  
  
## Syntax  
  
```  
  
      BOOL AFXAPI AfxWinInit(  
   HINSTANCE hInstance,  
   HINSTANCE hPrevInstance,  
   LPTSTR lpCmdLine,  
   int nCmdShow   
);  
```  
  
#### Parameters  
 `hInstance`  
 The handle of the currently running module.  
  
 *hPrevInstance*  
 A handle to a previous instance of the application. For a Win32-based application, this parameter is always **NULL**.  
  
 `lpCmdLine`  
 Points to a null-terminated string specifying the command line for the application.  
  
 `nCmdShow`  
 Specifies how the main window of a GUI application would be shown.  
  
## Remarks  
 For a console application, which does not use the MFC-supplied `WinMain` function, you must call `AfxWinInit` directly to initialize MFC.  
  
 If you call `AfxWinInit` yourself, you should declare an instance of a `CWinApp` class. For a console application, you might choose not to derive your own class from `CWinApp` and instead use an instance of `CWinApp` directly. This technique is appropriate if you decide to leave all functionality for your application in your implementation of **main**.  
  
> [!NOTE]
>  When it creates an activation context for an assembly, MFC uses a manifest resource provided by the user module. The activation context is created in `AfxWinInit`. For more information, see [Support for Activation Contexts in the MFC Module State](../vs140/Support-for-Activation-Contexts-in-the-MFC-Module-State.md).  
  
## Example  
 [!CODE [NVC_MFC_AfxWinInit#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_AfxWinInit#1)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [CWinApp: The Application Class](../vs140/CWinApp--The-Application-Class.md)   
 [main: Program Startup](../vs140/main--Program-Startup.md)   
 [WinMain](http://msdn.microsoft.com/library/windows/desktop/ms633559)