---
title: "&#39;Class_Terminate&#39; event is no longer supported"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 11eeac74-666d-4b23-81bc-b1691290ddd0
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Class_Terminate&#39; event is no longer supported
'Class_Terminate' event is no longer supported. Use 'Sub Finalize' to free resources.  
  
 The `Class_Terminate` event of previous versions of Visual Basic is replaced by class destructors.  
  
 By default, this message is a warning. For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
 **Error ID:** BC42002  
  
### To correct this error  
  
-   Declare a `Sub` procedure named `Finalize` to terminate a class. `Sub Finalize` is called when the garbage collector detects that there are no more active references to the instance.  
  
## See Also  
 [Classes for Visual Basic 6.0 Users](assetId:///d625222c-cd32-4c8d-b25c-ea71729b88b7)   
 [NOT IN BUILD: Using Constructors and Destructors](assetId:///548eebe1-86c4-4377-b2f5-447cb8be3d90)   
 [NOT IN BUILD: How to: Implement the Dispose Finalize Pattern (Visual Basic)](assetId:///adf7a232-4ebb-485d-8626-8d64421eb0c4)