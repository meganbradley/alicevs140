---
title: "Replace Command"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a15767f1-5a3d-44f5-8c77-7b0f1157f340
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Replace Command
Replaces text in files using a subset of the options available on the **Replace in Files** tab of the **Find and Replace** window.  
  
## Syntax  
  
```  
Edit.Replace findwhat replacewith [/all] [/case]  
[/doc|/proc|/open|/sel] [/hidden] [/options] [/reset] [/up]  
[/wild|/regex] [/word]  
```  
  
## Arguments  
 `findwhat`  
 Required. The text to match.  
  
 `replacewith`  
 Required. The text to substitute for the matched text.  
  
## Switches  
 /all or /a  
 Optional. Replaces all occurrences of the search text with the replacement text.  
  
 /case or /c  
 Optional. Matches occur only if when the uppercase and lowercase characters exactly match those specified in the `findwhat` argument.  
  
 /doc or /d  
 Optional. Searches the current document only. Specify only one of the available search scopes, `/doc`, `/proc`, `/open`, or `/sel`.  
  
 /hidden or /h  
 Optional. Searches concealed and collapsed text, such as the metadata of a design-time control, a hidden region of an outlined document, or a collapsed class or method.  
  
 /open or /o  
 Optional. Searches all open documents as if they were one document. Specify only one of the available search scopes, `/doc`, `/proc`, `/open`, or `/sel`.  
  
 /options or /t  
 Optional. Displays a list of the current find option settings and does not perform a search.  
  
 /proc or /p  
 Optional. Searches the current procedure only. Specify only one of the available search scopes, `/doc`, `/proc`, `/open`, or `/sel`.  
  
 /regex or /r  
 Optional. Uses pre-defined special characters in the `findwhat` argument as notations that represent patterns of text rather than the literal characters. For a complete list of regular expression characters, see [Regular Expressions](../vs140/Using-Regular-Expressions-in-Visual-Studio.md).  
  
 /reset or /e  
 Optional. Returns the find options to their default settings and does not perform a search.  
  
 /sel or /s  
 Optional. Searches the current selection only. Specify only one of the available search scopes, `/doc`, `/proc`, `/open`, or `/sel`.  
  
 /up or /u  
 Optional. Searches from the current location in the file toward the top of the file. By default, searches begin at the current location in the file and advance toward the bottom of the file.  
  
 /wild or /l  
 Optional. Uses pre-defined special characters in the `findwhat` argument as notations to represent a character or sequence of characters.  
  
 /word or /w  
 Optional. Searches only for whole words.  
  
## Example  
 This example replaces `btnSend` with `btnSubmit` in all open documents.  
  
```  
>Edit.Replace btnSend btnSubmit /open  
```  
  
## See Also  
 [Finding and Replacing Text](../vs140/Finding-and-Replacing-Text.md)   
 [Command Window](../vs140/Command-Window.md)   
 [Find/Command Box](../vs140/Find-Command-Box.md)   
 [Visual Studio Commands](../vs140/Visual-Studio-Commands.md)   
 [Visual Studio Command Aliases](../vs140/Visual-Studio-Command-Aliases.md)