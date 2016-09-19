---
title: "Find in Files Command"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2fc78bfe-b339-4599-97f9-4cafd8a194d9
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Find in Files Command
Search files using a subset of the options available on the **Find in Files** tab of the **Find and Replace** window.  
  
## Syntax  
  
```  
Edit.FindinFiles findwhat [/case] [/ext:extensions]  
[/lookin:searchpath] [/names] [/options] [/reset] [/stop] [/sub]  
[/text2] [/wild|/regex] [/word]  
```  
  
## Arguments  
 `findwhat`  
 Required. The text to match.  
  
## Switches  
 /case or /c  
 Optional. Matches occur only if the uppercase and lowercase characters exactly match those specified in the `findwhat` argument.  
  
 /ext: `extensions`  
 Optional. Specifies the file extensions for the files to be searched. If not specified, the previous extension is used if one was previously entered.  
  
 /lookin: `searchpath`  
 Optional. Directory to search. If the path contains spaces, enclose the entire path in quotation marks.  
  
 /names or /n  
 Optional. Displays a list of file names that contain matches.  
  
 /options or /t  
 Optional. Displays a list of the current find option settings and does not perform a search.  
  
 /regex or /r  
 Optional. Uses pre-defined special characters in the `findwhat` argument as notations that represent patterns of text rather than the literal characters. For a complete list of regular expression characters, see [Regular Expressions](../vs140/Using-Regular-Expressions-in-Visual-Studio.md).  
  
 /reset or /e  
 Optional. Returns the find options to their default settings and does not perform a search.  
  
 /stop  
 Optional. Halts the current search operation if one is in progress. Search ignores all other arguments when `/stop` has been specified. For example, to stop the current search you would enter the following:  
  
```  
>Edit.FindinFiles /stop  
```  
  
 /sub or /s  
 Optional. Searches the subfolders within the directory specified in the /lookin:`searchpath` argument.  
  
 /text2 or /2  
 Optional. Displays the results of the search in the Find Results 2 window.  
  
 /wild or /l  
 Optional. Uses pre-defined special characters in the `findwhat` argument as notations to represent a character or sequence of characters.  
  
 /word or /w  
 Optional. Searches only for whole words.  
  
## Example  
 This example searches for btnCancel in all .cls files located in the folder "My Visual Studio Projects" and displays the match information in the Find Results 2 Window.  
  
```  
>Edit.FindinFiles btnCancel /lookin:"c:/My Visual Studio Projects" /ext:*.cls /text2  
```  
  
## See Also  
 [Find in Files Tab, Find and Replace Window](../vs140/Find-in-Files.md)   
 [Command Window](../vs140/Command-Window.md)   
 [Find/Command Box](../vs140/Find-Command-Box.md)   
 [Visual Studio Commands](../vs140/Visual-Studio-Commands.md)   
 [Visual Studio Command Aliases](../vs140/Visual-Studio-Command-Aliases.md)