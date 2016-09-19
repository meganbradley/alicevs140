---
title: "CWinAppEx::OnAppContextHelp"
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
ms.assetid: 6a58142b-fecc-4644-94c7-f25ce6241fc3
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::OnAppContextHelp
The framework calls this method when the user requests context help for the **Customization** dialog box.  
  
## Syntax  
  
```  
virtual void OnAppContextHelp(  
   CWnd* pWndControl,  
   const DWORD dwHelpIDArray[]   
);  
```  
  
#### Parameters  
 [in] `pWndControl`  
 A pointer to a window object for which the user invoked context help.  
  
 [in] `dwHelpIDArray[]`  
 A reserved value.  
  
## Remarks  
 This method is currently reserved for future use. The default implementation does nothing and it is currently not called by the framework.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)