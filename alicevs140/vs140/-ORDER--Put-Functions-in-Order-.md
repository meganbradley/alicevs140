---
title: "-ORDER (Put Functions in Order)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
H1: /ORDER (Put Functions in Order)
ms.assetid: ecf5eb3e-e404-4e86-9a91-4e5ec157261a
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -ORDER (Put Functions in Order)
```  
/ORDER:@filename  
```  
  
## Parameters  
 *filename*  
 A text file specifying the linking order for COMDAT functions.  
  
## Remarks  
 The /ORDER option tells LINK to optimize your program by placing certain COMDATs into the image in a predetermined order. LINK places the functions in the specified order within each section in the image.  
  
 Specify the order in *filename*, which is a text file (response file) that lists the COMDATs in the order you want to link them. Each line in *filename* contains the name of one COMDAT. An object contains COMDATs if it has been compiled with the /Gy option. Function names are case sensitive.  
  
 LINK uses decorated forms of identifiers. The compiler decorates an identifier when it creates the .obj file. Use the [DUMPBIN](../vs140/DUMPBIN-Reference.md) tool to get the decorated form of an identifier when you need to specify it to the linker. For more information on decorated names, see [Decorated Names](../vs140/Decorated-Names.md).  
  
 If more than one /ORDER specification is used, the last one specified takes effect.  
  
 Ordering allows you to optimize your program's paging behavior through swap tuning by grouping a function with the functions it calls. You can also group frequently called functions together. These techniques increase the probability that a called function is in memory when it is needed and will not have to be paged from disk.  
  
 The linker will prepend an underscore (_) to every decorated name in *filename* unless the name starts with a question mark (?) or at sign (@). For example, if an object file contains `extern "C" int func(int)` and `int main(void)`, DUMPBIN [/SYMBOLS](../vs140/-SYMBOLS.md) will list these decorated names:  
  
```  
009 00000000 SECT3  notype ()    External     | _func  
00A 00000008 SECT3  notype ()    External     | _main  
```  
  
 However, the name specified in the order file should be `func` and `main`.  
  
 The /ORDER option disables incremental linking.  
  
> [!NOTE]
>  LINK cannot order static functions because static function names are not public symbol names. When /ORDER is specified, linker warning LNK4037 is generated for each symbol, in the order file, that is either static or not found.  
  
### To set this linker option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [Setting Visual C++ Project Properties](../vs140/Working-with-Project-Properties.md).  
  
2.  Click the **Linker** folder.  
  
3.  Click the **Optimization** property page.  
  
4.  Modify the **Function Order** property.  
  
### To set this linker option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.FunctionOrder?qualifyHint=False>.  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)   
 [Linker Options](../Topic/Linker%20Options.md)