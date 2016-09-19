---
title: "CTreeCtrl::SetAutoscrollInfo"
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
ms.assetid: 1f61d554-5885-40d8-a02f-bbbef1fd6da8
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::SetAutoscrollInfo
Sets the autoscroll rate of the current tree-view control.  
  
## Syntax  
  
```  
BOOL SetAutoscrollInfo(  
     UINT uPixelsPerSec,   
     UINT uUpdateTime  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `uPixelsPerSec`|The number of pixels per second to scroll.|  
|[in] `uUpdateTime`|The time interval between updates of the control.|  
  
## Return Value  
 Always returns `true`.  
  
## Remarks  
 The autoscroll parameters are used to scroll into view an item that is currently not visible. The tree-view control must have the `TVS_EX_AUTOHSCROLL` extended style, which is described in [Tree-View Control Extended Styles](http://msdn.microsoft.com/library/windows/desktop/bb759981).  
  
 This method sends the [TVM_SETAUTOSCROLLINFO](http://msdn.microsoft.com/library/windows/desktop/bb773738) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This method is supported in Windows XP and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## Example  
 The following code example defines a variable, `m_treeCtrl`, that is used to access the current tree-view control. The code example also defines an unsigned integer and several HTREEITEM variables. These variables are used in the next example.  
  
 [!CODE [NVC_MFC_CTreeCtrl_s1#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl_s1#1)]  
  
## Example  
 The following code example sets the autoscroll behavior of the current tree-view control. In an earlier section of the code example, which is not shown, we created a tree-view that consists of a root country/region node for the United States, subnodes for the states of Pennsylvania and Washington, and tree items for cities in those states. We intentionally made the tree-view control narrow so that it must automatically scroll to display the tree item that has the focus. The code example sets the tree-view control to automatically scroll 30 pixels per second every 5 seconds until the tree item is in view.  
  
 [!CODE [NVC_MFC_CTreeCtrl_s1#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl_s1#4)]  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [TVM_SETAUTOSCROLLINFO](http://msdn.microsoft.com/library/windows/desktop/bb773738)   
 [Tree-View Control Extended Styles](http://msdn.microsoft.com/library/windows/desktop/bb759981)