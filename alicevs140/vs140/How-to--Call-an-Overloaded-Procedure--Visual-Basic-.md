---
title: "How to: Call an Overloaded Procedure (Visual Basic)"
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
ms.assetid: 3bb331fb-f6bc-406f-9ca0-9609b497014c
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Call an Overloaded Procedure (Visual Basic)
The advantage of overloading a procedure is in the flexibility of the call. The calling code can obtain the information it needs to pass to the procedure and then call a single procedure name, no matter what arguments it is passing.  
  
### To call a procedure that has more than one version defined  
  
1.  In the calling code, determine which data to pass to the procedure.  
  
2.  Write the procedure call in the normal way, presenting the data in the argument list. Be sure the arguments match the parameter list in one of the versions defined for the procedure.  
  
3.  You do not have to determine which version of the procedure to call. [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] passes control to the version matching your argument list.  
  
     The following example calls the `post` procedure declared in [How to: Define Multiple Versions of a Procedure](../vs140/How-to--Define-Multiple-Versions-of-a-Procedure--Visual-Basic-.md). It obtains the customer identification, determines whether it is a `String` or an `Integer`, and then in either case calls the same procedure.  
  
     [!CODE [VbVbcnProcedures#56](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#56)]  
  
     [!CODE [VbVbcnProcedures#57](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#57)]  
  
## See Also  
 [Procedures in Visual Basic](../vs140/Procedures-in-Visual-Basic.md)   
 [Procedure Parameters and Arguments](../vs140/Procedure-Parameters-and-Arguments--Visual-Basic-.md)   
 [Procedure Overloading](../Topic/Procedure%20Overloading%20\(Visual%20Basic\).md)   
 [Troubleshooting Procedures](../vs140/Troubleshooting-Procedures--Visual-Basic-.md)   
 [How to: Define Multiple Versions of a Procedure](../vs140/How-to--Define-Multiple-Versions-of-a-Procedure--Visual-Basic-.md)   
 [How to: Overload a Procedure that Takes Optional Parameters](../vs140/How-to--Overload-a-Procedure-that-Takes-Optional-Parameters--Visual-Basic-.md)   
 [How to: Overload a Procedure that Takes an Indefinite Number of Parameters](../vs140/How-to--Overload-a-Procedure-that-Takes-an-Indefinite-Number-of-Parameters--Visual-Basic-.md)   
 [Considerations in Overloading Procedures](../vs140/Considerations-in-Overloading-Procedures--Visual-Basic-.md)   
 [Overload Resolution](../vs140/Overload-Resolution--Visual-Basic-.md)   
 [Overloads](../vs140/Overloads--Visual-Basic-.md)