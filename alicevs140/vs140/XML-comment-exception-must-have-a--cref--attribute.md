---
title: "XML comment exception must have a &#39;cref&#39; attribute"
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
ms.assetid: 62eeeba3-6811-48be-b1ef-c2e4feda3177
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# XML comment exception must have a &#39;cref&#39; attribute
The <exception\> tag provides a way to document the exceptions that may be thrown by a method. The required `cref` attribute designates the name of a member, which is checked by the documentation generator. If the member exists, it is translated to the canonical element name in the documentation file.  
  
 **Error ID:** BC42319  
  
### To correct this error  
  
-   Add the `cref` attribute to the exception as follows:  
  
    ```  
    '''<exception cref="member">description</exception>  
    ```  
  
## See Also  
 [<exception\> (Visual Basic)](../vs140/-exception---Visual-Basic-.md)   
 [How to: Create XML Documentation in Visual Basic](../vs140/How-to--Create-XML-Documentation-in-Visual-Basic.md)   
 [Recommended XML Tags for Documentation Comments (Visual Basic)](../vs140/Recommended-XML-Tags-for-Documentation-Comments--Visual-Basic-.md)