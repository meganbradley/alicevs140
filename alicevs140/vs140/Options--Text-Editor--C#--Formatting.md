---
title: "Options, Text Editor, C#, Formatting"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5a7bb668-1d0c-4ffe-9508-24592813162e
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Options, Text Editor, C#, Formatting
Use the **Formatting** property page dialog box to set options for formatting code in the Code Editor. To access this dialog box, click **Options** on the **Tools** menu, expand **Text Editor**, expand **C#**, and then click **Formatting**.  
  
> [!NOTE]
>  The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition. To change your settings, choose **Import and Export Settings** on the **Tools** menu. For more information, see [Customizing Development Settings in Visual Studio](assetId:///22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
## General Settings  
 The general settings affect how the Code Editor applies formatting options to code.  
  
## UIElement List  
  
|Label|Description|  
|-----------|-----------------|  
|**Automatically format completed statement on ;**|When selected, formats statements at completion according to the formatting options selected for the Code Editor. Clear this box if you do not want the Code Editor to alter statements.|  
|**Automatically format completed block on }**|When selected, formats code blocks according to the formatting options selected for the Code Editor as soon as you complete the code block. Clear this box if you do not want the Code Editor to alter blocks.|  
|**Adjust indentation on paste**|When selected, formats text pasted into the Code Editor to fit the formatting options selected for the Code Editor. Clear this box if you do not want pasted text to be altered.|  
  
## Preview Window  
 The **Indentation**, **New Lines**, **Spacing**, and **Wrapping** options panes each display a preview window. The preview window shows the effect of each option. To use the preview window, select a formatting option. The preview window shows an example of the selected option. When you change the setting, for example, when you select or clear a check box, the preview window updates to show the effect of the new setting.  
  
## Remarks  
 Indentation options on the **Tabs** pages for each language only determine where the Code Editor places the cursor when you press ENTER at the end of a line. Indentation options under **Formatting** apply when code is formatted automatically, for example, when you paste code into the file while **Adjust indentation on paste** is selected, and when the block being formatted is typed manually.  
  
## See Also  
 [General, Environment, Options Dialog Box](../vs140/General--Environment--Options-Dialog-Box.md)