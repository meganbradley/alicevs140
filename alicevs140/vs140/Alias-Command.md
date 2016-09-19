---
title: "Alias Command"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bdf857df-b5d5-450f-8c10-a6fd4dccc130
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Alias Command
Creates a new alias for a complete command, complete command and arguments, or another alias.  
  
> [!TIP]
>  Typing `>alias` without any arguments displays the current list of aliases and their definitions.  
  
## Syntax  
  
```  
Tools.Alias [/delete] [/reset] [aliasname] [aliasstring]  
```  
  
## Arguments  
 `aliasname`  
 Optional. The name for the new alias. If no value is supplied for `aliasname`, a list of the current aliases and their definitions appears.  
  
 `aliasstring`  
 Optional. The complete command name or existing alias and any parameters that you want to create as an alias. If no value is supplied for `aliasstring`, the alias name and alias string for the specified alias displays.  
  
## Switches  
 /delete or /del or /d  
 Optional. Deletes the specified alias, removing it from autocompletion.  
  
 /reset  
 Optional. Resets the list of pre-defined aliases to its original settings. That is, it restores all pre-defined aliases and removes all user-defined aliases.  
  
## Remarks  
 Since aliases represent commands, they must be located at the beginning of the command line.  
  
 When issuing this command, you should include the switches immediately after the command, not after the aliases, otherwise the switch itself will be included as part of the alias string.  
  
 The `/reset` switch asks for a confirmation before the aliases are restored. There is no short form of `/reset`.  
  
## Examples  
 This example creates a new alias, `upper`, for the complete command Edit.MakeUpperCase.  
  
```  
>Tools.Alias upper Edit.MakeUpperCase  
```  
  
 This example deletes the alias, `upper`.  
  
```  
>Tools.alias /delete upper  
```  
  
 This example displays a list of all current aliases and definitions.  
  
```  
>Tools.Alias  
```  
  
## See Also  
 [Visual Studio Commands](../vs140/Visual-Studio-Commands.md)   
 [Command Window](../vs140/Command-Window.md)   
 [Find/Command Box](../vs140/Find-Command-Box.md)   
 [Visual Studio Command Aliases](../vs140/Visual-Studio-Command-Aliases.md)