---
title: "&lt;c&gt; (Visual C++)"
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
ms.assetid: 3b23fc0f-e10d-4dd0-b197-48a46cbddd9f
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;c&gt; (Visual C++)
The <c\> tag indicates that text within a description should be marked as code. Use [<code\>](../vs140/-code---Visual-C---.md) to indicate multiple lines as code.  
  
## Syntax  
  
```  
<c>text</c>  
```  
  
#### Parameters  
 `text`  
 The text you want to indicate as code.  
  
## Remarks  
 Compile with [/doc](../Topic/-doc%20\(Process%20Documentation%20Comments\)%20\(C-C++\).md) to process documentation comments to a file.  
  
## Example  
  
```  
// xml_c_tag.cpp  
// compile with: /doc /LD  
// post-build command: xdcmake xml_c_tag.xdc  
  
/// Text for class MyClass.  
class MyClass {  
public:  
   int m_i;  
   MyClass() : m_i(0) {}  
  
   /// <summary><c>MyMethod</c> is a method in the <c>MyClass</c> class.  
   /// </summary>  
   int MyMethod(MyClass * a) {  
      return a -> m_i;  
   }  
};  
```  
  
## See Also  
 [XML Documentation](../vs140/XML-Documentation--Visual-C---.md)