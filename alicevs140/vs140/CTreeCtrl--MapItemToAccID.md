---
title: "CTreeCtrl::MapItemToAccID"
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
ms.assetid: 56d9a00c-28e4-4e6a-b489-96b7916c2864
caps.latest.revision: 21
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::MapItemToAccID
Maps the specified handle of a tree-view item in the current tree-view control to an accessibility identifier.  
  
## Syntax  
  
```  
UINT MapItemToAccID(  
     HTREEITEM hItem  
) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `hItem`|A handle of a tree-view item in the control. For more information, see the `hItem` member of the [TVITEMEX](http://msdn.microsoft.com/library/windows/desktop/bb773459) structure.|  
  
## Return Value  
 The accessibility identifier that corresponds to the `hItem` parameter.  
  
## Remarks  
 Accessibility aids are applications that help people with disabilities use computers. An accessibility identifier is used by the `IAccessible` interface to uniquely specify an element in a window. For more information about accessibility identifiers, search for the "About Active Accessibility Support" topic at [Microsoft Developer Network](http://go.microsoft.com/fwlink/?LinkId=56322).  
  
 This method sends the [TVM_MAPHTREEITEMTOACCID](http://msdn.microsoft.com/library/windows/desktop/bb773735) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This method is supported in Windows XP and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## Example  
 The following code example defines a variable, `m_treeCtrl`, that is used to access the current tree-view control. The code example also defines an unsigned integer and several HTREEITEM variables. These variables are used in the next example.  
  
 [!CODE [NVC_MFC_CTreeCtrl_s1#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl_s1#1)]  
  
## Example  
 The following code example obtains an identification number for a tree-view control item. In an earlier section of the code example, which is not shown, we created a tree-view that consists of a root country/region node for the United States, subnodes for the states of Pennsylvania and Washington, and tree items for cities in those states. This code example obtains a unique identification number for the root country/region node.  
  
 [!CODE [NVC_MFC_CTreeCtrl_s1#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl_s1#2)]  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [TVM_MAPHTREEITEMTOACCID](http://msdn.microsoft.com/library/windows/desktop/bb773735)   
 [TVITEMEX](http://msdn.microsoft.com/library/windows/desktop/bb773459)   
 [CTreeCtrl::MapAccIdToItem](../vs140/CTreeCtrl--MapAccIdToItem.md)