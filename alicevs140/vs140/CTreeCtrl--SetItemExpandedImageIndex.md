---
title: "CTreeCtrl::SetItemExpandedImageIndex"
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
ms.assetid: 174af8a5-ecc4-4697-9a05-0b2b3d839c42
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::SetItemExpandedImageIndex
Sets the index of the image to display when the specified item of the current tree-view control is in the expanded state.  
  
## Syntax  
  
```  
BOOL SetItemExpandedImageIndex(  
     HTREEITEM hItem,   
     int iExpandedImage  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `hItem`|Handle to a tree-view control item.|  
|[in] `iExpandedImage`|The index of the image to display when the specified item is in the expanded state.|  
  
## Return Value  
 `true` if this method is successful; otherwise, `false`.  
  
## Remarks  
 This method sends the [TVM_SETITEM](http://msdn.microsoft.com/library/windows/desktop/bb773758) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. This method assigns the `iExpandedImage` parameter to the `iExpandedImage` member of a [TVITEMEX](http://msdn.microsoft.com/library/windows/desktop/bb773459) structure, and then uses that structure in the message.  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## Example  
 The following code example defines a variable, `m_treeCtrl`, that is used to access the current tree-view control. The code example also defines an unsigned integer and several HTREEITEM variables. These variables are used in the next example.  
  
 [!CODE [NVC_MFC_CTreeCtrl_s1#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl_s1#1)]  
  
## Example  
 The following code example is a trivial test to determine whether the [CTreeCtrl::GetItemExpandedImageIndex](../vs140/CTreeCtrl--GetItemExpandedImageIndex.md) method returns the value set by the [CTreeCtrl::SetItemExpandedImageIndex](../vs140/CTreeCtrl--SetItemExpandedImageIndex.md) method. In an earlier section of the code example, which is not shown, we created a tree-view that consists of a root country/region node for the United States, subnodes for the states of Pennsylvania and Washington, and tree items for cities in those states.  
  
 [!CODE [NVC_MFC_CTreeCtrl_s1#8](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl_s1#8)]  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [TVM_SETITEM](http://msdn.microsoft.com/library/windows/desktop/bb773758)   
 [TVITEMEX](http://msdn.microsoft.com/library/windows/desktop/bb773459)   
 [CTreeCtrl::GetItemExpandedImageIndex](../vs140/CTreeCtrl--GetItemExpandedImageIndex.md)