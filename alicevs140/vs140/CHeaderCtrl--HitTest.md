---
title: "CHeaderCtrl::HitTest"
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
ms.assetid: 952627a8-be76-4422-bf66-5823b19fae5c
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeaderCtrl::HitTest
Determines which header item, if any, is located at a specified point.  
  
## Syntax  
  
```  
int HitTest(  
    LPHDHITTESTINFO* phdhti  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in, out] `phdhti`|Pointer to a [HDHITTESTINFO](http://msdn.microsoft.com/library/windows/desktop/bb775245) structure that specifies the point to test and receives the results of the test.|  
  
## Return Value  
 The zero-based index of the header item, if any, at the specified position; otherwise, –1.  
  
## Remarks  
 This method sends the [HDM_HITTEST](http://msdn.microsoft.com/library/windows/desktop/bb775349) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This method is supported in Windows NT 3.51 and later.  
  
## Example  
 The following code example defines the variable, `m_headerCtrl`, that is used to access the current header control. This variable is used in the next example.  
  
 [!CODE [NVC_MFC_CHeaderCtrl_s4#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CHeaderCtrl_s4#6)]  
  
## Example  
 The following code example demonstrates the `HitTest` method. In an earlier section of this code example, we created a header control with five columns. However, you can drag a column separator so that the column is not visible. This example reports the index of the column if it is visible and -1 if the column is not visible.  
  
 [!CODE [NVC_MFC_CHeaderCtrl_s4#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CHeaderCtrl_s4#1)]  
  
## See Also  
 [CHeaderCtrl Class](../vs140/CHeaderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [HDM_HITTEST](http://msdn.microsoft.com/library/windows/desktop/bb775349)   
 [HDHITTESTINFO](http://msdn.microsoft.com/library/windows/desktop/bb775245)