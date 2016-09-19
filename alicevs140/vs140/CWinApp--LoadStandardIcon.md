---
title: "CWinApp::LoadStandardIcon"
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
ms.assetid: f9cc187f-5a50-482c-9e04-a4e61ae1cefb
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::LoadStandardIcon
Loads the Windows predefined icon resource that `lpszIconName` specifies.  
  
## Syntax  
  
```  
  
      HICON LoadStandardIcon(  
   LPCTSTR lpszIconName   
) const;  
```  
  
#### Parameters  
 `lpszIconName`  
 A manifest constant identifier that specifies a predefined Windows icon. These identifiers are defined in WINDOWS.H. For a list of the possible predefined values and their descriptions, see the *lpIconName* parameter in [LoadIcon](http://msdn.microsoft.com/library/windows/desktop/ms648072) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 A handle to an icon if successful; otherwise **NULL**.  
  
## Remarks  
 Use the `LoadStandardIcon` or [LoadOEMIcon](../vs140/CWinApp--LoadOEMIcon.md) member function to access the predefined Windows icons.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::LoadOEMIcon](../vs140/CWinApp--LoadOEMIcon.md)   
 [CWinApp::LoadIcon](../vs140/CWinApp--LoadIcon.md)   
 [LoadIcon](http://msdn.microsoft.com/library/windows/desktop/ms648072)