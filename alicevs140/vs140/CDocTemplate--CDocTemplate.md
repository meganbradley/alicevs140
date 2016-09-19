---
title: "CDocTemplate::CDocTemplate"
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
ms.assetid: 5694de82-c90f-4ca2-83f1-d892c2a6e8dd
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocTemplate::CDocTemplate
Constructs a `CDocTemplate` object.  
  
## Syntax  
  
```  
  
      CDocTemplate (  
   UINT nIDResource,  
   CRuntimeClass* pDocClass,  
   CRuntimeClass* pFrameClass,  
   CRuntimeClass* pViewClass   
);  
```  
  
#### Parameters  
 `nIDResource`  
 Specifies the ID of the resources used with the document type. This may include menu, icon, accelerator table, and string resources.  
  
 The string resource consists of up to seven substrings separated by the '\n' character (the '\n' character is needed as a place holder if a substring is not included; however, trailing '\n' characters are not necessary); these substrings describe the document type. For information on the substrings, see [GetDocString](../vs140/CDocTemplate--GetDocString.md). This string resource is found in the application's resource file. For example:  
  
 `// MYCALC.RC`  
  
 `STRINGTABLE PRELOAD DISCARDABLE`  
  
 `BEGIN`  
  
 `IDR_SHEETTYPE "\nSheet\nWorksheet\nWorksheets (*.myc)\n.myc\n MyCalcSheet\nMyCalc Worksheet"`  
  
 `END`  
  
 Note that the string begins with a '\n' character; this is because the first substring is not used for MDI applications and so is not included. You can edit this string using the string editor; the entire string appears as a single entry in the String Editor, not as seven separate entries.  
  
 `pDocClass`  
 Points to the `CRuntimeClass` object of the document class. This class is a **CDocument**-derived class you define to represent your documents.  
  
 `pFrameClass`  
 Points to the `CRuntimeClass` object of the frame window class. This class can be a `CFrameWnd`-derived class, or it can be `CFrameWnd` itself if you want default behavior for your main frame window.  
  
 `pViewClass`  
 Points to the `CRuntimeClass` object of the view class. This class is a `CView`-derived class you define to display your documents.  
  
## Remarks  
 Use this member function to construct a `CDocTemplate` object. Dynamically allocate a `CDocTemplate` object and pass it to [CWinApp::AddDocTemplate](../vs140/CWinApp--AddDocTemplate.md) from the `InitInstance` member function of your application class.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocTemplate Class](../vs140/CDocTemplate-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocTemplate::GetDocString](../vs140/CDocTemplate--GetDocString.md)   
 [CMultiDocTemplate::CMultiDocTemplate](../vs140/CMultiDocTemplate--CMultiDocTemplate.md)   
 [CSingleDocTemplate::CSingleDocTemplate](../vs140/CSingleDocTemplate--CSingleDocTemplate.md)   
 [CWinApp::AddDocTemplate](../vs140/CWinApp--AddDocTemplate.md)   
 [CWinApp::InitInstance](../vs140/CWinApp--InitInstance.md)   
 [CRuntimeClass Structure](../vs140/CRuntimeClass-Structure.md)