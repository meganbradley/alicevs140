---
title: "Compiler Error CS1569"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1d5e89d6-0a05-4e4f-b472-9089146696bb
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1569
Error generating XML documentation file 'Filename' ('reason')  
  
 When attempting to write the XML documentation to the file named in the message, an error occurred for the reason specified. The reason may be something like "network drive not found," or "access denied." Often, the reason will suggest what needs to be done to correct the error. For example, if the error says "access denied," you would verify that you have write permission on the file.  
  
## Example  
  
```  
// 1569a.cs  
// compile with: /doc:CS1569.xml  
// post-build command: attrib +r CS1569.xml  
class Test  
{  
   /// <summary>Test.</summary>  
   public static void Main() {}  
}  
```  
  
## Example  
 The previous sample generated an .xml file that was then set to read only. This sample attempts to write to the same file. The following sample generates CS1569.  
  
```  
// CS1569.cs  
// compile with: /doc:CS1569.xml  
// CS1569 expected  
class Test  
{  
   /// <summary>Test.</summary>  
   public static void Main() {}  
}  
  
```