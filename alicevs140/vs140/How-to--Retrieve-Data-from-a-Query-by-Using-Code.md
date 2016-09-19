---
title: "How to: Retrieve Data from a Query by Using Code"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - lightswitch
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c3393804-5285-4ceb-b4f8-078566a43a23
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Retrieve Data from a Query by Using Code
You can retrieve queries from the model and then execute them in your code. This enables you to work with targeted collections of data in the business logic of your application.  
  
 For example, your model might contain a query named `Products in Stock`. To determine if a product is available, you can write validation code that retrieves the `Products in Stock` query, and then executes the query. After the query executes, your code can iterate over the resulting collection. If a product in this collection matches a product in the current sales order, the user can notify the customer about the delay.  
  
 You can also add code to narrow the results of a query by using a `where` clause. Using a where clause to narrow the results of a query can improve performance because the conditions of the where clause are applied on the server tier. For more information, see [Queries: Providing Targeted Information](../Topic/Queries:%20Retrieving%20Information%20from%20a%20Data%20Source.md).  
  
## Example: Retrieving Data from a Query and Iterating through the Results  
 The following helper method is called when a user adds a new line to a sales order. If you had an entity named `Order_Details`, you might call this method from the `Order_Details_Inserting` method.  
  
 This code retrieves the top ten customers based on sales orders by executing a query named `TopNSalesOrders`.  If the ID of the customer who placed this order matches the ID of any customers returned by the query, a 10% discount is applied to the line item.  
  
 [!CODE [LS_Queries#3](../CodeSnippet/VS_Snippets_Misc/ls_queries#3)]  
  
## Example: Narrowing the Results of a Query by Applying a Where Clause  
 The following code can be used as an alternative to the previous example. This code applies a where clause to the `TopNSalesOrders` query and only returns a customer if the customer is placing the current order..  
  
 [!CODE [LS_Queries#4](../CodeSnippet/VS_Snippets_Misc/ls_queries#4)]  
  
## Next Steps  
 To learn how to design a query visually by using a designer, see [How to: Design a Query by Using the Query Designer](../Topic/How%20to:%20Design%20a%20Query%20by%20Using%20the%20Query%20Designer.md).  
  
 To learn how to extend a query in the model by using code, see [How to: Extend a Query by Using Code](../Topic/How%20to:%20Extend%20a%20Query%20by%20Using%20Code.md).  
  
## See Also  
 [Queries: Providing Targeted Information](../Topic/Queries:%20Retrieving%20Information%20from%20a%20Data%20Source.md)   
 [How to: Add, Remove, and Modify a Query](../vs140/How-to--Add--Remove--and-Modify-a-Query.md)   
 [Walkthrough: The Screen Designer](../vs140/Walkthrough--Designing-a-Silverlight-Screen-in-LightSwitch.md)   
 [How to: Design a Query by Using the Query Designer](../Topic/How%20to:%20Design%20a%20Query%20by%20Using%20the%20Query%20Designer.md)   
 [How to: Extend a Query by Using Code](../Topic/How%20to:%20Extend%20a%20Query%20by%20Using%20Code.md)