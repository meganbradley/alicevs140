---
title: "CComboBox::SetMinVisibleItems"
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
ms.assetid: e7addf4f-a6cb-4df3-bb93-df496154a83a
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::SetMinVisibleItems
Sets the minimum number of visible items in the drop-down list of the current combo box control.  
  
## Syntax  
  
```  
BOOL SetMinVisibleItems(  
     int iMinVisible  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `iMinVisible`|Specifies the minimum number of visible items.|  
  
## Return Value  
 `true` if this method is successful; otherwise, `false`.  
  
## Requirements  
 **Header:** afxwin.h  
  
 This method is supported in Windows XP and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## Remarks  
 This method sends the [CB_SETMINVISIBLE](http://msdn.microsoft.com/library/windows/desktop/bb775915) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 The following code example defines the variable, `m_combobox`, that is used to programmatically access the combo box control. This variable is used in the next example.  
  
 [!CODE [NVC_MFC_CComboBox_s1#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox_s1#1)]  
  
## Example  
 The following code example inserts 20 items into the drop-down list of a combo box control. Then it specifies that a minimum of 10 items be displayed when a user presses the drop-down arrow.  
  
 [!CODE [NVC_MFC_CComboBox_s1#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox_s1#2)]  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::GetMinVisibleItems](../vs140/CComboBox--GetMinVisible.md)   
 [CComboBox::ShowDropDown](../vs140/CComboBox--ShowDropDown.md)   
 [CB_SETMINVISIBLE](http://msdn.microsoft.com/library/windows/desktop/bb775915)