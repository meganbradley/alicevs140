---
title: "How to: Determine If a File Is an Assembly (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: de26f410-9bd1-4b55-a343-cc82f81684be
caps.latest.revision: 8
---
# How to: Determine If a File Is an Assembly (Visual Basic)
A file is an assembly if and only if it is managed, and contains an assembly entry in its metadata. For more information on assemblies and metadata, see the topic [Assembly Manifest](assetId:///8e40fab9-549d-4731-aec2-ffa47a382de0).  
  
### How to manually determine if a file is an assembly  
  
1.  Start the [MSIL Disassembler (Ildasm.exe)](assetId:///db27f6b2-f1ec-499e-be3a-7eecf95ca42b).  
  
2.  Load the file you wish to test.  
  
3.  If **ILDASM** reports that the file is not a portable executable (PE) file, then it is not an assembly. For more information, see the topic [How to: View Assembly Contents](assetId:///fb7baaab-4c0d-47ad-8fd3-4591cf834709).  
  
### How to programmatically determine if a file is an assembly  
  
1.  Call the <xref:System.Reflection.AssemblyName.GetAssemblyName?qualifyHint=False> method, passing the full file path and name of the file you are testing.  
  
2.  If a <xref:System.BadImageFormatException?qualifyHint=False> exception is thrown, the file is not an assembly.  
  
## Example  
 This example tests a DLL to see if it is an assembly.  
  
```  
Module Module1  
    Sub Main()  
        Try  
            Dim testAssembly As Reflection.AssemblyName =  
                                Reflection.AssemblyName.GetAssemblyName("C:\Windows\Microsoft.NET\Framework\v3.5\System.Net.dll")  
            Console.WriteLine("Yes, the file is an Assembly.")  
        Catch ex As System.IO.FileNotFoundException  
            Console.WriteLine("The file cannot be found.")  
        Catch ex As System.BadImageFormatException  
            Console.WriteLine("The file is not an Assembly.")  
        Catch ex As System.IO.FileLoadException  
            Console.WriteLine("The Assembly has already been loaded.")  
        End Try  
        Console.ReadLine()  
    End Sub  
End Module  
' Output (with .NET Framework 3.5 installed):  
'        Yes, the file is an Assembly.  
```  
  
 The <xref:System.Reflection.AssemblyName.GetAssemblyName?qualifyHint=False> method loads the test file, and then releases it once the information is read.  
  
## See Also  
 <xref:System.Reflection.AssemblyName?qualifyHint=False>   
 [Visual Basic Programming Guide](../vs140/Visual-Basic-Programming-Guide.md)   
 [Assemblies and the Global Assembly Cache (Visual Basic)](../vs140/Assemblies-and-the-Global-Assembly-Cache--Visual-Basic-.md)