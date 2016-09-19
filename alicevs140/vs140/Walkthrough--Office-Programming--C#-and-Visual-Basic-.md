---
title: "Walkthrough: Office Programming (C# and Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 519cff31-f80b-4f0e-a56b-26358d0f8c51
caps.latest.revision: 48
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Walkthrough: Office Programming (C# and Visual Basic)
[!INCLUDE[vs_dev10_long](../vs140/includes/vs_dev10_long_md.md)] introduces new features in C# and Visual Basic that improve Microsoft Office programming. Each language has added features that already exist in the other language.  
  
 The new features in C# include named and optional arguments, return values that have type `dynamic`, and, in COM programming, the ability to omit the `ref` keyword and to access indexed properties. The new features in Visual Basic include auto-implemented properties, statements in lambda expressions, and collection initializers.  
  
 Both languages enable embedding of type information, which allows deployment of assemblies that interact with COM components without deploying primary interop assemblies (PIAs) to the user's computer. For more information, see [Walkthrough: Embedding Types from Managed Assemblies](../vs140/Walkthrough--Embedding-Types-from-Managed-Assemblies--C#-and-Visual-Basic-.md).  
  
 This walkthrough demonstrates the new features in the context of Office programming, but many of them are also useful in general programming. In the walkthrough, you will first use an Excel Add-in application to create an Excel workbook. You will then create a Word document that contains a link to the workbook. Finally, you will see how the PIA dependency can be turned on and off.  
  
## Prerequisites  
 You must have Microsoft Office Excel 2013 (or version 2007 or later) and Microsoft Office Word 2013 (or version 2007 or later) installed on your computer to complete this walkthrough.  
  
 If you are using an operating system that is older than [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)], make sure that [!INCLUDE[dnprdnlong](../vs140/includes/dnprdnlong_md.md)] is installed.  
  
 [!INCLUDE[note_settings_general](../vs140/includes/note_settings_general_md.md)]  
  
### To set up an Excel Add-in application  
  
1.  Start Visual Studio.  
  
2.  On the **File** menu, point to **New**, and then click **Project**.  
  
3.  In the **Installed Templates** pane, expand **Visual Basic** or **Visual C#**, expand **Office**, and then click **2013** (or **2010** or **2007**).  
  
4.  In the **Templates** pane, click **Excel 2013 Add-in** (or **Excel 2010 Add-in** or **Excel 2007 Add-in**).  
  
5.  Look at the top of the **Templates** pane to make sure that **.NET Framework 4**, or a later version, appears in the **Target Framework** box.  
  
6.  Type a name for your project in the **Name** box, if you want to.  
  
7.  Click **OK**.  
  
8.  The new project appears in **Solution Explorer**.  
  
### To add references  
  
1.  In **Solution Explorer**, right-click your project's name and then click **Add Reference**. The **Add Reference** dialog box appears.  
  
