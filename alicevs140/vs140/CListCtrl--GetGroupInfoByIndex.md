---
title: "CListCtrl::GetGroupInfoByIndex"
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
ms.assetid: 6da6fae9-98df-432f-be4e-e9592e281c00
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetGroupInfoByIndex
Retrieves information about a specified group in the current list-view control.  
  
## Syntax  
  
```  
BOOL GetGroupInfoByIndex(  
     int iIndex,   
     PLVGROUP pGroup  
) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `iIndex`|Zero-based index of a group.|  
|[out] `pGroup`|Pointer to an [LVGROUP](http://msdn.microsoft.com/library/windows/desktop/bb774769) structure that receives information about the group specified by the `iIndex` parameter.<br /><br /> The caller is responsible for initializing the members of the [LVGROUP](http://msdn.microsoft.com/library/windows/desktop/bb774769) structure. Set the `cbSize` member to the size of the structure, and the flags of the `mask` member to specify the information to retrieve.|  
  
## Return Value  
 `true` if this method is successful; otherwise, `false`.  
  
## Remarks  
 This method sends the [LVM_GETGROUPINFOBYINDEX](http://msdn.microsoft.com/library/windows/desktop/bb774933) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This control is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## Example  
 The following code example defines a variable, `m_listCtrl`, that is used to access the current list-view control. This variable is used in the next example.  
  
 [!CODE [NVC_MFC_CListCtrl_s2#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl_s2#6)]  
  
## Example  
 The following code example demonstrates the `GetGroupInfoByIndex` method. In an earlier section of this code example we created a list-view control that displays two columns titled "ClientID" and "Grade" in a report view. The following code example retrieves information about the group whose index is 0, if such a group exists.  
  
 [!CODE [NVC_MFC_CListCtrl_s2#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl_s2#2)]  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [LVM_GETGROUPINFOBYINDEX](http://msdn.microsoft.com/library/windows/desktop/bb774933)   
 [LVGROUP](http://msdn.microsoft.com/library/windows/desktop/bb774769)