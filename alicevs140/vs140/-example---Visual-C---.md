---
title: "&lt;example&gt; (Visual C++)"
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
ms.assetid: c821aaa7-7ea7-4bee-9922-6705ad57f877
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;example&gt; (Visual C++)
The <example\> tag lets you specify an example of how to use a method or other library member. Commonly, this would also involve use of the [<code\>](../vs140/-code---Visual-C---.md) tag.  
  
## Syntax  
  
```  
<example>description</example>  
```  
  
#### Parameters  
 `description`  
 A description of the code sample.  
  
## Remarks  
 Compile with [/doc](../Topic/-doc%20\(Process%20Documentation%20Comments\)%20\(C-C++\).md) to process documentation comments to a file.  
  
## Example  
  
```  
// xml_example_tag.cpp  
// compile with: /clr /doc /LD  
// post-build command: xdcmake xml_example_tag.dll  
  
/// Text for class MyClass.  
public ref class MyClass {  
public:  
   /// <summary>  
   /// GetZero method  
   /// </summary>  
   /// <example> This sample shows how to call the GetZero method.  
   /// <code>  
   /// int main()   
   /// {  
   ///    return GetZero();  
   /// }  
   /// </code>  
   /// </example>  
   static int GetZero() {  
      return 0;  
   }  
};  
```  
  
## See Also  
 [XML Documentation](../vs140/XML-Documentation--Visual-C---.md)