2.  On the **Assemblies** tab, select **Microsoft.Office.Interop.Excel**, version 15.0.0.0 (or version 14.0.0.0 for Excel 2010 or version 12.0.0.0 for Excel 2007), in the **Component Name** list, and then hold down the CTRL key and select **Microsoft.Office.Interop.Word**, version 15.0.0.0 (or version 14.0.0.0 for Word 2010 or 12.0.0.0 for Word 2007).  If you do not see the assemblies, you may need to ensure they are installed and displayed (see [How to install primary interop assemblies](assetId:///92948fcc-76c6-4b08-ba63-cab59dd60eb1)).  
  
3.  Click **OK**.  
  
### To add necessary Imports statements or using directives  
  
1.  In **Solution Explorer**, right-click the **ThisAddIn.vb** or **ThisAddIn.cs** file and then click **View Code**.  
  
2.  Add the following `Imports` statements (Visual Basic) or `using` directives (C#) to the top of the code file if they are not already present.  
  
     [!CODE [csOfficeWalkthrough#1](../CodeSnippet/VS_Snippets_VBCSharp/csofficewalkthrough#1)]  
  
### To create a list of bank accounts  
  
1.  In **Solution Explorer**, right-click your project's name, click **Add**, and then click **Class**. Name the class Account.vb if you are using Visual Basic or Account.cs if you are using C#. Click **Add**.  
  
2.  Replace the definition of the `Account` class with the following code. The class definitions use *auto-implemented properties*, new to Visual Basic in Visual Studio 2010. For more information, see [Auto-Implemented Properties (Visual Basic)](../vs140/Auto-Implemented-Properties--Visual-Basic-.md).  
  
     [!CODE [csOfficeWalkthrough#2](../CodeSnippet/VS_Snippets_VBCSharp/csofficewalkthrough#2)]  
  
3.  To create a `bankAccounts` list that contains two accounts, add the following code to the `ThisAddIn_Startup` method in ThisAddIn.vb or ThisAddIn.cs. The list declarations use *collection initializers*, new to Visual Basic in Visual Studio 2010. For more information, see [Collection Initializers Overview (Visual Basic)](../Topic/Collection%20Initializers%20\(Visual%20Basic\).md).  
  
     [!CODE [csOfficeWalkthrough#3](../CodeSnippet/VS_Snippets_VBCSharp/csofficewalkthrough#3)]  
  
### To export data to Excel  
  
1.  In the same file, add the following method to the `ThisAddIn` class. The method sets up an Excel workbook and exports data to it.  
  
     [!CODE [csOfficeWalkthrough#4](../CodeSnippet/VS_Snippets_VBCSharp/csofficewalkthrough#4)]  
  
     Two new C# features are used in this method. Both of these features already exist in Visual Basic.  
  
    -   Method [Add](http://go.microsoft.com/fwlink/?LinkId=210910) has an *optional parameter* for specifying a particular template. Optional parameters, new in [!INCLUDE[csharp_dev10_long](../vs140/includes/csharp_dev10_long_md.md)], enable you to omit the argument for that parameter if you want to use the parameter's default value. Because no argument is sent in the previous example, `Add` uses the default template and creates a new workbook. The equivalent statement in earlier versions of C# requires a placeholder argument: `excelApp.Workbooks.Add(Type.Missing)`.  
  
         For more information, see [Named and Optional Arguments (C# Programming Guide)](../Topic/Named%20and%20Optional%20Arguments%20\(C%23%20Programming%20Guide\).md).  
  
    -   The `Range` and `Offset` properties of the [Range](http://go.microsoft.com/fwlink/?LinkId=210911) object use the *indexed properties* feature. This feature enables you to consume these properties from COM types by using the following typical C# syntax. Indexed properties also enable you to use the `Value` property of the `Range` object, eliminating the need to use the `Value2` property. The `Value` property is indexed, but the index is optional. Optional arguments and indexed properties work together in the following example.  
  
         [!CODE [csOfficeWalkthrough#5](../CodeSnippet/VS_Snippets_VBCSharp/csofficewalkthrough#5)]  
  
         In earlier versions of the language, the following special syntax is required.  
  
         [!CODE [csOfficeWalkthrough#6](../CodeSnippet/VS_Snippets_VBCSharp/csofficewalkthrough#6)]  
  
         You cannot create indexed properties of your own. The feature only supports consumption of existing indexed properties.  
  
         For more information, see [How to: Use Indexed Properties in COM Interop Programming (C# Programming Guide)](../vs140/How-to--Use-Indexed-Properties-in-COM-Interop-Programming--C#-Programming-Guide-.md).  
  
2.  Add the following code at the end of `DisplayInExcel` to adjust the column widths to fit the content.  
  
     [!CODE [csOfficeWalkthrough#7](../CodeSnippet/VS_Snippets_VBCSharp/csofficewalkthrough#7)]  
  
     These additions demonstrate another new feature in C# 2010: treating `Object` values returned from COM hosts such as Office as if they have type [dynamic](../vs140/dynamic--C#-Reference-.md). This happens automatically when **Embed Interop Types** is set to its default value, `True`, or, equivalently, when the assembly is referenced by the [/link](../Topic/-link%20\(C%23%20Compiler%20Options\).md) compiler option. Type `dynamic` allows late binding, already available in Visual Basic, and avoids the explicit casting required in Visual C# 2008 and earlier versions of the language.  
  
     For example, `excelApp.Columns[1]` returns an `Object`, and `AutoFit` is an Excel  [Range](http://go.microsoft.com/fwlink/?LinkId=210911) method. Without `dynamic`, you must cast the object returned by `excelApp.Columns[1]` as an instance of `Range` before calling method `AutoFit`.  
  
     [!CODE [csOfficeWalkthrough#8](../CodeSnippet/VS_Snippets_VBCSharp/csofficewalkthrough#8)]  
  
     For more information about embedding interop types, see procedures "To find the PIA reference" and "To restore the PIA dependency" later in this topic. For more information about `dynamic`, see [dynamic (C# Reference)](../vs140/dynamic--C#-Reference-.md) or [Using Type dynamic (C# Programming Guide)](../vs140/Using-Type-dynamic--C#-Programming-Guide-.md).  
  
### To invoke DisplayInExcel  
  
1.  Add the following code at the end of the `ThisAddIn_StartUp` method. The call to `DisplayInExcel` contains two arguments. The first argument is the name of the list of accounts to be processed. The second argument is a multiline lambda expression that defines how the data is to be processed. The `ID` and `balance` values for each account are displayed in adjacent cells, and the row is displayed in red if the balance is less than zero. Multiline lambda expressions are a new feature in Visual Basic 2010. For more information, see [Lambda Expressions](../vs140/Lambda-Expressions--Visual-Basic-.md).  
  
     [!CODE [csOfficeWalkthrough#9](../CodeSnippet/VS_Snippets_VBCSharp/csofficewalkthrough#9)]  
  
2.  To run the program, press F5. An Excel worksheet appears that contains the data from the accounts.  
  
### To add a Word document  
  
1.  Add the following code at the end of the `ThisAddIn_StartUp` method to create a Word document that contains a link to the Excel workbook.  
  
     [!CODE [csOfficeWalkthrough#10](../CodeSnippet/VS_Snippets_VBCSharp/csofficewalkthrough#10)]  
  
     This code demonstrates several of the new features in C#: the ability to omit the `ref` keyword in COM programming, named arguments, and optional arguments. These features already exist in Visual Basic. The  [PasteSpecial](http://go.microsoft.com/fwlink/?LinkId=147099) method has seven parameters, all of which are defined as optional reference parameters. Prior to Visual C# 2010, you had to define object variables to use as arguments for the seven parameters, even when you had no meaningful values to send in. Named and optional arguments enable you to designate the parameters you want to access by name, and to send arguments to only those parameters. In this example, arguments are sent to indicate that a link to the workbook on the Clipboard should be created (parameter `Link`), and that the link is to be displayed in the Word document as an icon (parameter `DisplayAsIcon`). Visual C# 2010 also enables you to omit the `ref` keyword for these arguments. Compare the following code segment from Visual C# 2008 with the single line required in Visual C# 2010:  
  
     [!CODE [csOfficeWalkthrough#11](../CodeSnippet/VS_Snippets_VBCSharp/csofficewalkthrough#11)]  
  
### To run the application  
  
1.  Press F5 to run the application. Excel starts and displays a table that contains the information from the two accounts in `bankAccounts`. Then a Word document appears that contains a link to the Excel table.  
  
### To clean up the completed project  
  
1.  In Visual Studio, click **Clean Solution** on the **Build** menu. Otherwise, the add-in will run every time that you open Excel on your computer.  
  
### To find the PIA reference  
  
1.  Run the application again, but do not click **Clean Solution**.  
  
2.  On the **Start** menu, click **All Programs**. Next click **Microsoft Visual Studio 2013**, then **Visual Studio Tools**, then **Visual Studio Command Prompt (2013)**.  
  
3.  Type `ildasm` in the Visual Studio Command Prompt (2013) window, and then press ENTER. The IL DASM window appears.  
  
4.  On the **File** menu in the IL DASM window, click **Open**. Double-click **Visual Studio 2013**, and then double-click **Projects**. Open the folder for your project, and look in the bin/Debug folder for *your project name*.dll. Double-click *your project name*.dll. A new window displays your project's attributes, in addition to references to other modules and assemblies. Note that namespaces `Microsoft.Office.Interop.Excel` and `Microsoft.Office.Interop.Word` are included in the assembly. By default in Visual Studio 2013, the compiler imports the types you need from a referenced PIA into your assembly.  
  
     For more information, see [How to: View Assembly Contents](assetId:///fb7baaab-4c0d-47ad-8fd3-4591cf834709).  
  
5.  Double-click the **MANIFEST** icon. A window appears that contains a list of assemblies that contain items referenced by the project. `Microsoft.Office.Interop.Excel` and `Microsoft.Office.Interop.Word` are not included in the list. Because the types your project needs have been imported into your assembly, references to a PIA are not required. This makes deployment easier. The PIAs do not have to be present on the user's computer, and because an application does not require deployment of a specific version of a PIA, applications can be designed to work with multiple versions of Office, provided that the necessary APIs exist in all versions.  
  
     Because deployment of PIAs is no longer necessary, you can create an application in advanced scenarios that works with multiple versions of Office, including earlier versions. However, this works only if your code does not use any APIs that are not available in the version of Office you are working with. It is not always clear whether a particular API was available in an earlier version, and for that reason working with earlier versions of Office is not recommended.  
  
    > [!NOTE]
    >  Office did not publish PIAs before Office 2003. Therefore, the only way to generate an interop assembly for Office 2002 or earlier versions is by importing the COM reference.  
  
6.  Close the manifest window and the assembly window.  
  
### To restore the PIA dependency  
  
1.  In **Solution Explorer**, click the **Show All Files** button. Expand the **References** folder and select **Microsoft.Office.Interop.Excel**. Press F4 to display the **Properties** window.  
  
2.  In the **Propertie**s window, change the **Embed Interop Types** property from **True** to **False**.  
  
3.  Repeat steps 1 and 2 in this procedure for `Microsoft.Office.Interop.Word`.  
  
4.  In C#, comment out the two calls to `Autofit` at the end of the `DisplayInExcel` method.  
  
5.  Press F5 to verify that the project still runs correctly.  
  
6.  Repeat steps 1-3 from the previous procedure to open the assembly window. Notice that `Microsoft.Office.Interop.Word` and `Microsoft.Office.Interop.Excel` are no longer in the list of embedded assemblies.  
  
7.  Double-click the **MANIFEST** icon and scroll through the list of referenced assemblies. Both `Microsoft.Office.Interop.Word` and `Microsoft.Office.Interop.Excel` are in the list. Because the application references the Excel and Word PIAs, and the **Embed Interop Types** property is set to **False**, both assemblies must exist on the end user's computer.  
  
8.  In Visual Studio, click **Clean Solution** on the **Build** menu to clean up the completed project.  
  
## See Also  
 [Auto-Implemented Properties (Visual Basic)](../vs140/Auto-Implemented-Properties--Visual-Basic-.md)   
 [Auto-Implemented Properties (C# Programming Guide)](../vs140/Auto-Implemented-Properties--C#-Programming-Guide-.md)   
 [Collection Initializers Overview (Visual Basic)](../Topic/Collection%20Initializers%20\(Visual%20Basic\).md)   
 [Object and Collection Initializers (C# Programming Guide)](../Topic/Object%20and%20Collection%20Initializers%20\(C%23%20Programming%20Guide\).md)   
 [Optional Parameters](../vs140/Optional-Parameters--Visual-Basic-.md)   
 [Passing Arguments by Position and by Name](../vs140/Passing-Arguments-by-Position-and-by-Name--Visual-Basic-.md)   
 [Named and Optional Arguments (C# Programming Guide)](../Topic/Named%20and%20Optional%20Arguments%20\(C%23%20Programming%20Guide\).md)   
 [Early and Late Binding](../vs140/Early-and-Late-Binding--Visual-Basic-.md)   
 [dynamic (C# Reference)](../vs140/dynamic--C#-Reference-.md)   
 [Using Type dynamic (C# Programming Guide)](../vs140/Using-Type-dynamic--C#-Programming-Guide-.md)   
 [Lambda Expressions](../vs140/Lambda-Expressions--Visual-Basic-.md)   
 [Lambda Expressions (C# Programming Guide)](../Topic/Lambda%20Expressions%20\(C%23%20Programming%20Guide\).md)   
 [How to: Use Indexed Properties in COM Interop Programming (C# Programming Guide)](../vs140/How-to--Use-Indexed-Properties-in-COM-Interop-Programming--C#-Programming-Guide-.md)   
 [Walkthrough: Embedding Type Information from Microsoft Office Assemblies (C# and Visual Basic)](../vs140/Walkthrough--Embedding-Type-Information-from-Microsoft-Office-Assemblies--C#-and-Visual-Basic-.md)   
 [Walkthrough: Embedding Types from Managed Assemblies (C# and Visual Basic)](../vs140/Walkthrough--Embedding-Types-from-Managed-Assemblies--C#-and-Visual-Basic-.md)   
 [Walkthrough: Creating Your First Application-Level Add-in for Excel](assetId:///a855e2be-3ecf-4112-a7f5-ec0f7fad3b5f)   
 [COM Interop](../vs140/COM-Interop--Visual-Basic-.md)   
 [Interoperability (C# Programming Guide)](../Topic/Interoperability%20\(C%23%20Programming%20Guide\).md)