---
title: "CSplitButton::CSplitButton"
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
ms.assetid: 82c3d009-2138-406f-9e74-cf7319931deb
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitButton::CSplitButton
Constructs a `CSplitButton` object. The constructor's parameters specify a submenu that is displayed when a user clicks the drop-down arrow of the split button control.  
  
## Syntax  
  
```  
CSplitButton();  
CSplitButton(  
    UINT nMenuId,   
    UINT nSubMenuId  
)  
CSplitButton(  
    CMenu* pMenu  
)  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `nMenuId`|The resource ID of the menu bar.|  
|[in] `nSubMenuId`|The resource ID of a submenu.|  
|[in] `pMenu`|A pointer to a [CMenu](../vs140/CMenu-Class.md) object that specifies a submenu. The `CSplitButton` object deletes the `CMenu` object and its associated `HMENU` when the `CSplitButton` object goes out of scope.|  
  
## Remarks  
 Use the [CSplitButton::Create](../vs140/CSplitButton--Create.md) method to create a split button control and attach it to the `CSplitButton` object.  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CSplitButton Class](../vs140/CSplitButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSplitButton::Create](../vs140/CSplitButton--Create.md)