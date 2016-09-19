---
title: "CMFCToolBarsCustomizeDialog::OnBeforeChangeTool"
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
ms.assetid: 141a9f95-c278-4db8-9976-ef2b16252e2b
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarsCustomizeDialog::OnBeforeChangeTool
Performs custom processing when a change to a user tool when the user is about to apply a change.  
  
## Syntax  
  
```  
virtual void OnBeforeChangeTool(  
   CUserTool* pSelTool   
);  
```  
  
#### Parameters  
 [in, out] `pSelTool`  
 A pointer to the user tool object that is about to be replaced.  
  
## Remarks  
 This method is called by the framework when the properties of a user-defined tool is about to change. The default implementation does nothing. Override the `OnBeforeChangeTool` method in a class derived from [CMFCToolBarsCustomizeDialog](../vs140/CMFCToolBarsCustomizeDialog-Class.md) if you want to perform processing before a change to a user tool occurs, such as releasing resources that `pSelTool` uses.  
  
## Requirements  
 **Header:** afxToolBarsCustomizeDialog.h  
  
## See Also  
 [CMFCToolBarsCustomizeDialog Class](../vs140/CMFCToolBarsCustomizeDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)