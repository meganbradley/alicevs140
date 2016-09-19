---
title: "How to: Modify a Silverlight Screen by Using Code"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - lightswitch
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3db470ec-fd3b-4ec0-be27-7352fe96974d
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Modify a Silverlight Screen by Using Code
[!INCLUDE[smb_current_long](../vs140/includes/smb_current_long_md.md)] enables you to accomplish many screen-related design tasks by using designers and tool windows.  However, there are certain tasks that you might want to accomplish by using code.  This topic shows you how to accomplish a set of common screen-related design tasks by using the screen object model. For more information about where you can write code in your application, see any of the following topics:  
  
-   [How to: Handle Data Entity Events](../vs140/How-to--Handle-Data-Events.md)  
  
-   [How to: Handle Screen Events](../vs140/How-to--Handle-Silverlight-Screen-Events.md)  
  
-   [How to: Handle Query Events](../vs140/How-to--Handle-Query-Events.md)  
  
## Common Tasks  
 The following list describes some common data-related tasks that you accomplish by using the screen object model.  
  
-   [Making controls hidden, read-only, or disabled](#ReadingData)  
  
##  <a name="ReadingData"></a> Making Controls Hidden, Read-Only, or Disabled  
 You can hide or show controls on a screen by using code. You can also specify whether controls are read-only or disabled.  
  
 The following example hides a company name in a data grid if the company name is `Great Lakes Food Market`. This example also makes the control read-only so that viewers cannot modify the company name by typing text into the control.  
  
 [!CODE [LS_Screens#4](../CodeSnippet/VS_Snippets_Misc/ls_screens#4)]  
  
 The following example hides the company name in a details view on the screen if the company name of the selected item is `Great Lakes Food Market`. This example also disables the **Delete** button so that users cannot delete a customer who works for `Great Lakes Food Market`.  
  
 [!CODE [LS_Screens#5](../CodeSnippet/VS_Snippets_Misc/ls_screens#5)]  
  
## See Also  
 [Screens: What the User Sees](../vs140/Screens--The-User-Interface-of-Your-LightSwitch-Application.md)   
 [How to: Handle Screen Events](../vs140/How-to--Handle-Silverlight-Screen-Events.md)   
 [Performing Data-Related Tasks by Using Code](../vs140/Performing-Data-Related-Tasks-by-Using-Code.md)