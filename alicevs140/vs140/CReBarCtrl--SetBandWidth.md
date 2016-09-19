---
title: "CReBarCtrl::SetBandWidth"
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
ms.assetid: 4cd4f61c-7353-4e4b-9765-8b7a5aaa8e03
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::SetBandWidth
Sets the width of the specified docked band in the current rebar control.  
  
## Syntax  
  
```  
BOOL SetBandWidth(  
     UINT uBand,   
     int cxWidth  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `uBand`|Zero-based index of a rebar band.|  
|[in] `cxWidth`|New width of the rebar band, in pixels.|  
  
## Return Value  
 `true` if the method is successful; otherwise, `false`.  
  
## Remarks  
 This method sends the [RB_SETBANDWIDTH](http://msdn.microsoft.com/library/windows/desktop/bb774511) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## Example  
 The following code example defines the variable, `m_rebar`, that is used to access the current rebar control. This variable is used in the next example.  
  
 [!CODE [NVC_MFC_CReBarCtrl_s1#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CReBarCtrl_s1#1)]  
  
## Example  
 The following code example sets each rebar band to be the same width.  
  
 [!CODE [NVC_MFC_CReBarCtrl_s1#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CReBarCtrl_s1#2)]  
  
## See Also  
 [CReBarCtrl Class](../vs140/CReBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [RB_SETBANDWIDTH](http://msdn.microsoft.com/library/windows/desktop/bb774511)