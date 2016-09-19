---
title: "How to: Define Keywords in Visual C++"
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
ms.assetid: 2dfcf343-e861-4bde-b5a4-7deb6773d9c8
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Define Keywords in Visual C++
Keywords are predefined, reserved identifiers that have special meanings. They cannot be used as identifiers in a program. However, you can define your own keywords to use in Visual C++, and you can assign customized syntax coloring to the keywords. Syntax coloring gives you visual cues about the structure and state of your code.  
  
### To define your own Visual C++ keywords  
  
1.  Use the Visual Studio [Code and Text Editor](assetId:///508e1f18-99d5-48ad-b5ad-d011b21c6ab1) or Notepad.exe to create a text-only file named `usertype.dat`.  
  
2.  In `usertype.dat`, type each user-defined keyword on a separate line.  
  
3.  Save `usertype.dat`in the directory that contains devenv.exe. By default, the path of that directory is *<drive\>*:\Program Files\\[!INCLUDE[TLA#tla_visualstu](../vs140/includes/TLA#tla_visualstu_md.md)] *<major.minor version number>*\Common7\\[!INCLUDE[TLA2#tla_ide](../vs140/includes/TLA2#tla_ide_md.md)]. Because that directory is read-only by default, you need administrative credentials to save `usertype.dat`.  
  
4.  Exit Visual Studio, and then restart it.  
  
    > [!NOTE]
    >  You cannot rename or reload the `usertype.dat` file during an editing session because it is read during initialization. All previously defined color settings take precedence because the syntax coloring mechanism checks the `usertype.dat` file last.  
  
5.  On the **Tools** menu, click **Options**. In the **Options** dialog box, click **Environment**, then click **Fonts and Colors**, and then in the **Display items:** list, click **C/C++ User Keywords**.  
  
6.  Set the font and color properties of your user-defined keywords as described in [Fonts and Colors, Environment, Options Dialog Box](../vs140/Fonts-and-Colors--Environment--Options-Dialog-Box.md).  
  
 For more information, see [Keywords](../vs140/Keywords--C---.md).  
  
## See Also  
 [Running as a Member of the Users Group](../vs140/Running-as-a-Member-of-the-Users-Group.md)   
 [Default Keyboard Shortcuts](../vs140/Default-Keyboard-Shortcuts-in-Visual-Studio.md)