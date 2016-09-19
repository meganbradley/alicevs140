---
title: "VSPackage State"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6056a9ea-e7a8-481c-9fc8-340229fa12d9
caps.latest.revision: 27
translation.priority.ht: 
  - de-de
  - ja-jp
---
# VSPackage State
Many factors determine the set of persisted values, or state, of a [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] application.  
  
-   Projects have project and configuration properties.  
  
-   Solutions have properties.  
  
-   User settings determine the size and position of document windows, tool windows, docking state, and keyboard shortcuts.  
  
-   Applications can have options that a user sets.  
  
-   Objects that an application creates can have properties of their own.  
  
 Here are some of the ways that a [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] application state can be managed:  
  
-   Through the project and solution property pages.  
  
-   Through the **Import and Export Settings Wizard**, which enables a user to move settings from one computer to another.  
  
-   Through the **Options** dialog box, which includes options related to applications.  
  
-   Through the **Properties** window, which exposes properties of objects.  
  
-   Through Automation. An application can access VSPackage and object properties that have been exposed to Automation.  
  
 Underlying the application state are various persistence mechanisms that enable the application state to be saved and restored.  
  
## In This Section  
 [Support for State Persistence](../Topic/Support%20for%20State%20Persistence.md)  
 Lists common strategies for saving, restoring, and resetting the state of a VSPackage.  
  
 [Support for Tools/Options Pages](../vs140/Options-and-Options-Pages.md)  
 Introduces general and custom Options pages and explains how to implement them.  
  
 [Walkthrough: Creating an Options Page (C#)](../Topic/Creating%20an%20Options%20Page.md)  
 Explains how to create two Options pages, a simple page and a custom page.  
  
 [Support for Settings Categories](../Topic/Support%20for%20Settings%20Categories.md)  
 Discusses user settings and how they are created and persisted.  
  
 [Walkthrough: Creating a Settings Category (C#)](../Topic/Creating%20a%20Settings%20Category.md)  
 Explains how to create a [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] settings category and use it to save values to and restore values from a settings file.  
  
 [Support for the Property Browser](../vs140/Extending-Properties-and-the-Property-Window.md)  
 Explains how to display and change the value of an object in the **Properties** window.  
  
 [Walkthrough: Exposing Properties to the Properties Window (C#)](../Topic/Exposing%20Properties%20to%20the%20Properties%20Window.md)  
 Explains how to expose the public properties of an object to the **Properties** window.  
  
 [Support for Project and Configuration Properties](../Topic/Support%20for%20Project%20and%20Configuration%20Properties.md)  
 Explains how to display and change project and configuration properties.  
  
 [Walkthrough: Retrieving Project Properties (C#)](../vs140/Getting-Project-Properties.md)  
 Guides you through the steps of creating a managed VSPackage that displays project properties in a tool window.  
  
 [Walkthrough: Using the Settings Store](../Topic/Using%20the%20Settings%20Store.md)  
 Explains the Settings Store persistence mechanism and how to use it.  
  
## Related Sections  
 [VSPackages](../vs140/VSPackages.md)  
 Provides a general orientation to topics that explain how to create and use VSPackages.