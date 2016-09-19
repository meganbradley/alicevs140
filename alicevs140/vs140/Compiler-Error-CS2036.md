---
title: "Compiler Error CS2036"
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
ms.assetid: 44b73be4-b792-4735-bdbd-bd757ab22683
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS2036
The /pdb option requires that the /debug option also be used.  
  
 Program database files are only generated for debug builds. The **/pdb** option is therefore meaningless in a retail build.  
  
### To correct this error  
  
-   Add the **/debug** compiler option.  
  
-   Remove the **/pdb** compiler option.  
  
## Example  
 The following example generates CS2036 when it is compiled with the **/pdb** option but not the /debug option:  
  
```  
// cs2036.cs  
// Compile with: /pdb  
// CS2036  
class Test  
{  
    public static int Main()  
    {  
        return 1;  
    }  
}  
```  
  
## See Also  
 [/pdb (Specify Debug Symbol File) (C# Compiler Options)](../vs140/-pdb--C#-Compiler-Options-.md)   
 [/debug (Emit Debugging Information) (C# Compiler Options)](../Topic/-debug%20\(C%23%20Compiler%20Options\).md)