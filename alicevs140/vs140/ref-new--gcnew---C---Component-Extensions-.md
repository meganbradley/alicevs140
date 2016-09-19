---
title: "ref new, gcnew  (C++ Component Extensions)"
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
ms.assetid: 388a62da-c2df-4a94-a9a2-205b53e577da
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ref new, gcnew  (C++ Component Extensions)
The `ref new` aggregate keyword allocates an instance of a type that is garbage collected when the object becomes inaccessible, and that returns a handle ([^](../vs140/Handle-to-Object-Operator--^----C---Component-Extensions-.md)) to the allocated object.  
  
## All Runtimes  
 Memory for an instance of a type that is allocated by `ref new` is deallocated automatically.  
  
 A `ref new` operation throws `OutOfMemoryException` if it is unable to allocate memory.  
  
 For more information about how memory for native C++ types is allocated and deallocated, see [the new and delete operators](../vs140/new-and-delete-Operators.md).  
  
## [!INCLUDE[wrt](../vs140/includes/wrt_md.md)]  
 Use `ref new` to allocate memory for Windows Runtime objects whose lifetime you want to administer automatically. The object is automatically deallocated when its reference count goes to zero, which occurs after the last copy of the reference has gone out of scope. For more information, see [Ref classes and structs](http://msdn.microsoft.com/library/windows/apps/hh699870.aspx).  
  
### Requirements  
 Compiler option: **/ZW**  
  
## [!INCLUDE[clr_for_headings](../vs140/includes/clr_for_headings_md.md)]  
 Memory for a managed type (reference or value type) is allocated by `gcnew`, and deallocated by using garbage collection.  
  
### Requirements  
 Compiler option: **/clr**  
  
### Examples  
 **Example**  
  
 The following example uses `gcnew` to allocate a Message object.  
  
```  
// mcppv2_gcnew_1.cpp  
// compile with: /clr  
ref struct Message {  
   System::String^ sender;  
   System::String^ receiver;  
   System::String^ data;  
};  
  
int main() {  
   Message^ h_Message  = gcnew Message;  
  //...  
}  
```  
  
 **Example**  
  
 The following example uses `gcnew` to create a boxed value type for use like a reference type.  
  
```  
// example2.cpp : main project file.  
// compile with /clr  
using namespace System;  
value class Boxed {  
    public:  
        int i;  
};  
int main()  
{  
    Boxed^ y = gcnew Boxed;  
    y->i = 32;  
    Console::WriteLine(y->i);  
    return 0;  
}  
```  
  
 **Output**  
  
 **32**   
## See Also  
 [Language Extensions for Runtime Platforms](../Topic/Component%20Extensions%20for%20Runtime%20Platforms.md)