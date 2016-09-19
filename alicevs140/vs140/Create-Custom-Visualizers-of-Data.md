---
title: "Create Custom Visualizers of Data"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
  - JScript
  - VB
  - CSharp
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c24c006f-f2ac-429f-89db-677fc0c6e1ea
caps.latest.revision: 30
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Create Custom Visualizers of Data
Visualizers are components of the [!INCLUDE[vs_current_short](../vs140/includes/vs_current_short_md.md)] debugger user interface. A *visualizer* creates a dialog box or another interface to display a variable or object in a manner that is appropriate to its data type. For example, an HTML visualizer interprets an HTML string and displays the result as it would appear in a browser window; a bitmap visualizer interprets a bitmap structure and displays the graphic it represents. Some visualizers enable you to modify as well as view the data.  
  
 The [!INCLUDE[vs_current_short](../vs140/includes/vs_current_short_md.md)] debugger includes six standard visualizers. These are the text, HTML, XML, and JSON visualizers, all of which work on string objects; the WPF Tree visualizer, for displaying the properties of a WPF object visual tree; and the dataset visualizer, which works for DataSet, DataView, and DataTable objects. Additional visualizers may be available for download from Microsoft Corporation in the future, and are available from third-parties and the community. In addition, you can write your own visualizers and install them in the [!INCLUDE[vs_current_short](../vs140/includes/vs_current_short_md.md)] debugger.  
  
> [!NOTE]
>  In **Store** apps, only the standard text, HTML, XML, and JSON visualizers are supported. Custom (user-created) visualizers are not supported.  
  
 Visualizers are represented in the debugger by a magnifying glass icon. When you see the magnifying glass icon in a **DataTip**, in a debugger variables window, or in the **QuickWatch** dialog box, you can click the magnifying glass to select a visualizer appropriate to the data type of the corresponding object.  
  
 Visualizers are not supported on the Compact Framework.  
  
> [!NOTE]
>  Debugger visualizers require greater privileges than are allowed by a partial trust application. As a result, visualizers do not load when you are stopped in code with partial trust. To debug using a visualizer, you must run the code with full trust.  
  
## In This Section  
 [How to: Write a Visualizer](../Topic/How%20to:%20Write%20a%20Visualizer.md)  
  
 [Walkthrough: Writing a Visualizer](../vs140/Walkthrough--Writing-a-Visualizer-in-C#.md)  
  
 [How to: Install a Visualizer](../vs140/How-to--Install-a-Visualizer.md)  
  
 [How to: Test and Debug a Visualizer](../Topic/How%20to:%20Test%20and%20Debug%20a%20Visualizer.md)  
  
 [Visualizer API Reference](../Topic/Visualizer%20API%20Reference.md)  
  
## Related Sections  
 [Viewing Data in the Debugger](../vs140/Viewing-Data-in-the-Debugger.md)