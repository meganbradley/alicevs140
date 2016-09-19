---
title: "CTreeCtrl::SetExtendedStyle"
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
ms.assetid: 4769a2db-9dd8-4e54-8b38-ecf77f4b3d4c
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::SetExtendedStyle
Sets the extended styles for the current tree-view control.  
  
## Syntax  
  
```  
DWORD SetExtendedStyle(  
      DWORD dwExMask,   
      DWORD dwExStyles  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `dwExMask`|A bitmask that specifies which styles in the current tree-view control are affected by this method. If this parameter is zero, it is ignored and the value of the `dwExStyles` parameter is assigned to the tree-view control.<br /><br /> Specify zero or a bitwise combination (OR) of styles described in [Tree-View Control Extended Styles](http://msdn.microsoft.com/library/windows/desktop/bb759981).|  
|[in] `dwExStyles`|A bitmask that specifies which styles in the current tree-view control to set or clear.<br /><br /> To set a combination of styles, specify a bitwise combination (OR) of styles described in [Tree-View Control Extended Styles](http://msdn.microsoft.com/library/windows/desktop/bb759981). To clear a set of styles, specify zero.|  
  
## Return Value  
 A value that contains the previous extended control styles.  
  
## Remarks  
 This method clears the styles specified in the `dwExMask` parameter, then sets the styles specified in the `dwExStyles` parameter. Only the extended styles that correspond to the bits in `dwExMask` change.  
  
 This method sends the [TVM_SETEXTENDEDSTYLE](http://msdn.microsoft.com/library/windows/desktop/bb773744) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This method is supported in Windows XP and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## Example  
 The following code example defines a variable, `m_treeCtrl`, that is used to access the current tree-view control. The code example also defines an unsigned integer and several HTREEITEM variables. These variables are used in the next example.  
  
 [!CODE [NVC_MFC_CTreeCtrl_s1#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl_s1#1)]  
  
## Example  
 The following code example adds the `TVS_EX_AUTOHSCROLL` extended style to the current tree-view control. In an earlier section of the code example, which is not shown, we created a tree-view that consists of a root country/region node for the United States, subnodes for the states of Pennsylvania and Washington, and tree items for cities in those states. We intentionally made the tree-view control narrow so that it must automatically scroll to display the tree item that has the focus.  
  
 [!CODE [NVC_MFC_CTreeCtrl_s1#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl_s1#3)]  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [TVM_SETEXTENDEDSTYLE](http://msdn.microsoft.com/library/windows/desktop/bb773744)   
 [CTreeCtrl::GetExtendedStyle](../vs140/CTreeCtrl--GetExtendedStyle.md)   
 [Tree-View Control Extended Styles](http://msdn.microsoft.com/library/windows/desktop/bb759981)