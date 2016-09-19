---
title: "Performing Tasks with My.Application, My.Computer, and My.User (Visual Basic)"
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
ms.assetid: c8af61bd-4dd3-4a0f-9af5-795b594b240b
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Performing Tasks with My.Application, My.Computer, and My.User (Visual Basic)
The three central `My` objects that provide access to information and commonly used functionality are `My.Application` (<xref:Microsoft.VisualBasic.ApplicationServices.ApplicationBase?qualifyHint=False>), `My.Computer` (<xref:Microsoft.VisualBasic.Devices.Computer?qualifyHint=False>), and `My.User` (<xref:Microsoft.VisualBasic.ApplicationServices.User?qualifyHint=False>). You can use these objects to access information that is related to the current application, the computer that the application is installed on, or the current user of the application, respectively.  
  
## My.Application, My.Computer, and My.User  
 The following examples demonstrate how information can be retrieved using `My`.  
  
 [!CODE [VbVbcnMy#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMy#1)]  
  
 [!CODE [VbVbcnMy#2](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMy#2)]  
  
 In addition to retrieving information, the members exposed through these three objects also allow you to execute methods related to that object. For instance, you can access a variety of methods to manipulate files or update the registry through `My.Computer`.  
  
 File I/O is significantly easier and faster with `My`, which includes a variety of methods and properties for manipulating files, directories, and drives. The <xref:Microsoft.VisualBasic.FileIO.TextFieldParser?qualifyHint=False> object allows you to read from large structured files that have delimited or fixed-width fields. This example opens the `TextFieldParser``reader` and uses it to read from `C:\TestFolder1\test1.txt`.  
  
 [!CODE [VbVbalrTextFieldParser#23](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrTextFieldParser#23)]  
  
 `My.Application` allows you to change the culture for your application. The following example demonstrates how this method can be called.  
  
 [!CODE [VbVbcnMy#3](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMy#3)]  
  
## See Also  
 <xref:Microsoft.VisualBasic.ApplicationServices.ApplicationBase?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.Devices.Computer?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.ApplicationServices.User?qualifyHint=False>   
 [How My Depends on Project Type](../Topic/How%20My%20Depends%20on%20Project%20Type%20\(Visual%20Basic\).md)