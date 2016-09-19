---
title: "CWinApp::LoadCursor"
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
ms.assetid: d4131bba-5703-4bcc-8d11-a45a458efbd4
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::LoadCursor
Loads the cursor resource named by `lpszResourceName` or specified by `nIDResource` from the current executable file.  
  
## Syntax  
  
```  
  
      HCURSOR LoadCursor(  
   LPCTSTR lpszResourceName   
) const;  
HCURSOR LoadCursor(  
   UINT nIDResource   
) const;  
```  
  
#### Parameters  
 `lpszResourceName`  
 Points to a null-terminated string that contains the name of the cursor resource. You can use a `CString` for this argument.  
  
 `nIDResource`  
 ID of the cursor resource. For a list of resources, see [LoadCursor](http://msdn.microsoft.com/library/windows/desktop/ms648391) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 A handle to a cursor if successful; otherwise **NULL**.  
  
## Remarks  
 `LoadCursor` loads the cursor into memory only if it has not been previously loaded; otherwise, it retrieves a handle of the existing resource.  
  
 Use the [LoadStandardCursor](../vs140/CWinApp--LoadStandardCursor.md) or [LoadOEMCursor](../vs140/CWinApp--LoadOEMCursor.md) member function to access the predefined Windows cursors.  
  
## Example  
 [!CODE [NVC_MFCWindowing#44](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#44)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::LoadStandardCursor](../vs140/CWinApp--LoadStandardCursor.md)   
 [CWinApp::LoadOEMCursor](../vs140/CWinApp--LoadOEMCursor.md)   
 [LoadCursor](http://msdn.microsoft.com/library/windows/desktop/ms648391)