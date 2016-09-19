---
title: "CStatusBarCtrl::GetIcon"
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
ms.assetid: 35f651c0-ebc9-4a40-8d27-23d5c6e324f1
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStatusBarCtrl::GetIcon
Retrieves the icon for a part (also known as a pane) in the current status bar control.  
  
## Syntax  
  
```  
HICON GetIcon(  
      int iPart  
) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `iPart`|The zero-based index of the part that contains the icon to be retrieved. If this parameter is -1, the status bar is assumed to be a simple mode status bar.|  
  
## Return Value  
 The handle to the icon if the method successful; otherwise, `NULL`.  
  
## Remarks  
 This method sends the [SB_GETICON](http://msdn.microsoft.com/library/windows/desktop/bb760744) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 A status bar control consists of a row of text output panes, which are also known as parts. For more information about the status bar, see [Status Bar Implementation in MFC](../vs140/Status-Bar-Implementation-in-MFC.md) and [Setting the Mode of a CStatusBarCtrl Object](../vs140/Setting-the-Mode-of-a-CStatusBarCtrl-Object.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## Example  
 The following code example defines a variable, `m_statusBar`, that is used to access the current status bar control. This variable is used in the next example.  
  
 [!CODE [NVC_MFC_CStatusBarCtrl_s1#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CStatusBarCtrl_s1#1)]  
  
## Example  
 The following code example copies an icon to two panes of the current status bar control. In an earlier section of the code example we created a status bar control with three panes and then added an icon to the first pane. This example retrieves the icon from the first pane and then adds it to the second and third pane.  
  
 [!CODE [NVC_MFC_CStatusBarCtrl_s1#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CStatusBarCtrl_s1#2)]  
  
## See Also  
 [CStatusBarCtrl Class](../vs140/CStatusBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Using CStatusBarCtrl](../vs140/Using-CStatusBarCtrl.md)   
 [SB_GETICON](http://msdn.microsoft.com/library/windows/desktop/bb760744)   
 [CStatusBarCtrl::SetParts](../vs140/CStatusBarCtrl--SetParts.md)