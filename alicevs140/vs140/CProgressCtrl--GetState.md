---
title: "CProgressCtrl::GetState"
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
ms.assetid: 8eb06e30-7384-4862-aff9-e73f20ecdcf6
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CProgressCtrl::GetState
Gets the state of the current progress bar control.  
  
## Syntax  
  
```  
int GetState() const;  
```  
  
## Return Value  
 The state of the current progress bar control, which is one of the following values:  
  
|Value|State|  
|-----------|-----------|  
|`PBST_NORMAL`|In progress|  
|`PBST_ERROR`|Error|  
|`PBST_PAUSED`|Paused|  
  
## Remarks  
 This method sends the [PBM_GETSTATE](http://msdn.microsoft.com/library/windows/desktop/bb760834) message, which is described in the[!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This control is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## Example  
 The following code example defines the variable, `m_progressCtrl`, that is used to programmatically access the progress bar control. This variable is used in the next example.  
  
 [!CODE [NVC_MFC_CProgressCtrl_s1#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CProgressCtrl_s1#9)]  
  
## Example  
 The following code example retrieves the state of the current progress bar control.  
  
 [!CODE [NVC_MFC_CProgressCtrl_s1#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CProgressCtrl_s1#5)]  
  
## See Also  
 [CProgressCtrl Class](../vs140/CProgressCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Using CProgressCtrl](../vs140/Using-CProgressCtrl.md)   
 [PBM_GETSTATE](http://msdn.microsoft.com/library/windows/desktop/bb760834)   
 [CProgressCtrl::SetState](../vs140/CProgressCtrl--SetState.md)