---
title: "CMenu::LoadMenu"
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
ms.assetid: 7217f8f5-01a0-4004-a2ee-12b0d5713b05
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMenu::LoadMenu
Loads a menu resource from the application's executable file and attaches it to the `CMenu` object.  
  
## Syntax  
  
```  
  
      BOOL LoadMenu(  
   LPCTSTR lpszResourceName   
);  
BOOL LoadMenu(  
   UINT nIDResource   
);  
```  
  
#### Parameters  
 `lpszResourceName`  
 Points to a null-terminated string that contains the name of the menu resource to load.  
  
 `nIDResource`  
 Specifies the menu ID of the menu resource to load.  
  
## Return Value  
 Nonzero if the menu resource was loaded successfully; otherwise 0.  
  
## Remarks  
 Before exiting, an application must free system resources associated with a menu if the menu is not assigned to a window. An application frees a menu by calling the [DestroyMenu](../vs140/CMenu--DestroyMenu.md) member function.  
  
## Example  
 [!CODE [NVC_MFCWindowing#29](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#29)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMenu Class](../vs140/CMenu-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMenu::AppendMenu](../vs140/CMenu--AppendMenu.md)   
 [CMenu::DestroyMenu](../vs140/CMenu--DestroyMenu.md)   
 [CMenu::LoadMenuIndirect](../vs140/CMenu--LoadMenuIndirect.md)   
 [LoadMenu](http://msdn.microsoft.com/library/windows/desktop/ms647990)