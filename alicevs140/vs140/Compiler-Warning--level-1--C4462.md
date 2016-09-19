---
title: "Compiler Warning (level 1) C4462"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: 4e20aca4-293e-4c75-a83d-961c27ab7840
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4462
cannot determine the GUID of the type. Program may fail at runtime.  
  
 Warning C4462 occurs in a Windows Runtime app or component when a public `TypedEventHandler` has as one of its type parameters a reference to the enclosing class.  
  
 **This kind of code raises the warning:**  
  
```  
namespace N  
{  
       public ref struct EventArgs sealed {};  
       public ref struct R sealed  
       {  
              R() {}  
              event Windows::Foundation::TypedEventHandler<R ^, EventArgs^>^ e;  
       };  
}  
  
[Platform::MTAThread]  
int main()  
{  
     auto x = ref new N::R();  
}  
  
```  
  
 **To fix the error:**  
  
 There are two ways to work around the error. One way, shown in the next example, is to give the event internal accessibility so that it is available to code in the same executable but not to code in other Windows Runtime components.  
  
```  
  
      internal:  
event Windows::Foundation::TypedEventHandler<R ^, EventArgs^>^ e;  
  
```  
  
 If the event must be public, then you can use the other workaround, which is to expose it through a default interface:  
  
```  
  
ref struct R;  
public interface struct IR{ event Windows::Foundation::TypedEventHandler<R ^, EventArgs^>^ e;};  
  
public ref struct R sealed : [Windows::Foundation::Metadata::Default] IR  
{  
    R() {}  
    virtual event Windows::Foundation::TypedEventHandler<R ^, EventArgs^>^ e;  
};  
  
```  
  
 A GUID of the type `Windows::Foundation::TypedEventHandler<R ^, EventArgs^>^` is only used when the type is accessed from another component. The first workaround works because it can only be accessed within its own component after the workaround. Otherwise, the compiler has to assume the worst case and emit the warning.