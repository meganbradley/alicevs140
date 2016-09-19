---
title: "Choosing a Screen Type for an HTML Client of a LightSwitch App"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - lightswitch
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 21bd9c95-1508-4550-aff3-cf8cafb54af6
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Choosing a Screen Type for an HTML Client of a LightSwitch App
When you develop an HTML client project by using Visual Studio LightSwitch, you can create the following types of screens:  
  
## Browse Data Screen  
 Create this type of screen to display a list of records, such as a list of appointments or customers. Tapping an item in the list typically opens another screen to display or edit details for the item. This kind of screen typically acts as the home screen for an application.  
  
 ![Browse Data Screen](../vs140/media/LS_Detail.PNG "LS_Detail")  
  
### View Details Screen  
 Create this type of screen to display a single record, such as information about one appointment or one customer, and any related child records. For example, you could create this kind of screen to display information such as the name and address of a customer and a list of orders for that customer. You typically launch this type of screen by using the `ItemTap` method from a **Browse Data** screen.  
  
 ![View Details Screen](../vs140/media/LS_View.PNG "LS_View")  
  
### Add/Edit Details Screen  
 Create this type of screen so that users can create or edit a single record or related child records. You typically launch this type of screen when the user taps a button on another screen.  
  
 ![Add&#47;Edit Details Screen](../vs140/media/LS_Add.PNG "LS_Add")  
  
## Common Screen Set  
 The **Common Screen Set** creates a **Browse Data Screen**, **View Details Screen**, and **Add/Edit Details** screen for an entity in a single step. Common navigation between the screens is automatically enabled when you create a screen set.  
  
## See Also  
 [How to: Create an HTML Client Screen](../vs140/How-to--Create-an-HTML-Client-Screen.md)   
 [How to: Create an HTML Client Dialog](../vs140/How-to--Create-a-Dialog-or-Popup-for-a-Mobile-Client-of-a-LightSwitch-App.md)   
 [HTML Client Applications in LightSwitch](../vs140/HTML-Client-Screens-for-LightSwitch-Apps.md)