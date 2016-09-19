---
title: "CMFCToolBarsCustomizeDialog::OnAfterChangeTool"
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
ms.assetid: b937e3cc-6ca0-4b1d-ac2d-34c8447c6930
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarsCustomizeDialog::OnAfterChangeTool
Responds to a change in a user tool immediately after it occurs.  
  
## Syntax  
  
```  
virtual void OnAfterChangeTool(  
   CUserTool* pSelTool   
);  
```  
  
#### Parameters  
 [in, out] `pSelTool`  
 A pointer to the user tool object that has been changed.  
  
## Remarks  
 This method is called by the framework when a user changes the properties of a user-defined tool. The default implementation does nothing. Override this method in a class derived from [CMFCToolBarsCustomizeDialog](../vs140/CMFCToolBarsCustomizeDialog-Class.md) to perform processing after a change to a user tool occurs.  
  
## Requirements  
 **Header:** afxToolBarsCustomizeDialog.h  
  
## See Also  
 [CMFCToolBarsCustomizeDialog Class](../vs140/CMFCToolBarsCustomizeDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)