---
title: "CHeaderCtrl::SetFilterChangeTimeout"
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
ms.assetid: 768dfe94-e377-4ca8-8916-f51f764b70a2
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeaderCtrl::SetFilterChangeTimeout
Sets the timeout interval between the time a change takes place in the filter attributes and the posting of an [HDN_FILTERCHANGE](http://msdn.microsoft.com/library/windows/desktop/bb775277) notification.  
  
## Syntax  
  
```  
  
      int SetFilterChangeTimeout(  
   DWORD dwTimeOut   
);  
```  
  
#### Parameters  
 *dwTimeOut*  
 Timeout value, in milliseconds.  
  
## Return Value  
 The index of the filter control being modified.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [HDM_SETFILTERCHANGETIMEOUT](http://msdn.microsoft.com/library/windows/desktop/bb775359), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CHeaderCtrl#15](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CHeaderCtrl#15)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CHeaderCtrl Class](../vs140/CHeaderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHeaderCtrl::ClearAllFilters](../vs140/CHeaderCtrl--ClearAllFilters.md)   
 [CHeaderCtrl::ClearFilter](../vs140/CHeaderCtrl--ClearFilter.md)   
 [CHeaderCtrl::EditFilter](../vs140/CHeaderCtrl--EditFilter.md)