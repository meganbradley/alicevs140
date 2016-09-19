---
title: "Command Routing in VSPackages"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a9c7f9ae-3594-4557-a314-8cf76f5f8772
caps.latest.revision: 26
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Command Routing in VSPackages
A command is routed in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] based on the context in which it is executed. It is routed from the initial context outward to the global context.  
  
## In This Section  
 [Command Routing Algorithm](../Topic/Command%20Routing%20Algorithm.md)  
 Describes the order of command routing resolution.  
  
 [How Command Context Affects Available Menu Items](../Topic/Command%20Availability.md)  
 Discusses command routing.  
  
 [Commands and Menus Using Interop Assemblies](../Topic/Commands%20and%20Menus%20That%20Use%20Interop%20Assemblies.md)  
 Discusses considerations in routing commands between managed code and COM.  
  
## Related Sections  
 [Selection Context Objects](../Topic/Selection%20Context%20Objects.md)  
 Discusses the model for how you can determine the user's selection context focus on a window.  
  
 [Menus and Toolbars](../Topic/Commands,%20Menus,%20and%20Toolbars.md)  
 Explains how to create a UI that includes menus, toolbars, and command combo boxes.