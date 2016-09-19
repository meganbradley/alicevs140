---
title: "CWinApp::InitInstance"
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
ms.topic: reference
ms.assetid: 0dcf01bb-276d-4615-ba6b-ef9bafaa80ba
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::InitInstance
Windows allows several copies of the same program to run at the same time.  
  
## Syntax  
  
```  
  
virtual BOOL InitInstance( );  
```  
  
## Return Value  
 Nonzero if initialization is successful; otherwise 0.  
  
## Remarks  
 Application initialization is conceptually divided into two sections: one-time application initialization that is done the first time the program runs, and instance initialization that runs each time a copy of the program runs, including the first time. The framework's implementation of `WinMain` calls this function.  
  
 Override `InitInstance` to initialize each new instance of your application running under Windows. Typically, you override `InitInstance` to construct your main window object and set the `CWinThread::m_pMainWnd` data member to point to that window. For more information on overriding this member function, see [CWinApp: The Application Class](../vs140/CWinApp--The-Application-Class.md).  
  
> [!NOTE]
>  MFC applications must be initialized as single threaded apartment (STA). If you call [CoInitializeEx](http://msdn.microsoft.com/library/windows/desktop/ms695279) in your `InitInstance` override, specify `COINIT_APARTMENTTHREADED` (rather than `COINIT_MULTITHREADED`). For more information, see PRB: MFC Application Stops Responding When You Initialize the Application as a Multithreaded Apartment (828643) at [http://support.microsoft.com/default.aspx?scid=kb;en-us;828643](http://support.microsoft.com/default.aspx?scid=kb;en-us;828643).  
  
## Example  
 [!CODE [NVC_MFCListView#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCListView#9)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)