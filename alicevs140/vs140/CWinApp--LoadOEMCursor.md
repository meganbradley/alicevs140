---
title: "CWinApp::LoadOEMCursor"
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
ms.assetid: ea360729-97aa-456e-a4d1-92397a370952
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::LoadOEMCursor
Loads the Windows predefined cursor resource specified by `nIDCursor`.  
  
## Syntax  
  
```  
  
      HCURSOR LoadOEMCursor(  
   UINT nIDCursor   
) const;  
```  
  
#### Parameters  
 `nIDCursor`  
 An **OCR_** manifest constant identifier that specifies a predefined Windows cursor. You must have **#define OEMRESOURCE** before **#include <afxwin.h>** to gain access to the **OCR_** constants in WINDOWS.H.  
  
## Return Value  
 A handle to a cursor if successful; otherwise **NULL**.  
  
## Remarks  
 Use the `LoadOEMCursor` or [LoadStandardCursor](../vs140/CWinApp--LoadStandardCursor.md) member function to access the predefined Windows cursors.  
  
## Example  
 [!CODE [NVC_MFCWindowing#45](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#45)]  
  
 [!CODE [NVC_MFCWindowing#46](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#46)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::LoadCursor](../vs140/CWinApp--LoadCursor.md)   
 [CWinApp::LoadStandardCursor](../vs140/CWinApp--LoadStandardCursor.md)   
 [LoadCursor](http://msdn.microsoft.com/library/windows/desktop/ms648391)