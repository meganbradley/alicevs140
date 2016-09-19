---
title: "Performing Data-Related Tasks by Using Code"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - lightswitch
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6531546b-8435-4200-82c0-5d7a4f9f4a49
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Performing Data-Related Tasks by Using Code
You can use the designers and tool windows in [!INCLUDE[smb_current_long](../vs140/includes/smb_current_long_md.md)] to accomplish many data-related design tasks.  However, certain tasks can only be accomplished by adding code to an application. For example, to validate a field by applying custom conditions, you must write code.  This document shows how to accomplish data-related tasks by using the data runtime object model. For more information about where you can write code in an application, see the following topics:  
  
-   [How to: Handle Data Entity Events](../vs140/How-to--Handle-Data-Events.md)  
  
-   [How to: Handle Screen Events](../vs140/How-to--Handle-Silverlight-Screen-Events.md)  
  
-   [How to: Handle Query Events](../vs140/How-to--Handle-Query-Events.md)  
  
## Common Tasks  
 The following list shows common data-related tasks that you can accomplish by using the data runtime object model. The tasks are described later in this document.  
  
-   [Reading Data](#ReadingData)  
  
-   [Updating Data](#UpdatingData)  
  
-   [Deleting Data](#DeletingData)  
  
-   [Adding Data](#CreatingAnd)  
  
-   [Saving Data](#SavingData)  
  
-   [Validating Data](#ValidatingFields)  
  
-   [Setting Permissions on Data](#SettingPermissions)  
  
-   [Working with Change Sets](#WorkingWith)  
  
-   [Extending Queries](#ExtendingModeled)  
  
##  <a name="ReadingData"></a> Reading Data  
 You can read individual data items or collections of data items from any data source in your application.  
  
 The following example retrieves the customer that is currently selected in a screen.  
  
 [!CODE [LS_Data#5](../CodeSnippet/VS_Snippets_Misc/ls_data#5)]  
  
 The following example iterates over a collection of customers.  
  
 [!CODE [LS_Data#6](../CodeSnippet/VS_Snippets_Misc/ls_data#6)]  
  
### Navigating Data Relationships  
 You can read data from related entities. For example, a Customer entity might have a one-to-many relationship with an Orders entity. You could iterate over all orders that have been placed by a customer by using the **Orders** property of the Customer entity.  
  
 The following example iterates over the collection of orders that are related to a customer.  
  
 [!CODE [LS_Data#7](../CodeSnippet/VS_Snippets_Misc/ls_data#7)]  
  
 The following example gets the customer who placed a specific order.  
  
 [!CODE [LS_Data#8](../CodeSnippet/VS_Snippets_Misc/ls_data#8)]  
  
### Reading Data by Executing a Query  
 You can retrieve queries from the model and then execute them in your code. To view an example, see [How to: Retrieve Data from a Query by Using Code](../vs140/How-to--Retrieve-Data-from-a-Query-by-Using-Code.md).  
  
##  <a name="UpdatingData"></a> Updating Data  
 You can update data for any entity by using code. The following example shows code that runs when a user creates an order in the Order entity in a screen and then clicks the **Save** button. The code updates a field in the Products entity by using a field in the Order Details entity.  
  
 [!CODE [LS_Data#9](../CodeSnippet/VS_Snippets_Misc/ls_data#9)]  
  
> [!NOTE]
>  If your code modifies data from other data sources, you must commit those changes by calling the `SaveChanges` method of that data source.  
  
##  <a name="DeletingData"></a> Deleting Data  
 You can delete data by calling the `Delete` method of any entity. The following example deletes a customer from the NorthwindData data source.  
  
 [!CODE [LS_Data#10](../CodeSnippet/VS_Snippets_Misc/ls_data#10)]  
  
##  <a name="CreatingAnd"></a> Adding Data  
 The following example adds a new customer to the NorthwindData data source.  This example populates the fields that describe the new customer by using information from a contact that was recently added to a SharePoint list. The example calls a query named `NewCustomersInSharePoint` to determine which contacts in the SharePoint list have not yet been imported to the NorthwindData data source.  
  
 [!CODE [LS_Data#11](../CodeSnippet/VS_Snippets_Misc/ls_data#11)]  
  
##  <a name="SavingData"></a> Saving Data  
 Typically, pending changes are committed to a data source when the user clicks the **Save** button in a screen. However, you can also commit pending changes by adding code that calls the `SaveChanges` method of a data source. You must add this code if you want to accomplish either of these tasks:  
  
-   Commit changes that you make to data that is located in other data sources.  
  
-   Override the `Save` event of a screen.  
  
### Committing Changes That You Make to Data That Is Located in Other Data Sources  
 The files in which you write custom code have a primary data source. If you add custom code that modifies data from another data source in your [!INCLUDE[smb_current_short](../vs140/includes/smb_current_short_md.md)] solution, you must commit those changes by calling the `SaveChanges` method of that data source.  
  
 The following example shows code that runs when a user creates an order in an Order entity in a screen and then clicks the **Save** button. The code updates a field in the Products entity by using a field in the Order Details entity.  Because the Products entity is located in another data source, this code calls the `SaveChanges` method of that data source to commit the changes.  
  
 [!CODE [LS_Data#16](../CodeSnippet/VS_Snippets_Misc/ls_data#16)]  
  
### Overriding the Save Event of a Screen  
 You can change the behavior of the **Save** button on a screen by overriding the `Save` event. Because you are replacing the behavior of the **Save** button, your code must call the `SaveChanges` method when you want to commit pending changes.  
  
 The following example overrides the `Save` event of a customer screen to catch and handle a specific exception that might be thrown if the save operation fails.  
  
 [!CODE [LS_Data#12](../CodeSnippet/VS_Snippets_Misc/ls_data#12)]  
  
##  <a name="ValidatingFields"></a> Validating Data  
 You can apply custom validation rules to the fields of an entity. You can add custom error messages that appear when users modify the value of properties in ways that do not conform to your validation rules. For more information, see [How to: Validate an Entity](../vs140/How-to--Validate-Data-in-a-LightSwitch-Application.md)  
  
##  <a name="SettingPermissions"></a> Setting Permissions on Data  
 By default, all users can view, insert, delete, or update data that appears in a screen. However, you can restrict these permissions by adding code to one of the following methods:  
  
-   `CanRead`  
  
-   `CanInsert`  
  
-   `CanDelete`  
  
-   `CanUpdate`  
  
 If you restrict an operation by using these methods, [!INCLUDE[smb_current_short](../vs140/includes/smb_current_short_md.md)] makes the operation unavailable to users who do not have unrestricted permissions. For more information, see [How to: Handle Data Entity Events](../vs140/How-to--Handle-Data-Events.md).  
  
 The following example enables a user to update customer information if the user has update permission. This code example requires a permissions group named `RoleUpdate`. For more information about how to add a permissions group to your application, see [Creating Roles and Permissions](../vs140/Enabling-Authorization-and-Creating-Permissions-in-LightSwitch.md).  
  
 [!CODE [LS_Data#13](../CodeSnippet/VS_Snippets_Misc/ls_data#13)]  
  
 By default, [!INCLUDE[smb_current_short](../vs140/includes/smb_current_short_md.md)] calls these methods when a user attempts to view, insert, delete, or update information. You can also call these methods in your custom code before data is read or modified.  
  
##  <a name="WorkingWith"></a> Working with Change Sets  
 You can identify and discard pending changes before they are committed to a data source. The following example shows three user methods that identify and discard pending changes. The `UndoAllCustomerUpdates` method discards all changes made to all customers. The `UndoAllUpdates` method discards all changes made to the data source. The `UndoCustomerEdit` method discards changes made to the currently selected row of data in a customer screen.  
  
 [!CODE [LS_Data#14](../CodeSnippet/VS_Snippets_Misc/ls_data#14)]  
  
##  <a name="ExtendingModeled"></a> Extending Modeled Queries  
 If you want to modify a query beyond the capabilities of the Query Designer, you can extend the query by adding code to the `PreProcessQuery` method of the query. For more information, see [How to: Extend a Query by Using Code](../Topic/How%20to:%20Extend%20a%20Query%20by%20Using%20Code.md).