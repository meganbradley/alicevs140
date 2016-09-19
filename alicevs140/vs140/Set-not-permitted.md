---
title: "Set not permitted"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 809f6768-7dd7-4632-b4dd-83856edfdb48
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Set not permitted
You attempted to change a property whose settings either cannot be set at run time or else can only be set under certain conditions. For example, you may have tried to change the `Appearance`, `ControlBox`,`MinButton`, or `MaxButton` property settings for the form at run time, or you may have tried to set the `Visible` property to `False` for the last remaining visible submenu on a parent menu.  
  
### To correct this error  
  
1.  Check the property and determine under what conditions it can be set.  
  
## See Also  
 [NIB How to: Modify Project Properties and Configuration Settings](assetId:///e7184bc5-2f2b-4b4f-aa9a-3ecfcbc48b67)