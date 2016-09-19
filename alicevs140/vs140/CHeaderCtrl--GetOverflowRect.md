---
title: "CHeaderCtrl::GetOverflowRect"
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
ms.assetid: 661259b2-f01a-4323-a987-ccde53237b52
caps.latest.revision: 20
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeaderCtrl::GetOverflowRect
Gets the bounding rectangle of the overflow button of the current header control.  
  
## Syntax  
  
```  
BOOL GetOverflowRect(  
     LPRECT lpRect  
) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[out] `lpRect`|Pointer to a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure that receives the bounding rectangle information.|  
  
## Return Value  
 `true` if this function is successful; otherwise, `false`.  
  
## Remarks  
 If the header control contains more items than can be simultaneously displayed, the control can display an overflow button that scrolls to items that are not visible. The header control must have the `HDS_OVERFLOW` and `HDF_SPLITBUTTON` styles to display the overflow button. The bounding rectangle encloses the overflow button and exists only when the overflow button is displayed. For more information, see [Header Control Styles](http://msdn.microsoft.com/library/windows/desktop/bb775241).  
  
 This method sends the [HDM_GETOVERFLOWRECT](http://msdn.microsoft.com/library/windows/desktop/bb775345) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This control is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## Example  
 The following code example defines the variable, `m_headerCtrl`, that is used to access the current header control. This variable is used in the next example.  
  
 [!CODE [NVC_MFC_CHeaderCtrl_s4#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CHeaderCtrl_s4#6)]  
  
## Example  
 The following code example demonstrates the `GetOverflowRect` method. In an earlier section of the code, we created a header control with five columns. However, you can drag a column separator so that the column is not visible. If some columns are not visible, the header control draws an overflow button. The following code example draws a 3D rectangle around the location of the overflow button.  
  
 [!CODE [NVC_MFC_CHeaderCtrl_s4#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CHeaderCtrl_s4#3)]  
  
## See Also  
 [CHeaderCtrl Class](../vs140/CHeaderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [HDM_GETOVERFLOWRECT](http://msdn.microsoft.com/library/windows/desktop/bb775345)   
 [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897)