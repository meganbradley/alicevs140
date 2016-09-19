---
title: "Find in Files"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 989e0737-46d7-4474-8453-fad52a74669d
caps.latest.revision: 43
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Find in Files
**Find in Files** allows you to search a specified set of files. The matches found and actions taken are listed in the **Find Results** window selected in **Result options**.  
  
 You can use any of the following methods to display **Find in Files** in the **Find and Replace** window.  
  
### To display Find in Files  
  
1.  On the menu bar, choose **Edit**, **Find and Replace**.  
  
2.  Choose **Find in Files**.  
  
 To cancel a Find operation, press CTRL + BREAK.  
  
> [!NOTE]
>  The Find and Replace tool does not search directories with the `Hidden` or `System` attribute set.  
  
## Find what  
 To search for a new text string or expression, specify it in the box. To search for any of the 20 strings that you searched for most recently, open the list, and choose the string for which you want to search. Choose the adjacent **Expression Builder** button if you want to use one or more regular expressions in your search string. For more information, see [Using Regular Expressions in Visual Studio](../vs140/Using-Regular-Expressions-in-Visual-Studio.md).  
  
## Look in  
 The option chosen from the **Look in** drop-down list determines whether **Find in Files** searches only in currently active files or in all files stored within certain folders. Select a search scope from the list or click the **Browse (...)** button to display the **Choose Search Folders** dialog box and to enter your own set of directories. You can also type a path directly into the **Look in** box.  
  
> [!WARNING]
>  With the **Entire Solution** or **Current Project** options, project and solution files are not searched. If you want to look in project files, choose a search folder.  
  
> [!NOTE]
>  If the **Look in** option selected causes you to search a file that you have checked out from source code control, only the version of that file which has been downloaded to your local machine is searched.  
  
## Include subfolders  
 Specifies that subfolders of the **Look in** folder will be searched.  
  
## Find options  
 You can expand or collapse the **Find options** section. The following options can be selected or cleared:  
  
 Match case  
 When selected, a **Find Results** search will be case-sensitive  
  
 Match whole word  
 When selected, the **Find Results** windows will only return whole word matches.  
  
 Use Regular Expressions  
 If this check box is selected, you can use special notations to define patterns of text to match in the **Find what** or **Replace with** text boxes. For a list of these notations, see [Using Regular Expressions in Visual Studio](../vs140/Using-Regular-Expressions-in-Visual-Studio.md).  
  
 Look at these file types  
 This list indicates the types of files to search through in the **Look in** directories. If this field is blank, all of the files in the **Look in** directories will be searched.  
  
 Select any item in the list to enter a preconfigured search string that will find files of those particular types.  
  
## Result options  
 You can expand or collapse the **Result options** section. The following options can be selected or cleared:  
  
 Find results 1 window  
 When selected, the results of the current search will replace the content of the **Find Results 1** window. This window opens automatically to display your search results. To open this window manually, select **Other Windows** from the **View** menu and choose **Find Results 1**.  
  
 Find results 2 window  
 When selected, the results of the current search will replace the content of the **Find Results 2** window. This window opens automatically to display your search results. To open this window manually, select **Other Windows** from the **View** menu and choose **Find Results 2**.  
  
 Display file names only  
 Displays a list of files containing search matches rather than displaying the search matches themselves.  
  
 Append results  
 Appends the results from the search to the previous search results.  
  
## See Also  
 [Findng and Replacing Text](../vs140/Finding-and-Replacing-Text.md)   
 [Replace in Files Tab, Find and Replace Window](../vs140/Replace-in-Files.md)   
 [Visual Studio Commands with Arguments](../vs140/Visual-Studio-Commands.md)