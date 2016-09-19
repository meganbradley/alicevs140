---
title: "Toolbar Button Properties"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b2705814-7c5d-4f24-8f77-07559b0cdda2
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Toolbar Button Properties
The properties of a toolbar button are:  
  
|Property|Description|  
|--------------|-----------------|  
|**ID**|Defines the ID for the button. The drop-down list provides common **ID** names.|  
|**Width**|Sets the width of the button. 16 pixels is recommended.|  
|**Height**|Sets the height of the button. Note that the height of one button changes the height of all buttons on the toolbar. 15 pixels is recommended.|  
|**Prompt**|Defines the message displayed in the status bar. Adding \n and a name adds a ToolTip to that toolbar button. For more information, see [Creating a ToolTip](../vs140/Creating-a-Tool-Tip-for-a-Toolbar-Button.md).|  
  
 **Width** and **Height** apply to all buttons. A bitmap that is used to create a toolbar has a maximum width of 2048. So if you set the button width to 512, you can only have four buttons and if you set the width to 513, you can only have three buttons.  
  
 For information on adding resources to managed projects, please see [Resources in Applications](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890) in the *.NET Framework Developer's Guide.* For information on manually adding resource files to managed projects, accessing resources, displaying static resources, and assigning resources strings to properties, see [Walkthrough: Localizing Windows Forms](assetId:///9a96220d-a19b-4de0-9f48-01e5d82679e5) and [Walkthrough: Using Resources for Localization with ASP.NET](assetId:///bb4e5b44-e2b0-48ab-bbe9-609fb33900b6).  
  
## Requirements  
 MFC or ATL  
  
## See Also  
 [Changing the Properties of a Toolbar Button](../vs140/Changing-the-Properties-of-a-Toolbar-Button.md)   
 [Toolbar Editor](../vs140/Toolbar-Editor.md)