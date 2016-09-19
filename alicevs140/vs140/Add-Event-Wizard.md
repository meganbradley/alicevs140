---
title: "Add Event Wizard"
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
ms.topic: article
ms.assetid: bdd2a7bb-13d5-44d7-abc9-e785ba4e05ce
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Add Event Wizard
This wizard adds an event to an MFC ActiveX control project. You can specify your own event, you can customize a typically stock event, or you can select from a list of stock events.  
  
 **Event name**  
 Sets the name used by Automation clients to request an event from the class. Enter a name or select one from the list.  
  
 **Event type**  
 Indicates the type of event to add. Available only if you select from the **Event Name** list.  
  
|Option|Description|  
|------------|-----------------|  
|**Stock**|Specifies that a stock event, such as a button click, will be implemented for this class. Stock events are defined in the Microsoft Foundation Class (MFC) Library.|  
|**Custom**|Specifies that you are providing your own implementation of the event.|  
  
 **Internal name**  
 Sets the name of the member function that sends the event. Available only for custom events. The name is based on **Event name**. You can change the internal name if you want to provide a name different than **Event name**.  
  
 **Parameter type**  
 Sets the type for the **Parameter name**. Select the type from the list.  
  
 **Parameter name**  
 Sets the name of a parameter to pass through your event. After typing the name, you must click **Add** to add it the list of parameters.  
  
 Once you click **Add**, the parameter name appears in **Parameter list**.  
  
> [!NOTE]
>  If you supply a parameter name and then click **Finish** before you click **Add**, then the parameter is not added to the event. You must find the method and insert the parameter manually. **Parameter list**  
  
 **Add**  
 Adds the parameter you specify in **Parameter name**, and its type, to **Parameter list**. You must click **Add** to add a parameter to the list.  
  
 **Remove**  
 Removes the parameter you select in **Parameter list** from the list.  
  
 **Parameter list**  
 Displays all parameters and their types currently added for the method. As you add parameters, the wizard updates **Parameter list** to display each parameter with its type.  
  
## See Also  
 [Adding an Event](../vs140/Adding-an-Event--Visual-C---.md)