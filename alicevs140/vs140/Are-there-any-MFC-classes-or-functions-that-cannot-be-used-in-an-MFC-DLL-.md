---
title: "Are there any MFC classes or functions that cannot be used in an MFC DLL?"
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
ms.assetid: 18e2f1cb-4f72-4d3a-a951-3488208872c7
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Are there any MFC classes or functions that cannot be used in an MFC DLL?
Extension DLLs use the `CWinApp`-derived class of the client application. They must not have their own `CWinApp`-derived class.  
  
 Regular DLLs must have a `CWinApp`-derived class and a single object of that application class, as does an MFC application. Unlike the `CWinApp` object of an application, the `CWinApp` object of the DLL does not have a main message pump.  
  
 Note that because the `CWinApp::Run` mechanism does not apply to a DLL, the application owns the main message pump. If the DLL opens modeless dialog boxes or has a main frame window of its own, the application's main message pump must call a routine exported by the DLL, which in turn calls the `CWinApp::PreTranslateMessage` member function of the DLL's application object.  
  
## See Also  
 [DLL Frequently Asked Questions](../vs140/DLL-Frequently-Asked-Questions.md)