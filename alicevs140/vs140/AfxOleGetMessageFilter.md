---
title: "AfxOleGetMessageFilter"
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
ms.assetid: 36cca011-4775-4086-b471-5557a87b266c
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxOleGetMessageFilter
Retrieves the application's current message filter.  
  
## Syntax  
  
```  
  
COleMessageFilter* AFXAPI AfxOleGetMessageFilter( );  
```  
  
## Return Value  
 A pointer to the current message filter.  
  
## Remarks  
 Call this function to access the current `COleMessageFilter`-derived object, just as you would call `AfxGetApp` to access the current application object.  
  
## Example  
 [!CODE [NVC_MFCAutomation#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCAutomation#3)]  
  
 [!CODE [NVC_MFCAutomation#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCAutomation#4)]  
  
## Requirements  
 **Header**: <afxwin.h>  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [COleMessageFilter Class](../vs140/COleMessageFilter-Class.md)   
 [AfxGetApp](../vs140/AfxGetApp.md)