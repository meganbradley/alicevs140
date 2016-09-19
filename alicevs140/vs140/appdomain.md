---
title: "appdomain"
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
ms.assetid: 29d843cb-cb6b-4d1b-a48d-d928a877234d
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# appdomain
Specifies that each application domain of your managed application should have its own copy of a particular global variable or static member variable. See [Application Domains and Visual C++](../vs140/Application-Domains-and-Visual-C--.md) for more information.  
  
 Every application domain has its own copy of a per-appdomain variable. A constructor of an appdomain variable is executed when an assembly is loaded into an application domain, and the destructor is executed when the application domain is unloaded.  
  
 If you want all application domains within a process in the common language runtime to share a global variable, use the `__declspec(process)` modifier. `__declspec(process)` is in effect by default under [/clr](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md) and `__declspec(appdomain)` is in effect by default under **/clr:pure**. `__declspec(appdomain)` is enforced under **/clr:safe**.  
  
 `__declspec(appdomain)` is only valid when one of the **/clr** compiler options is used. Only a global variable, static member variable, or a static local variable can be marked with `__declspec(appdomain)`. It is an error to apply `__declspec(appdomain)` to static members of managed types because they always have this behavior.  
  
 Using `__declspec(appdomain)` is similar to using [Thread Local Storage (TLS)](../Topic/Thread%20Local%20Storage%20\(TLS\).md). Threads have their own storage, as do application domains. Using `__declspec(appdomain)` ensures the global variable has its own storage in each application domain created for this application.  
  
 There are limitations to mixing the use of per process and per appdomain variables; see [process](../vs140/process.md) for more information.  
  
 For example, at program start up, all per-process variables are initialized, then all per-appdomain variables are initialized. Therefore when a per-process variable is being initialized, it cannot depend on the value of any per-application domain variable. It is bad practice to mix the use (assignment) of per appdomain and per process variables.  
  
 For information on how to call a function in a specific application domain, see [call_in_appdomain Function](../vs140/call_in_appdomain-Function.md).  
  
## Example  
  
```  
// declspec_appdomain.cpp  
// compile with: /clr  
#include <stdio.h>  
using namespace System;  
  
class CGlobal {  
public:  
   CGlobal(bool bProcess) {  
      Counter = 10;  
      m_bProcess = bProcess;  
      Console::WriteLine("__declspec({0}) CGlobal::CGlobal constructor", m_bProcess ? (String^)"process" : (String^)"appdomain");  
   }  
  
   ~CGlobal() {  
      Console::WriteLine("__declspec({0}) CGlobal::~CGlobal destructor", m_bProcess ? (String^)"process" : (String^)"appdomain");  
   }  
  
   int Counter;  
  
private:  
   bool m_bProcess;  
};  
  
__declspec(process) CGlobal process_global = CGlobal(true);  
__declspec(appdomain) CGlobal appdomain_global = CGlobal(false);  
  
value class Functions {  
public:  
   static void change() {  
      ++appdomain_global.Counter;  
   }  
  
   static void display() {  
      Console::WriteLine("process_global value in appdomain '{0}': {1}",   
         AppDomain::CurrentDomain->FriendlyName,  
         process_global.Counter);  
  
      Console::WriteLine("appdomain_global value in appdomain '{0}': {1}",   
         AppDomain::CurrentDomain->FriendlyName,  
         appdomain_global.Counter);  
   }  
};  
  
int main() {  
   AppDomain^ defaultDomain = AppDomain::CurrentDomain;  
   AppDomain^ domain = AppDomain::CreateDomain("Domain 1");  
   AppDomain^ domain2 = AppDomain::CreateDomain("Domain 2");  
   CrossAppDomainDelegate^ changeDelegate = gcnew CrossAppDomainDelegate(&Functions::change);  
   CrossAppDomainDelegate^ displayDelegate = gcnew CrossAppDomainDelegate(&Functions::display);  
  
   // Print the initial values of appdomain_global in all appdomains.  
   Console::WriteLine("Initial value");  
   defaultDomain->DoCallBack(displayDelegate);  
   domain->DoCallBack(displayDelegate);  
   domain2->DoCallBack(displayDelegate);  
  
   // Changing the value of appdomain_global in the domain and domain2  
   // appdomain_global value in "default" appdomain remain unchanged  
   process_global.Counter = 20;  
   domain->DoCallBack(changeDelegate);  
   domain2->DoCallBack(changeDelegate);  
   domain2->DoCallBack(changeDelegate);  
  
   // Print values again  
   Console::WriteLine("Changed value");  
   defaultDomain->DoCallBack(displayDelegate);  
   domain->DoCallBack(displayDelegate);  
   domain2->DoCallBack(displayDelegate);  
  
   AppDomain::Unload(domain);  
   AppDomain::Unload(domain2);  
}  
```  
  
 **__declspec(process) CGlobal::CGlobal constructor**  
**__declspec(appdomain) CGlobal::CGlobal constructor**  
**Initial value**  
**process_global value in appdomain 'declspec_appdomain.exe': 10**  
**appdomain_global value in appdomain 'declspec_appdomain.exe': 10**  
**__declspec(appdomain) CGlobal::CGlobal constructor**  
**process_global value in appdomain 'Domain 1': 10**  
**appdomain_global value in appdomain 'Domain 1': 10**  
**__declspec(appdomain) CGlobal::CGlobal constructor**  
**process_global value in appdomain 'Domain 2': 10**  
**appdomain_global value in appdomain 'Domain 2': 10**  
**Changed value**  
**process_global value in appdomain 'declspec_appdomain.exe': 20**  
**appdomain_global value in appdomain 'declspec_appdomain.exe': 10**  
**process_global value in appdomain 'Domain 1': 20**  
**appdomain_global value in appdomain 'Domain 1': 11**  
**process_global value in appdomain 'Domain 2': 20**  
**appdomain_global value in appdomain 'Domain 2': 12**  
**__declspec(appdomain) CGlobal::~CGlobal destructor**  
**__declspec(appdomain) CGlobal::~CGlobal destructor**  
**__declspec(appdomain) CGlobal::~CGlobal destructor**  
**__declspec(process) CGlobal::~CGlobal destructor**   
## See Also  
 [__declspec](../vs140/__declspec.md)   
 [Keywords](../vs140/Keywords--C---.md)