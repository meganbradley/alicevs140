---
title: "__event"
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
ms.assetid: d3019b3e-722e-48df-8536-c05878461f9e
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __event
Declares an event.  
  
## Syntax  
  
```  
  
      __event   
      method-declarator  
      ;  
__event __interface interface-specifier;  
__event member-declarator;  
```  
  
## Remarks  
 The keyword `__event` can be applied to a method declaration, an interface declaration, or a data member declaration. However, you cannot use the `__event` keyword to qualify a member of a nested class.  
  
 Depending on whether your event source and receiver are native C++, COM, or managed (.NET Framework), you can use the following constructs as events:  
  
|Native C++|COM|Managed (.NET Framework)|  
|------------------|---------|--------------------------------|  
|Method|—|method|  
|—|interface|—|  
|—|—|data member|  
  
 Use [__hook](../vs140/__hook.md) in an event receiver to associate a handler method with an event method. Note that after you create an event with the `__event` keyword, all event handlers subsequently hooked to that event will be called when the event is called.  
  
 An `__event` method declaration cannot have a definition; a definition is implicitly generated, so the event method can be called as if it were any ordinary method.  
  
> [!NOTE]
>  A templated class or struct cannot contain events.  
  
## Native Events  
 Native events are methods. The return type is typically `HRESULT` or `void`, but can be any integral type, including an `enum`. When an event uses an integral return type, an error condition is defined when an event handler returns a nonzero value, in which case the event being raised will call the other delegates.  
  
```  
// Examples of native C++ events:  
__event void OnDblClick();  
__event HRESULT OnClick(int* b, char* s);  
```  
  
 See [Event Handling in Native C++](../vs140/Event-Handling-in-Native-C--.md) for sample code.  
  
## COM Events  
 COM events are interfaces. The parameters of a method in an event source interface should be **in** parameters (but this is not rigorously enforced), because an **out** parameter is not useful when multicasting. A level 1 warning will be issued if you use an **out** parameter.  
  
 The return type is typically `HRESULT` or `void`, but can be any integral type, including `enum`. When an event uses an integral return type and an event handler returns a nonzero value, it is an error condition, in which case the event being raised aborts calls to the other delegates. Note that the compiler will automatically mark an event source interface as a [source](../vs140/source--C---.md) in the generated IDL.  
  
 The [__interface](../vs140/__interface.md) keyword is always required after `__event` for a COM event source.  
  
```  
// Example of a COM event:  
__event __interface IEvent1;  
```  
  
 See [Event Handling in COM](../vs140/Event-Handling-in-COM.md) for sample code.  
  
## Managed Events  
 For information on coding events in the new syntax, see [event](../vs140/event---C---Component-Extensions-.md).  
  
 Managed events are data members or methods. When used with an event, the return type of a delegate must be compliant with the [Common Language Specification](assetId:///4f0b77d0-4844-464f-af73-6e06bedeafc6). The return type of the event handler must match the return type of the delegate. For more information on delegates, see [__delegate](../vs140/__delegate.md). If a managed event is a data member, its type must be a pointer to a delegate.  
  
 In the .NET Framework, you can treat a data member as if it were a method itself (that is, the `Invoke` method of its corresponding delegate). You must predefine the delegate type for declaring a managed event data member. In contrast, a managed event method implicitly defines the corresponding managed delegate if it is not already defined. For example, you can declare an event value such as `OnClick` as an event as follows:  
  
```  
// Examples of managed events:  
__event ClickEventHandler* OnClick;  // data member as event  
__event void OnClick(String* s);  // method as event  
```  
  
 When implicitly declaring a managed event, you can specify add and remove accessors that will be called when event handlers are added or removed. You can also define the method that calls (raises) the event from outside the class.  
  
## Example: Native Events  
  
```  
// EventHandling_Native_Event.cpp  
// compile with: /c  
[event_source(native)]  
class CSource {  
public:  
   __event void MyEvent(int nValue);  
};  
```  
  
## Example: COM Events  
  
```  
// EventHandling_COM_Event.cpp  
// compile with: /c  
#define _ATL_ATTRIBUTES 1  
#include <atlbase.h>  
#include <atlcom.h>  
  
[ module(dll, name="EventSource", uuid="6E46B59E-89C3-4c15-A6D8-B8A1CEC98830") ];  
  
[ dual, uuid("00000000-0000-0000-0000-000000000002") ]  
__interface IEventSource {  
   [id(1)] HRESULT MyEvent();  
};  
 [ coclass, uuid("00000000-0000-0000-0000-000000000003"),  event_source(com) ]  
class CSource : public IEventSource {  
public:  
   __event __interface IEventSource;  
   HRESULT FireEvent() {  
      __raise MyEvent();  
      return S_OK;  
   }  
};  
```  
  
## Example: Managed Events  
  
```  
// EventHandling_Managed_Event.cpp  
// compile with: /clr:oldSyntax /c  
using namespace System;  
[event_source(managed)]  
public __gc class CPSource {  
  
public:  
   __event void MyEvent(Int16 nValue);  
};  
```  
  
 When applying an attribute to an event, you can specify that the attribute apply to either the generated methods or to the Invoke method of the generated delegate.  The default (`event:`) is to apply the attribute to the event.  
  
```  
// EventHandling_Managed_Event_2.cpp  
// compile with: /clr:oldSyntax /c  
using namespace System;  
[attribute(All, AllowMultiple=true)]  
public __gc class Attr {};  
  
public __delegate void D();  
  
public __gc class X {  
public:  
   [method:Attr] __event D* E;  
   [returnvalue:Attr] __event void noE();  
};  
```  
  
## See Also  
 [Keywords](../vs140/Keywords--C---.md)   
 [Event Handling](../vs140/Event-Handling.md)   
 [event_source](../vs140/event_source.md)   
 [event_receiver](../vs140/event_receiver.md)   
 [__hook](../vs140/__hook.md)   
 [__unhook](../vs140/__unhook.md)   
 [__raise](../vs140/__raise.md)