---
title: "CProgressCtrl::GetRange"
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
ms.assetid: 3c7beb69-9024-4e12-a9e8-38b4031a5c9d
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CProgressCtrl::GetRange
Gets the current lower and upper limits, or range, of the progress bar control.  
  
## Syntax  
  
```  
  
      void GetRange(   
   int& nLower,    
   int& nUpper    
);  
```  
  
#### Parameters  
 `nLower`  
 A reference to an integer receiving the lower limit of the progress bar control.  
  
 `nUpper`  
 A reference to an integer receiving the upper limit of the progress bar control.  
  
## Remarks  
 This function copies the values of the lower and upper limits to the integers referenced by `nLower` and `nUpper`, respectively.  
  
## Example  
 [!CODE [NVC_MFC_CProgressCtrl#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CProgressCtrl#4)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CProgressCtrl Class](../vs140/CProgressCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [PBRANGE](http://msdn.microsoft.com/library/windows/desktop/bb760822)   
 [PBM_GETRANGE](http://msdn.microsoft.com/library/windows/desktop/bb760832)