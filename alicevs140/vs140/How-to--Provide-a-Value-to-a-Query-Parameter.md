---
title: "How to: Provide a Value to a Query Parameter"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - lightswitch
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5db4a8eb-b833-4048-8c7e-0224af79aa16
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Provide a Value to a Query Parameter
By binding a parameter to a field in a screen, you can enable users to provide the value of a query parameter.  
  
 Users can provide a value either directly or implicitly. They can type the value directly into a text box or they can select an item from a related list on the screen. For example, to view a list of sales orders, a user can type the ID number of a customer or select a customer from a customer list.  
  
 To enable users to type a value, bind the parameter to a field in the screen. To enable users to provide the value implicitly, bind the parameter to a field in a list that appears on the screen. For example, you might bind the `CustomerID` parameter of an `Orders` query to the `CustomerID` field of a **Customers** list.  
  
 ![link to video](../vs140/media/PlayVideo.gif "PlayVideo") For a related video demonstration, see [How Do I: Pass a Parameter into a Screen from the Command Bar in a LightSwitch Application?](http://go.microsoft.com/fwlink/?LinkID=205131).  
  
#### To Bind a Query Parameter to a Field  
  
1.  Create a query that accepts a parameter (for example: the ID of a customer). For more information, see [How to: Design a Query by Using the Query Designer](../Topic/How%20to:%20Design%20a%20Query%20by%20Using%20the%20Query%20Designer.md).  
  
2.  Add the query to the **Screen Content Tree**. For more information, see [How to: Design a Screen by Using the Screen Designer](../Topic/How%20to:%20Design%20a%20Silverlight%20Screen%20by%20Using%20the%20Screen%20Designer.md).  
  
3.  Add a local field to the screen. For more information, see [How to: Add a Local Field to a Screen](../vs140/How-to--Add-a-Local-Property-to-a-Silverlight-Screen.md).  
  
4.  In the **Screen Members List** of the **Screen Designer**, select the parameter of the query.  
  
5.  On the **View** menu, click **Properties Window**.  
  
6.  Select the **Parameter Value** text box.  
  
7.  Select or type the name of the local field.  
  
#### To Bind a Query Parameter to a Field in a List  
  
1.  Create a query that accepts a parameter (for example: the ID of a customer). For more information, see [How to: Design a Query by Using the Query Designer](../Topic/How%20to:%20Design%20a%20Query%20by%20Using%20the%20Query%20Designer.md).  
  
2.  Add the query to the Screen Content Tree. For more information, see [How to: Add Data to a Screen](../vs140/How-to--Add-Data-to-a-Screen.md).  
  
3.  Add a second query to the **Screen Content Tree**. Make sure that the entity returned by this query contains a field that matches the parameter of the first query.  
  
     For example, if the first query accepts a customer ID as a parameter, make sure that the second query returns an entity that contains a customer ID field.  
  
4.  In the **Screen Members List** of the **Screen Designer**, select the parameter of the query.  
  
5.  On the **View** menu, click **Properties Window**.  
  
6.  Select the **Parameter Value** text box.  
  
7.  Select or type the fully qualified name of a field from the second query (for example: **CustomerList.SelectedItem.CustomerID**).  
  
## Next Steps  
 To learn how provide parameter values to a query by using code, see [How to: Retrieve Data from a Query by Using Code](../vs140/How-to--Retrieve-Data-from-a-Query-by-Using-Code.md).  
  
## See Also  
 [Queries: Providing Targeted Information](../Topic/Queries:%20Retrieving%20Information%20from%20a%20Data%20Source.md)   
 [How to: Add, Remove, and Modify a Query](../vs140/How-to--Add--Remove--and-Modify-a-Query.md)   
 [Walkthrough: The Screen Designer](../vs140/Walkthrough--Designing-a-Silverlight-Screen-in-LightSwitch.md)   
 [How to: Design a Query by Using the Query Designer](../Topic/How%20to:%20Design%20a%20Query%20by%20Using%20the%20Query%20Designer.md)   
 [How to: Retrieve Data From a Query by Using Code](../vs140/How-to--Retrieve-Data-from-a-Query-by-Using-Code.md)