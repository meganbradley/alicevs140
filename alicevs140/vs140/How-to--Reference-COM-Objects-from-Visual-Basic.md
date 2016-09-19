---
title: "How to: Reference COM Objects from Visual Basic"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9c518fb4-27d9-4112-9e6a-5a7d0210af6f
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Reference COM Objects from Visual Basic
In [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)], adding references to COM objects that have type libraries requires the creation of an interop assembly for the COM library. References to the members of the COM object are routed to the interop assembly and then forwarded to the actual COM object. Responses from the COM object are routed to the interop assembly and forwarded to your [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] application.  
  
 You can reference a COM object without using an interop assembly by embedding the type information for the COM object in a .NET assembly. To embed type information, set the `Embed Interop Types` property to `True` for the reference to the COM object. If you are compiling by using the command-line compiler, use the `/link` option to reference the COM library. For more information, see [/link (Visual Basic)](../Topic/-link%20\(Visual%20Basic\).md).  
  
 [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] automatically creates interop assemblies when you add a reference to a type library from the integrated development environment (IDE). When working from the command line, you can use the Tlbimp utility to manually create interop assemblies.  
  
### To add references to COM objects  
  
1.  On the **Project** menu, choose **Add Reference** and then click the **COM** tab in the dialog box.  
  
2.  Select the component you want to use from the list of COM objects.  
  
3.  To simplify access to the interop assembly, add an `Imports` statement to the top of the class or module in which you will use the COM object. For example, the following code example imports the namespace `INKEDLib` for objects referenced in the `Microsoft InkEdit Control 1.0` library.  
  
     [!CODE [VbVbalrInterop#40](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrInterop#40)]  
  
### To create an interop assembly using Tlbimp  
  
1.  Add the location of Tlbimp to the search path, if it is not already part of the search path and you are not currently in the directory where it is located.  
  
2.  Call Tlbimp from a command prompt, providing the following information:  
  
    -   Name and location of the DLL that contains the type library  
  
    -   Name and location of the namespace where the information should be placed  
  
    -   Name and location of the target interop assembly  
  
     The following code provides an example:  
  
    ```  
    Tlbimp test3.dll /out:NameSpace1 /out:Interop1.dll  
    ```  
  
     You can use Tlbimp to create interop assemblies for type libraries, even for unregistered COM objects. However, the COM objects referred to by interop assemblies must be properly registered on the computer where they are to be used. You can register a COM object by using the Regsvr32 utility included with the Windows operating system.  
  
## See Also  
 [COM Interop](../vs140/COM-Interop--Visual-Basic-.md)   
 [Type Library Importer (Tlbimp.exe)](assetId:///ec0a8d63-11b3-4acd-b398-da1e37e97382)   
 [Type Library Exporter (Tlbexp.exe)](assetId:///a487d61b-d166-467b-a7ca-d8b52fbff42d)   
 [Walkthrough: Implementing Inheritance with COM Objects](../vs140/Walkthrough--Implementing-Inheritance-with-COM-Objects--Visual-Basic-.md)   
 [Troubleshooting Interoperability](../vs140/Troubleshooting-Interoperability--Visual-Basic-.md)   
 [Imports Statement (.NET Namespace and Type)](../Topic/Imports%20Statement%20\(.NET%20Namespace%20and%20Type\).md)