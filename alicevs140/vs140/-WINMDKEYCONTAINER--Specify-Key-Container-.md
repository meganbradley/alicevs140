---
title: "-WINMDKEYCONTAINER (Specify Key Container)"
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
H1: /WINMDKEYCONTAINER (Specify Key Container)
ms.assetid: c2fc44dc-7cb5-42b9-897f-1b124928f2f7
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -WINMDKEYCONTAINER (Specify Key Container)
Specifies a key container to sign a Windows Metadata (.winmd) file.  
  
```  
/WINMDKEYCONTAINER:name  
```  
  
## Remarks  
 Resembles the [/KEYCONTAINER](../vs140/-KEYCONTAINER--Specify-a-Key-Container-to-Sign-an-Assembly-.md) linker option that is applied to a (.winmd) file.  
  
### To set this linker option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [Working with Project Properties](../vs140/Working-with-Project-Properties.md).  
  
2.  Select the **Linker** folder.  
  
3.  Select the **Windows Metadata** property page.  
  
4.  In the **Windows Metadata Key Container** box, enter the location.  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)   
 [Linker Options](../Topic/Linker%20Options.md)