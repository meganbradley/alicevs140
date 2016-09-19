---
title: "Illegal call expression or index expression"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: eed6a16e-4a44-4f72-b1de-d4212940da37
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Illegal call expression or index expression
A value in parentheses follows an expression that is not a procedure, property, or array.  
  
 The following code can generate this error.  
  
 `Dim testVariable As Object = Nothing(1)`  
  
 Because `Nothing` does not take arguments or indexes, you cannot use it with parentheses.  
  
 **Error ID:** BC32303  
  
### To correct this error  
  
-   Remove the parentheses and any value they contain.  
  
## See Also  
 [How to: Call a Procedure that Returns a Value](../vs140/How-to--Call-a-Procedure-That-Returns-a-Value--Visual-Basic-.md)   
 [How to: Call a Procedure that Does Not Return a Value](../vs140/How-to--Call-a-Procedure-that-Does-Not-Return-a-Value--Visual-Basic-.md)   
 [NOTINBUILD How to: Put a Value into an Array](assetId:///6dddc79c-cf60-41c2-b572-8bfa49b4fe7e)   
 [NOTINBUILD How to: Get a Value from an Array](assetId:///202a6468-8ccb-4864-bd8b-eab3b42d4288)   
 [How to: Put a Value in a Property](../Topic/How%20to:%20Put%20a%20Value%20in%20a%20Property%20\(Visual%20Basic\).md)   
 [How to: Get a Value from a Property](../vs140/How-to--Get-a-Value-from-a-Property--Visual-Basic-.md)