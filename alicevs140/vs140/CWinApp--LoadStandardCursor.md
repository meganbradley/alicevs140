---
title: "CWinApp::LoadStandardCursor"
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
ms.assetid: ddcd46bb-459d-41b2-a080-b550de736299
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::LoadStandardCursor
Loads the Windows predefined cursor resource that `lpszCursorName` specifies.  
  
## Syntax  
  
```  
  
      HCURSOR LoadStandardCursor(  
   LPCTSTR lpszCursorName   
) const;  
```  
  
#### Parameters  
 `lpszCursorName`  
 An **IDC_** manifest constant identifier that specifies a predefined Windows cursor. These identifiers are defined in WINDOWS.H. The following list shows the possible predefined values and meanings for `lpszCursorName`:  
  
-   **IDC_ARROW** Standard arrow cursor  
  
-   **IDC_IBEAM** Standard text-insertion cursor  
  
-   **IDC_WAIT** Hourglass cursor used when Windows performs a time-consuming task  
  
-   **IDC_CROSS** Cross-hair cursor for selection  
  
-   **IDC_UPARROW** Arrow that points straight up  
  
-   **IDC_SIZE** Obsolete and unsupported; use **IDC_SIZEALL**  
  
-   **IDC_SIZEALL** A four-pointed arrow. The cursor to use to resize a window.  
  
-   **IDC_ICON** Obsolete and unsupported. Use **IDC_ARROW**.  
  
-   **IDC_SIZENWSE** Two-headed arrow with ends at upper left and lower right  
  
-   **IDC_SIZENESW** Two-headed arrow with ends at upper right and lower left  
  
-   **IDC_SIZEWE** Horizontal two-headed arrow  
  
-   **IDC_SIZENS** Vertical two-headed arrow  
  
## Return Value  
 A handle to a cursor if successful; otherwise **NULL**.  
  
## Remarks  
 Use the `LoadStandardCursor` or [LoadOEMCursor](../vs140/CWinApp--LoadOEMCursor.md) member function to access the predefined Windows cursors.  
  
## Example  
 [!CODE [NVC_MFCWindowing#47](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#47)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::LoadOEMCursor](../vs140/CWinApp--LoadOEMCursor.md)   
 [CWinApp::LoadCursor](../vs140/CWinApp--LoadCursor.md)   
 [LoadCursor](http://msdn.microsoft.com/library/windows/desktop/ms648391)