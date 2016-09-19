---
title: "Walkthrough: Manipulating Files by Using .NET Framework Methods (Visual Basic)"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7d2109eb-f98a-4389-b43d-30f384aaa7d5
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Walkthrough: Manipulating Files by Using .NET Framework Methods (Visual Basic)
This walkthrough demonstrates how to open and read a file using the <xref:System.IO.StreamReader?qualifyHint=False> class, check to see if a file is being accessed, search for a string within a file read with an instance of the <xref:System.IO.StreamReader?qualifyHint=False> class, and write to a file using the <xref:System.IO.StreamWriter?qualifyHint=False> class.  
  
 [!INCLUDE[note_settings_general](../vs140/includes/note_settings_general_md.md)]  
  
## Creating the Application  
 Start [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] and begin the project by creating a form that the user can use to write to the designated file.  
  
#### To create the project  
  
1.  On the **File** menu, select **New Project**.  
  
2.  In the **New Project** pane, click **Windows Application**.  
  
3.  In the **Name** box type `MyDiary` and click **OK**.  
  
     [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] adds the project to **Solution Explorer**, and the **Windows Forms Designer** opens.  
  
4.  Add the controls in the following table to the form and set the corresponding values for their properties.  
  
||||  
|-|-|-|  
|**Object**|**Properties**|**Value**|  
|<xref:System.Windows.Forms.Button?qualifyHint=False>|**Name**<br /><br /> **Text**|`Submit`<br /><br /> **Submit Entry**|  
|<xref:System.Windows.Forms.Button?qualifyHint=False>|**Name**<br /><br /> **Text**|`Clear`<br /><br /> **Clear Entry**|  
|<xref:System.Windows.Forms.TextBox?qualifyHint=False>|**Name**<br /><br /> **Text**<br /><br /> **Multiline**|`Entry`<br /><br /> **Please enter something.**<br /><br /> `False`|  
  
## Writing to the File  
 To add the ability to write to a file via the application, use the <xref:System.IO.StreamWriter?qualifyHint=False> class. <xref:System.IO.StreamWriter?qualifyHint=False> is designed for character output in a particular encoding, whereas the <xref:System.IO.Stream?qualifyHint=False> class is designed for byte input and output. Use <xref:System.IO.StreamWriter?qualifyHint=False> for writing lines of information to a standard text file. For more information on the <xref:System.IO.StreamWriter?qualifyHint=False> class, see <xref:System.IO.StreamWriter?qualifyHint=False>.  
  
#### To add writing functionality  
  
1.  From the **View** menu, choose **Code** to open the Code Editor.  
  
