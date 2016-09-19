---
title: "CWinApp::ParseCommandLine"
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
ms.assetid: 7ee5b480-7cb1-4ce5-91a0-a99ae5aa8417
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::ParseCommandLine
Call this member function to parse the command line and send the parameters, one at a time, to [CCommandLineInfo::ParseParam](../vs140/CCommandLineInfo--ParseParam.md).  
  
## Syntax  
  
```  
  
      void ParseCommandLine(  
   CCommandLineInfo& rCmdInfo   
);  
```  
  
#### Parameters  
 `rCmdInfo`  
 A reference to a [CCommandLineInfo](../vs140/CCommandLineInfo-Class.md) object.  
  
## Remarks  
 When you start a new MFC project using the Application Wizard, the Application Wizard will create a local instance of `CCommandLineInfo`, and then call `ProcessShellCommand` and `ParseCommandLine` in the [InitInstance](../vs140/CWinApp--InitInstance.md) member function. A command line follows the route described below:  
  
1.  After being created in `InitInstance`, the `CCommandLineInfo` object is passed to `ParseCommandLine`.  
  
2.  `ParseCommandLine` then calls `CCommandLineInfo::ParseParam` repeatedly, once for each parameter.  
  
3.  `ParseParam` fills the `CCommandLineInfo` object, which is then passed to [ProcessShellCommand](../vs140/CWinApp--ProcessShellCommand.md).  
  
4.  `ProcessShellCommand` handles the command-line arguments and flags.  
  
 Note that you can call `ParseCommandLine` directly as needed.  
  
 For a description of the command-line flags, see [CCommandLineInfo::m_nShellCommand](../vs140/CCommandLineInfo--m_nShellCommand.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CCommandLineInfo Class](../vs140/CCommandLineInfo-Class.md)   
 [CWinApp::InitInstance](../vs140/CWinApp--InitInstance.md)   
 [CCommandLineInfo::ParseParam](../vs140/CCommandLineInfo--ParseParam.md)   
 [CWinApp::ProcessShellCommand](../vs140/CWinApp--ProcessShellCommand.md)   
 [CCommandLineInfo::m_nShellCommand](../vs140/CCommandLineInfo--m_nShellCommand.md)