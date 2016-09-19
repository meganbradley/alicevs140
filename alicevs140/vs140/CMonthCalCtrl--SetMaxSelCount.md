---
title: "CMonthCalCtrl::SetMaxSelCount"
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
ms.assetid: e4095510-c98b-4928-be2b-b31be59f9583
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMonthCalCtrl::SetMaxSelCount
Sets the maximum number of days that can be selected in a month calendar control.  
  
## Syntax  
  
```  
  
      BOOL SetMaxSelCount(  
   int nMax   
);  
```  
  
#### Parameters  
 `nMax`  
 The value that will be set to represent the maximum number of selectable days.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [MCM_SETMAXSELCOUNT](http://msdn.microsoft.com/library/windows/desktop/bb761008), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CMonthCalCtrl#8](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CMonthCalCtrl#8)]  
  
## Requirements  
 **Header:** afxdtctl.h  
  
## See Also  
 [CMonthCalCtrl Class](../vs140/CMonthCalCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMonthCalCtrl::GetMaxSelCount](../vs140/CMonthCalCtrl--GetMaxSelCount.md)