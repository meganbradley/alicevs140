---
title: "CCommandLineInfo::ParseParam"
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
ms.assetid: 2dae5356-d15e-4000-bcdc-ce4ee1bcba75
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCommandLineInfo::ParseParam
The framework calls this function to parse/interpret individual parameters from the command line. The second version differs from the first only in Unicode projects.  
  
## Syntax  
  
```  
  
      virtual void ParseParam(   
   const char* pszParam,   
   BOOL bFlag,   
   BOOL bLast   
);  
virtual void ParseParam(   
   const TCHAR* pszParam,    
   BOOL bFlag,   
   BOOL bLast  
);  
```  
  
#### Parameters  
 `pszParam`  
 The parameter or flag.  
  
 *bFlag*  
 Indicates whether `pszParam` is a parameter or a flag.  
  
 `bLast`  
 Indicates if this is the last parameter or flag on the command line.  
  
## Remarks  
 [CWinApp::ParseCommandLine](../vs140/CWinApp--ParseCommandLine.md) calls `ParseParam` once for each parameter or flag on the command line, passing the argument to `pszParam`. If the first character of the parameter is a '**-**' or a '**/**', then it is removed and *bFlag* is set to **TRUE**. When parsing the final parameter, `bLast` is set to **TRUE**.  
  
 The default implementation of this function recognizes the following flags: **/p**, **/pt**, **/dde**, **/Automation**, and **/Embedding**, as shown in the following table:  
  
|Command-line argument|Command executed|  
|----------------------------|----------------------|  
|*app*|New file.|  
|*app* filename|Open file.|  
|*app* **/p** filename|Print file to default printer.|  
|*app* **/pt** filename printer driver port|Print file to the specified printer.|  
|*app* **/dde**|Start up and await DDE command.|  
|*app* **/Automation**|Start up as an OLE automation server.|  
|*app* **/Embedding**|Start up to edit an embedded OLE item.|  
|*app* **/Register**<br /><br /> *app* **/Regserver**|Informs the application to perform any registration tasks.|  
|*app* **/Unregister**<br /><br /> *app* **/Unregserver**|Informs the application to perform any un-registration tasks.|  
  
 This information is stored in [m_bRunAutomated](../vs140/CCommandLineInfo--m_bRunAutomated.md), [m_bRunEmbedded](../vs140/CCommandLineInfo--m_bRunEmbedded.md), and [m_nShellCommand](../vs140/CCommandLineInfo--m_nShellCommand.md). Flags are marked by either a forward-slash '**/**' or hyphen '**-**'.  
  
 The default implementation puts the first non-flag parameter into [m_strFileName](../vs140/CCommandLineInfo--m_strFileName.md). In the case of the **/pt** flag, the default implementation puts the second, third, and fourth non-flag parameters into [m_strPrinterName](../vs140/CCommandLineInfo--m_strPrinterName.md), [m_strDriverName](../vs140/CCommandLineInfo--m_strDriverName.md), and [m_strPortName](../vs140/CCommandLineInfo--m_strPortName.md), respectively.  
  
 The default implementation also sets [m_bShowSplash](../vs140/CCommandLineInfo--m_bShowSplash.md) to **TRUE** only in the case of a new file. In the case of a new file, the user has taken action involving the application itself. In any other case, including opening existing files using the shell, the user action involves the file directly. In a document-centric standpoint, the splash screen does not need to announce the application starting up.  
  
 Override this function in your derived class to handle other flag and parameter values.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCommandLineInfo Class](../vs140/CCommandLineInfo-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::ParseCommandLine](../vs140/CWinApp--ParseCommandLine.md)