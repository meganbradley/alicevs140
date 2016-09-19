---
title: "Boxing  (C++ Component Extensions)"
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
ms.assetid: b5fd2c98-c578-4f83-8257-6dd663478665
caps.latest.revision: 27
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Boxing  (C++ Component Extensions)
The Visual C++ compiler can convert value types to objects in a process called *boxing*, and convert objects to value types in a process called *unboxing*.  
  
## All Runtimes  
 (There are no remarks for this language feature that apply to all runtimes.)  
  
## Windows Runtime  
 [!INCLUDE[cppwrt_short](../vs140/includes/cppwrt_short_md.md)] supports a shorthand syntax for boxing value types and unboxing reference types. A value type is boxed when it is assigned to a variable of type `Object`. An `Object` variable is unboxed when it is assigned to a value type variable and the unboxed type is specified in parentheses; that is, when the object variable is cast to a value type.  
  
```  
  
  Platform::Object^  
  object_variable  = value_variable;  
value_variable = (value_type) object_variable;  
  
```  
  
### Requirements  
 Compiler option: **/ZW**  
  
### Examples  
 The following code example boxes and unboxes a `DateTime` value. First, the example obtains a DateTime value that represents the current date and time and assigns it to a DateTime variable. Then the DateTime is boxed by assigning it to an Object variable. Finally, the boxed value is unboxed by assigning it to another DateTime variable.  
  
 To test the example, create a BlankApplication project, replace the BlankPage::OnNavigatedTo() method, and then specify breakpoints at the closing bracket and the assignment to variable str1. When the example reaches the closing bracket, examine str1.  
  
```  
  
void BlankPage::OnNavigatedTo(NavigationEventArgs^ e)  
{  
    using namespace Windows::Globalization::DateTimeFormatting;  
  
    Windows::Foundation::DateTime dt, dtAnother;  
    Platform::Object^ obj1;  
  
    Windows::Globalization::Calendar^ c =   
        ref new Windows::Globalization::Calendar;  
    c->SetToNow();  
    dt = c->GetDateTime();  
    auto dtf = ref new DateTimeFormatter(  
                           YearFormat::Full,   
                           MonthFormat::Numeric,   
                           DayFormat::Default,   
                           DayOfWeekFormat::None);  
    String^ str1 = dtf->Format(dt);  
    OutputDebugString(str1->Data());  
    OutputDebugString(L"\r\n");  
  
    // Box the value type and assign to a reference type.  
    obj1 = dt;  
    // Unbox the reference type and assign to a value type.  
    dtAnother = (Windows::Foundation::DateTime) obj1;  
  
    // Format the DateTime for display.  
    String^ str2 = dtf->Format(dtAnother);  
    OutputDebugString(str2->Data());  
}  
  
```  
  
 For more information, see [Boxing (C++/CX)](http://msdn.microsoft.com/library/windows/apps/hh969554.aspx).  
  
## Common Language Runtime  
 The Visual C++ compiler now boxes value types to <xref:System.Object?qualifyHint=False>.  This is possible because of a compiler-defined conversion to convert value types to <xref:System.Object?qualifyHint=False>.  
  
 Boxing and unboxing enable value types to be treated as objects. Value types, including both struct types and built-in types such as int, can be converted to and from the type <xref:System.Object?qualifyHint=False>.  
  
 For more information, see:  
  
-   [How to: Explicitly Request Boxing](../vs140/How-to--Explicitly-Request-Boxing.md)  
  
-   [How to: Use gcnew to Create Value Types and Use Implicit Boxing](../vs140/How-to--Use-gcnew-to-Create-Value-Types-and-Use-Implicit-Boxing.md)  
  
-   [How to: Unboxing](../vs140/How-to--Unbox.md)  
  
-   [Standard Conversions and Implicit Boxing](../vs140/Standard-Conversions-and-Implicit-Boxing.md)  
  
### Requirements  
 Compiler option: **/clr**  
  
### Examples  
 **Example**  
  
 The following sample shows how implicit boxing works.  
  
```cpp  
// vcmcppv2_explicit_boxing2.cpp  
// compile with: /clr  
using namespace System;  
  
ref class A {  
public:  
   void func(System::Object^ o){Console::WriteLine("in A");}  
};  
  
value class V {};  
  
interface struct IFace {  
   void func();  
};  
  
value class V1 : public IFace {  
public:  
   virtual void func() {  
      Console::WriteLine("Interface function");  
   }  
};  
  
value struct V2 {  
   // conversion operator to System::Object  
   static operator System::Object^(V2 v2) {  
      Console::WriteLine("operator System::Object^");  
      return (V2^)v2;  
   }  
};  
  
void func1(System::Object^){Console::WriteLine("in void func1(System::Object^)");}  
void func1(V2^){Console::WriteLine("in func1(V2^)");}  
  
void func2(System::ValueType^){Console::WriteLine("in func2(System::ValueType^)");}  
void func2(System::Object^){Console::WriteLine("in func2(System::Object^)");}  
  
int main() {  
   // example 1 simple implicit boxing  
   Int32^ bi = 1;  
   Console::WriteLine(bi);  
  
   // example 2 calling a member with implicit boxing  
   Int32 n = 10;  
   Console::WriteLine("xx = {0}", n.ToString());  
  
   // example 3 implicit boxing for function calls  
   A^ a = gcnew A;  
   a->func(n);  
  
   // example 4 implicit boxing for WriteLine function call  
   V v;  
   Console::WriteLine("Class {0} passed using implicit boxing", v);  
   Console::WriteLine("Class {0} passed with forced boxing", (V^)(v));   // force boxing  
  
   // example 5 casting to a base with implicit boxing  
   V1 v1;  
   IFace ^ iface = v1;  
   iface->func();  
  
   // example 6 user-defined conversion preferred over implicit boxing for function-call parameter matching  
   V2 v2;  
   func1(v2);   // user defined conversion from V2 to System::Object preferred over implicit boxing  
                // Will call void func1(System::Object^);  
  
   func2(v2);   // OK: Calls "static V2::operator System::Object^(V2 v2)"  
   func2((V2^)v2);   // Using explicit boxing: calls func2(System::ValueType^)  
}  
```  
  
 **Output**  
  
 **1**   
 **xx = 10**   
 **in A**   
 **Class V passed using implicit boxing**   
 **Class V passed with forced boxing**   
 **Interface function**   
 **in func1(V2^)**   
 **in func2(System::ValueType^)**   
 **in func2(System::ValueType^)**   
## See Also  
 [Component Extensions for Runtime Platforms](../Topic/Component%20Extensions%20for%20Runtime%20Platforms.md)