---
title: "How to: Add Data to a Screen"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - lightswitch
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b00a798a-80eb-4b0b-b57f-ee08066f434c
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Add Data to a Screen
You can add groups of data to a screen. The data can come from any data source in a [!INCLUDE[smb_current_short](../vs140/includes/smb_current_short_md.md)] application.  
  
### To add data to a screen  
  
1.  At the top of the **Screen Designer**, click **Add Data Item**.  
  
2.  In the **Add Data Item** dialog box, select **Query**.  
  
3.  In the list of queries, select a query that returns the data that you want. Queries that end with the label **(All)** return a collection of data. Queries that end with the label **(Single)** return an individual item of data.  
  
4.  In the **Name** box, type a name, and then click **OK**.  
  
     The query that you selected appears in the screen members list.  
  
5.  From the **Screen Members List**, drag the query onto the desired area of the **Screen Content Tree**.  
  
     If the query returns a collection of data, a group appears in the **Screen Content Tree**. This group contains the fields of data returned by the query.  
  
     If the query returns an individual item of data, a control that is appropriate for displaying an individual item of data, such as a text box, appears in the **Screen Content Tree**.  
  
## Next Steps  
 Add commands to the group. For more information, see [How to: Add a Custom Command to a Screen](../vs140/How-to--Add-a-Custom-Command-to-a-Silverlight-Screen.md) or [How to: Add a Custom Command to an HTML Screen](../vs140/How-to--Add-a-Button-to-a-Mobile-Client-for-LightSwitch.md).  
  
 Customize how the data in the group is filtered. For more information, see [How to: Filter Data on a Screen](../vs140/How-to--Filter-Data-on-a-Silverlight-Screen.md) or [How to: Filter Data on an HTML Screen](../vs140/How-to--Filter-Data-in-an-HTML-Client-for-a-LightSwitch-App.md).  
  
 Move groups to other positions on the screen or change the layout of the data in the group. For more information, see [How to: Design a Screen by Using the Screen Designer](../Topic/How%20to:%20Design%20a%20Silverlight%20Screen%20by%20Using%20the%20Screen%20Designer.md) or [How to: Design an HTML Screen by Using the Screen Designer](../vs140/How-to--Design-an-HTML-Screen-by-Using-the-Screen-Designer.md).  
  
## See Also  
 [Screens: The User Interface of Your Application](../vs140/Screens--The-User-Interface-of-Your-LightSwitch-Application.md)