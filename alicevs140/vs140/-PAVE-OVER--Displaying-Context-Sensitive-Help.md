---
title: "&lt;PAVE OVER&gt; Displaying Context-Sensitive Help"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0979c267-3742-4d4a-a658-5185f13976e4
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;PAVE OVER&gt; Displaying Context-Sensitive Help
Context-sensitive help, for the purpose of this discussion, refers to help support for the controls in a dialog box that users access:  
  
-   By pressing the F1 key.  
  
-   By right-clicking a control (What's This? Help).  
  
-   By using the question-mark pointer (the What's This? Help pointer).  
  
 For each control that you want to support context-sensitive help, set the **HelpID** property to **True**.  
  
 If necessary, add htmlhelp.lib to the **Additional Dependencies** property, which is in the **Input** property page of the **Linker** folder in your project's **Property Pages** dialog box.  
  
 The source information for context-sensitive help is stored in a .txt file that you include in your HTML Help project.  
  
### To create the context-sensitive help text file  
  
1.  Use a text editor to create a .txt file.  
  
2.  Format the topics as follows:  
  
     `.topic 1`  
  
     `help text for control 1`  
  
     `.topic 2`  
  
     `help text for control 2`  
  
> [!NOTE]
>  For more information, see "Designing context-sensitive help" in HTML Help's online help. From the **Help** menu (in HTML Help Workshop), choose **Help Topics**.  
  
 After you create the .txt file, add it to the [Files] section in your .hhp file.  
  
 To support help for resources in a dialog box, you must create a two-dimensional array that maps control IDs to help IDs (topic numbers).  
  
#### To create the two-dimensional array  
  
1.  In the .cpp file, for every class that represents a dialog box, add a two-dimensional array to the end of the class. For example:  
  
     [!CODE [NVC_MFCHtmlHelp#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCHtmlHelp#1)]  
  
 Each entry in the two-dimensional array pairs a resource ID for a dialog-box control with a topic number from the context-sensitive help text file. If you do not want a specific resource to have What's This? Help, use –1. The last pair in this array should be 0,0.  
  
 F1 access to context-sensitive help means that users will be able to press F1 when a control has focus to access help.  
  
#### To enable F1 access to context-sensitive help  
  
1.  Implement a handler for the **WM_HELPINFO** message (in each dialog-box class where you want F1 access to context-sensitive help) and implement the following code for the handler:  
  
     [!CODE [NVC_MFCHtmlHelp#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCHtmlHelp#2)]  
  
 What's This? Help displays the control's help when a user right-clicks the control.  
  
#### To implement right-click What's This? Help  
  
1.  Implement a handler (see [Mapping Messages to Functions](../vs140/Mapping-Messages-to-Functions.md)) for the **WM_CONTEXTMENU** message in each dialog-box class where you want What's This? Help (select the ID for the dialog box from the list of Object IDs). Implement the following code for the handler:  
  
     [!CODE [NVC_MFCHtmlHelp#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCHtmlHelp#3)]  
  
 When you specify the .chm file, the expected location is the project's working directory. See the **Debug** tab of the **Property Pages** dialog box for the location of the working directory (by default, the project directory). When you specify the text file in the .chm that contains the context-sensitive help, you must specify the same location information as is specified for the .txt file in the .chm's .hhp file.  
  
 If you already implement F1 access to context-sensitive help, you can easily enable the What's This? pointer, which causes a question mark to appear on the title bar, in the upper right-hand corner of the dialog box.  
  
#### To enable the What's This? Help question-mark pointer  
  
1.  Select the **Context help** check box in the **Extended Styles** tab of the dialog box properties.  
  
## See Also  
 [HTML Help: Context-Sensitive Help for Your Programs](../vs140/HTML-Help--Context-Sensitive-Help-for-Your-Programs.md)