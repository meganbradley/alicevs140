---
title: "CHeaderCtrl::GetItemDropDownRect"
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
ms.assetid: cd4dccd7-5156-4ed8-bada-42472faf5a99
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeaderCtrl::GetItemDropDownRect
Gets the bounding rectangle of the drop-down button for a header item in the current header control.  
  
## Syntax  
  
```  
BOOL GetItemDropDownRect(  
     int iItem,   
     LPRECT lpRect  
) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `iItem`|Zero-based index of a header item whose style is `HDF_SPLITBUTTON`. For more information, see the `fmt` member of the [HDITEM](http://msdn.microsoft.com/library/windows/desktop/bb775247) structure.|  
|[out] `lpRect`|Pointer to a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure to receive the bounding rectangle information.|  
  
## Return Value  
 `true` if this function is successful; otherwise, `false`.  
  
## Remarks  
 This method sends the [HDM_GETITEMDROPDOWNRECT](http://msdn.microsoft.com/library/windows/desktop/bb775339) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## Example  
 The following code example defines the variable, `m_headerCtrl`, that is used to access the current header control. This variable is used in the next example.  
  
 [!CODE [NVC_MFC_CHeaderCtrl_s4#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CHeaderCtrl_s4#6)]  
  
## Example  
 The following code example demonstrates the `GetItemDropDownRect` method. In an earlier section of the code, we created a header control with five columns. The following code example draws a 3D rectangle around the location on the first column that is reserved for the header drop-down button.  
  
 [!CODE [NVC_MFC_CHeaderCtrl_s4#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CHeaderCtrl_s4#2)]  
  
## See Also  
 [CHeaderCtrl Class](../vs140/CHeaderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [HDM_GETITEMDROPDOWNRECT](http://msdn.microsoft.com/library/windows/desktop/bb775339)   
 [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897)   
 [HDITEM](http://msdn.microsoft.com/library/windows/desktop/bb775247)