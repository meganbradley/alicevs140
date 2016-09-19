---
title: "CWinApp::LoadIcon"
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
ms.assetid: 83b01cc2-8ea0-4d65-8095-a6f7fe0bf812
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::LoadIcon
Loads the icon resource named by `lpszResourceName` or specified by `nIDResource` from the executable file.  
  
## Syntax  
  
```  
  
      HICON LoadIcon(  
   LPCTSTR lpszResourceName   
) const;  
HICON LoadIcon(  
   UINT nIDResource   
) const;  
```  
  
#### Parameters  
 `lpszResourceName`  
 Points to a null-terminated string that contains the name of the icon resource. You can also use a `CString` for this argument.  
  
 `nIDResource`  
 ID number of the icon resource.  
  
## Return Value  
 A handle to an icon if successful; otherwise **NULL**.  
  
## Remarks  
 `LoadIcon` loads the icon only if it has not been previously loaded; otherwise, it retrieves a handle of the existing resource.  
  
 You can use the [LoadStandardIcon](../vs140/CWinApp--LoadStandardIcon.md) or [LoadOEMIcon](../vs140/CWinApp--LoadOEMIcon.md) member function to access the predefined Windows icons.  
  
> [!NOTE]
>  This member function calls the Win32 API function [LoadIcon](http://msdn.microsoft.com/library/windows/desktop/ms648072), which can only load an icon whose size conforms to the **SM_CXICON** and **SM_CYICON** system metric values.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::LoadStandardIcon](../vs140/CWinApp--LoadStandardIcon.md)   
 [CWinApp::LoadOEMIcon](../vs140/CWinApp--LoadOEMIcon.md)   
 [LoadIcon](http://msdn.microsoft.com/library/windows/desktop/ms648072)