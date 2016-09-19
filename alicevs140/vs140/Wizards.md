---
title: "Wizards"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 59d9a77f-ee80-474b-a14f-90f477ab717b
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Wizards
After you create a wizard, you typically want to add it to the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] integrated development environment (IDE) so that others can use it. The added wizard then appears in the **Add New Project** or **Add New Item** dialog boxes. To see the **Add New Project** or **Add New Item** dialog boxes, right-click an open solution in **Solution Explorer**, point to **Add**, and then click **New Project** or **New Item**.  
  
 Wizards can be implemented in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] to let users select from a tree view of available values when they open the **Add New Project** dialog box or the **Add New Item** dialog box, or when they right-click an item in **Solution Explorer**.  
  
 In your wizard, you can provide the option of localizing the name of a new project or ites, and you can determine the icon that users will see when they select the wizard. You can also control the order in which new items appear relative to other available items; items do not have to be organized alphabetically.  
  
 You can also supply a wizard that starts differently, based on custom parameters that are passed to the wizard when it is opened.  
  
 The topics in this section discuss the files that you implement to cause the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] **Add New Project** and **Add New Item** dialog boxes to list your wizard among the available wizards and templates, and the requirements that your wizard must meet to operate correctly in the IDE.  
  
## In This Section  
 [Template Directory Description (.Vsdir) Files](../vs140/Template-Directory-Description--.Vsdir--Files.md)  
 Provides an overview of what template directory description files and explains how they function in the IDE to display folders, wizard .vsz files, and template files that are associated with a project in the dialog boxes.  
  
 [Wizard (.Vsz) File](../vs140/Wizard--.Vsz--File.md)  
 Explains how the IDE starts wizards and lists the three parts of the .vsz file.  
  
 [Wizard Interface (IDTWizard)](../vs140/Wizard-Interface--IDTWizard-.md)  
 Describes the `IDTWizard` interface that wizards must implement to work in the IDE.  
  
 [Context Parameters](../Topic/Context%20Parameters.md)  
 Explains how wizards are implemented and what occurs when the IDE passes Context Parameters to the implementation.  
  
 [Custom Parameters](../Topic/Custom%20Parameters.md)  
 Explains how to use Custom Parameters to control the operation of the wizard after the wizard is started.  
  
## Related Sections  
 [Project Types](../vs140/Project-Types.md)  
 Provides links to additional topics that offer information about how to design new project types.  
  
 [Walkthrough: Creating a Wizard](assetId:///adb41fe9-fcca-4e87-bf4f-bf2fa68e8b06)  
 Illustrates how to create a wizard.  
  
 [Projects and Solutions](../vs140/Extending-Projects.md)  
 Describes how to use [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] projects and solutions to organize code files and resource files, and how to implement source control.