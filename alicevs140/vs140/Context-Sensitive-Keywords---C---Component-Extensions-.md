---
title: "Context-Sensitive Keywords  (C++ Component Extensions)"
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
ms.topic: language-reference
ms.assetid: e33da089-f434-44e9-8cce-4668d05a8939
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Context-Sensitive Keywords  (C++ Component Extensions)
*Context-sensitive keywords* are language elements that are recognized only in specific contexts. Outside the specific context, a context-sensitive keyword can be a user-defined symbol.  
  
## All Runtimes  
 **Remarks**  
  
 The following is a list of context-sensitive keywords:  
  
-   [abstract](../vs140/abstract---C---Component-Extensions-.md)  
  
-   [delegate](../vs140/delegate---C---Component-Extensions-.md)  
  
-   [event](../vs140/event---C---Component-Extensions-.md)  
  
-   [finally](../vs140/finally.md)  
  
-   [for each, in](../Topic/for%20each,%20in.md)  
  
-   [initonly](../vs140/initonly--C---CLI-.md)  
  
-   `internal` (see [Member Visibility](../vs140/Member-Visibility.md))  
  
-   [literal](../vs140/literal--C---Component-Extensions-.md)  
  
-   [override](../vs140/override---C---Component-Extensions-.md)  
  
-   [property](../vs140/property---C---Component-Extensions-.md)  
  
-   [sealed](../vs140/sealed---C---Component-Extensions-.md)  
  
-   `where` (part of [generics](../vs140/Generics---C---Component-Extensions-.md))  
  
 For readability purposes, you may want to limit your use of context-sensitive keywords as user–defined symbols.  
  
## [!INCLUDE[wrt](../vs140/includes/wrt_md.md)]  
 **Remarks**  
  
 (There are no platform-specific remarks for this feature.)  
  
### Requirements  
 Compiler option: **/ZW**  
  
## [!INCLUDE[clr_for_headings](../vs140/includes/clr_for_headings_md.md)]  
 **Remarks**  
  
 (There are no platform-specific remarks for this feature.)  
  
### Requirements  
 Compiler option: **/clr**  
  
### Examples  
 **Example**  
  
 The following code example shows that in the appropriate context, the `property` context-sensitive keyword can be used to define a property and a variable.  
  
```  
// context_sensitive_keywords.cpp  
// compile with: /clr  
public ref class C {  
   int MyInt;  
public:  
   C() : MyInt(99) {}  
  
   property int Property_Block {   // context-sensitive keyword  
      int get() { return MyInt; }  
   }  
};  
  
int main() {  
   int property = 0;               // variable name  
   C ^ MyC = gcnew C();  
   property = MyC->Property_Block;  
   System::Console::WriteLine(++property);  
}  
```  
  
 **Output**  
  
 **100**   
## See Also  
 [Language Extensions for Runtime Platforms](../Topic/Component%20Extensions%20for%20Runtime%20Platforms.md)