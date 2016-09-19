---
title: "-WINMDDELAYSIGN (Partially Sign a winmd)"
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
H1: /WINMDDELAYSIGN (Partially Sign a winmd)
ms.assetid: 445cd602-62cb-400a-8e3a-4beb6572724d
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -WINMDDELAYSIGN (Partially Sign a winmd)
Enables partial signing of a Windows Runtime Metadata (.winmd) file by putting the public key in the file.  
  
```  
/WINMDDELAYSIGN[:NO]  
```  
  
## Remarks  
 Resembles the [/DELAYSIGN](../Topic/-DELAYSIGN%20\(Partially%20Sign%20an%20Assembly\).md) linker option that is applied to the .winmd file. Use **/WINMDDELAYSIGN** if you want to put only the public key in the .winmd file. By default, the linker acts as if **/WINMDDELAYSIGN:NO** were specified; that is, it does not sign the winmd file.  
  
### To set this linker option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [Working with Project Properties](../vs140/Working-with-Project-Properties.md).  
  
2.  Select the **Linker** folder.  
  
3.  Select the **Windows Metadata** property page.  
  
4.  In the **Windows Metadata Delay Sign** drop-down list box, select the option you want.  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)   
 [Linker Options](../Topic/Linker%20Options.md)