2.  Because the application references the <xref:System.IO?qualifyHint=False> namespace, add the following statements at the very beginning of your code, before the class declaration for the form, which begins `Public Class Form1`.  
  
     [!CODE [VbVbcnMyFileSystem#35](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMyFileSystem#35)]  
  
     Before writing to the file, you must create an instance of a <xref:System.IO.StreamWriter?qualifyHint=False> class.  
  
3.  From the **View** menu, choose **Designer** to return to the **Windows Forms Designer**. Double-click the `Submit` button to create a <xref:System.Windows.Forms.Control.Click?qualifyHint=False> event handler for the button, and then add the following code.  
  
     [!CODE [VbVbcnMyFileSystem#36](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMyFileSystem#36)]  
  
> [!NOTE]
>  The Visual Studio Integrated Development Environment (IDE) will return to the Code Editor and position the insertion point within the event handler where you should add the code.  
  
1.  To write to the file, use the <xref:System.IO.StreamWriter.Write?qualifyHint=False> method of the <xref:System.IO.StreamWriter?qualifyHint=False> class. Add the following code directly after `Dim fw As StreamWriter`. You do not need to worry that an exception will be thrown if the file is not found, because it will be created if it does not already exist.  
  
     [!CODE [VbVbcnMyFileSystem#37](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMyFileSystem#37)]  
  
2.  Make sure that the user cannot submit a blank entry by adding the following code directly after `Dim ReadString As String`.  
  
     [!CODE [VbVbcnMyFileSystem#38](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMyFileSystem#38)]  
  
3.  Because this is a diary, the user will want to assign a date to each entry. Insert the following code after `fw = New StreamWriter("C:\MyDiary.txt", True)` to set the variable `Today` to the current date.  
  
     [!CODE [VbVbcnMyFileSystem#39](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMyFileSystem#39)]  
  
4.  Finally, attach code to clear the <xref:System.Windows.Forms.TextBox?qualifyHint=False>. Add the following code to the `Clear` button's <xref:System.Windows.Forms.Control.Click?qualifyHint=False> event.  
  
     [!CODE [VbVbcnMyFileSystem#40](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMyFileSystem#40)]  
  
## Adding Display Features to the Diary  
 In this section, you add a feature that displays the latest entry in the `DisplayEntry`<xref:System.Windows.Forms.TextBox?qualifyHint=False>. You can also add a <xref:System.Windows.Forms.ComboBox?qualifyHint=False> that displays various entries and from which a user can select an entry to display in the `DisplayEntry`<xref:System.Windows.Forms.TextBox?qualifyHint=False>. An instance of the <xref:System.IO.StreamReader?qualifyHint=False> class reads from `MyDiary.txt`. Like the <xref:System.IO.StreamWriter?qualifyHint=False> class, <xref:System.IO.StreamReader?qualifyHint=False> is intended for use with text files.  
  
 For this section of the walkthrough, add the controls in the following table to the form and set the corresponding values for their properties.  
  
|Control|Properties|Values|  
|-------------|----------------|------------|  
|<xref:System.Windows.Forms.TextBox?qualifyHint=False>|**Name**<br /><br /> **Visible**<br /><br /> **Size**<br /><br /> **Multiline**|`DisplayEntry`<br /><br /> `False`<br /><br /> `120,60`<br /><br /> `True`|  
|<xref:System.Windows.Forms.Button?qualifyHint=False>|**Name**<br /><br /> **Text**|`Display`<br /><br /> **Display**|  
|<xref:System.Windows.Forms.Button?qualifyHint=False>|**Name**<br /><br /> **Text**|`GetEntries`<br /><br /> **Get Entries**|  
|<xref:System.Windows.Forms.ComboBox?qualifyHint=False>|**Name**<br /><br /> **Text**<br /><br /> **Enabled**|`PickEntries`<br /><br /> **Select an Entry**<br /><br /> `False`|  
  
#### To populate the combo box  
  
1.  The `PickEntries`<xref:System.Windows.Forms.ComboBox?qualifyHint=False> is used to display the dates on which a user submits each entry, so the user can select an entry from a specific date. Create a <xref:System.Windows.Forms.Control.Click?qualifyHint=False> event handler to the `GetEntries` button and add the following code.  
  
     [!CODE [VbVbcnMyFileSystem#41](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMyFileSystem#41)]  
  
2.  To test your code, press F5 to compile the application, and then click **Get Entries**. Click the drop-down arrow in the <xref:System.Windows.Forms.ComboBox?qualifyHint=False> to display the entry dates.  
  
#### To choose and display individual entries  
  
1.  Create a <xref:System.Windows.Forms.Control.Click?qualifyHint=False> event handler for the `Display` button and add the following code.  
  
     [!CODE [VbVbcnMyFileSystem#42](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMyFileSystem#42)]  
  
2.  To test your code, press F5 to compile the application, and then submit an entry. Click **Get Entries**, select an entry from the <xref:System.Windows.Forms.ComboBox?qualifyHint=False>, and then click **Display**. The contents of the selected entry appear in the `DisplayEntry`<xref:System.Windows.Forms.TextBox?qualifyHint=False>.  
  
## Enabling Users to Delete or Modify Entries  
 Finally, you can include additional functionality enables users to delete or modify an entry by using `DeleteEntry` and `EditEntry` buttons. Both buttons remain disabled unless an entry is displayed.  
  
 Add the controls in the following table to the form and set the corresponding values for their properties.  
  
|Control|Properties|Values|  
|-------------|----------------|------------|  
|<xref:System.Windows.Forms.Button?qualifyHint=False>|**Name**<br /><br /> **Text**<br /><br /> **Enabled**|`DeleteEntry`<br /><br /> **Delete Entry**<br /><br /> `False`|  
|<xref:System.Windows.Forms.Button?qualifyHint=False>|**Name**<br /><br /> **Text**<br /><br /> **Enabled**|`EditEntry`<br /><br /> **Edit Entry**<br /><br /> `False`|  
|<xref:System.Windows.Forms.Button?qualifyHint=False>|**Name**<br /><br /> **Text**<br /><br /> **Enabled**|`SubmitEdit`<br /><br /> **Submit Edit**<br /><br /> `False`|  
  
#### To enable deletion and modification of entries  
  
1.  Add the following code to the `Display` button's <xref:System.Windows.Forms.Control.Click?qualifyHint=False> event, after `DisplayEntry.Text = ReadString`.  
  
     [!CODE [VbVbcnMyFileSystem#43](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMyFileSystem#43)]  
  
2.  Create a <xref:System.Windows.Forms.Control.Click?qualifyHint=False> event handler for the `DeleteEntry` button and add the following code.  
  
     [!CODE [VbVbcnMyFileSystem#44](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMyFileSystem#44)]  
  
3.  When a user displays an entry, the `EditEntry` button becomes enabled. Add the following code to the <xref:System.Windows.Forms.Control.Click?qualifyHint=False> event of the `Display` button after `DisplayEntry.Text = ReadString`.  
  
     [!CODE [VbVbcnMyFileSystem#45](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMyFileSystem#45)]  
  
4.  Create a <xref:System.Windows.Forms.Control.Click?qualifyHint=False> event handler for the `EditEntry` button and add the following code.  
  
     [!CODE [VbVbcnMyFileSystem#46](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMyFileSystem#46)]  
  
5.  Create a <xref:System.Windows.Forms.Control.Click?qualifyHint=False> event handler for the `SubmitEdit` button and add the following code  
  
     [!CODE [VbVbcnMyFileSystem#47](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMyFileSystem#47)]  
  
 To test your code, press F5 to compile the application. Click **Get Entries**, select an entry, and then click **Display**. The entry appears in the `DisplayEntry`<xref:System.Windows.Forms.TextBox?qualifyHint=False>. Click **Edit Entry**. The entry appears in the `Entry`<xref:System.Windows.Forms.TextBox?qualifyHint=False>. Edit the entry in the `Entry`<xref:System.Windows.Forms.TextBox?qualifyHint=False> and click **Submit Edit**. Open the `MyDiary.txt` file to confirm your correction. Now select an entry and click **Delete Entry**. When the <xref:System.Windows.Forms.MessageBox?qualifyHint=False> requests confirmation, click **OK**. Close the application and open `MyDiary.txt` to confirm the deletion.  
  
## See Also  
 <xref:System.IO.StreamReader?qualifyHint=False>   
 <xref:System.IO.StreamWriter?qualifyHint=False>   
 [Walkthroughs](../Topic/Visual%20Basic%20Language%20Walkthroughs.md)