---
title: "Usage Warnings"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fe7dc2a3-289d-4bf7-a1e4-0947a81287c4
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Usage Warnings
Usage warnings support proper usage of the .NET Framework.  
  
## In This Section  
  
|Rule|Description|  
|----------|-----------------|  
|[CA1801: Review unused parameters](../vs140/CA1801--Review-unused-parameters.md)|A method signature includes a parameter that is not used in the method body.|  
|[CA1806: Do not ignore method results](../vs140/CA1806--Do-not-ignore-method-results.md)|A new object is created but never used; or a method that creates and returns a new string is called and the new string is never used; or a COM or P/Invoke method returns an HRESULT or error code that is never used.|  
|[CA1816: Call GC.SuppressFinalize correctly](../Topic/CA1816:%20Call%20GC.SuppressFinalize%20correctly.md)|A method that is an implementation of Dispose does not call GC.SuppressFinalize; or a method that is not an implementation of Dispose calls GC.SuppressFinalize; or a method calls GC.SuppressFinalize and passes something other than this (Me in Visual Basic).|  
|[CA2200: Rethrow to preserve stack details](../vs140/CA2200--Rethrow-to-preserve-stack-details.md)|An exception is re-thrown and the exception is explicitly specified in the throw statement. If an exception is re-thrown by specifying the exception in the throw statement, the list of method calls between the original method that threw the exception and the current method is lost.|  
|[CA2201: Do not raise reserved exception types](../Topic/CA2201:%20Do%20not%20raise%20reserved%20exception%20types.md)|This makes the original error hard to detect and debug.|  
|[CA2202: Do not dispose objects multiple times](../vs140/CA2202--Do-not-dispose-objects-multiple-times.md)|A method implementation contains code paths that could cause multiple calls to System.IDisposable.Dispose or a Dispose equivalent (such as a Close() method on some types) on the same object.|  
|[CA2204: Literals should be spelled correctly](../Topic/CA2204:%20Literals%20should%20be%20spelled%20correctly.md)|A literal string in a method body contains one or more words that are not recognized by the Microsoft spelling checker library.|  
|[CA2205: Use managed equivalents of Win32 API](../Topic/CA2205:%20Use%20managed%20equivalents%20of%20Win32%20API.md)|A platform invoke method is defined and a method with the equivalent functionality exists in the .NET Framework class library.|  
|[CA2207: Initialize value type static fields inline](../vs140/CA2207--Initialize-value-type-static-fields-inline.md)|A value type declares an explicit static constructor. To fix a violation of this rule, initialize all static data when it is declared and remove the static constructor.|  
|[CA2208: Instantiate argument exceptions correctly](../vs140/CA2208--Instantiate-argument-exceptions-correctly.md)|A call is made to the default (parameterless) constructor of an exception type that is or derives from ArgumentException, or an incorrect string argument is passed to a parameterized constructor of an exception type that is or derives from ArgumentException.|  
|[CA2211: Non-constant fields should not be visible](../vs140/CA2211--Non-constant-fields-should-not-be-visible.md)|Static fields that are neither constants nor read-only are not thread-safe. Access to such a field must be carefully controlled and requires advanced programming techniques for synchronizing access to the class object.|  
|[CA2212: Do not mark serviced components with WebMethod](../vs140/CA2212--Do-not-mark-serviced-components-with-WebMethod.md)|A method in a type that inherits from System.EnterpriseServices.ServicedComponent is marked with System.Web.Services.WebMethodAttribute. Because WebMethodAttribute and a ServicedComponent method have conflicting behavior and requirements for context and transaction flow, the behavior of the method will be incorrect in some scenarios.|  
|[CA2213: Disposable fields should be disposed](../Topic/CA2213:%20Disposable%20fields%20should%20be%20disposed.md)|A type that implements System.IDisposable declares fields that are of types that also implement IDisposable. The Dispose method of the field is not called by the Dispose method of the declaring type.|  
|[CA2214: Do not call overridable methods in constructors](../vs140/CA2214--Do-not-call-overridable-methods-in-constructors.md)|When a constructor calls a virtual method, it is possible that the constructor for the instance that invokes the method has not executed.|  
|[CA2215: Dispose methods should call base class dispose](../vs140/CA2215--Dispose-methods-should-call-base-class-dispose.md)|If a type inherits from a disposable type, it must call the Dispose method of the base type from its own Dispose method.|  
|[CA2216: Disposable types should declare finalizer](../Topic/CA2216:%20Disposable%20types%20should%20declare%20finalizer.md)|A type that implements System.IDisposable, and has fields that suggest the use of unmanaged resources, does not implement a finalizer as described by Object.Finalize.|  
|[CA2217: Do not mark enums with FlagsAttribute](../Topic/CA2217:%20Do%20not%20mark%20enums%20with%20FlagsAttribute.md)|An externally visible enumeration is marked with FlagsAttribute, and it has one or more values that are not powers of two or a combination of the other defined values on the enumeration.|  
|[CA2218: Override GetHashCode on overriding Equals](../vs140/CA2218--Override-GetHashCode-on-overriding-Equals.md)|GetHashCode returns a value, based on the current instance, that is suited for hashing algorithms and data structures such as a hash table. Two objects that are the same type and are equal must return the same hash code.|  
|[CA2219: Do not raise exceptions in exception clauses](../vs140/CA2219--Do-not-raise-exceptions-in-exception-clauses.md)|When an exception is raised in a finally or fault clause, the new exception hides the active exception. When an exception is raised in a filter clause, the run time silently catches the exception. This makes the original error hard to detect and debug.|  
|[CA2220: Finalizers should call base class finalizer](../Topic/CA2220:%20Finalizers%20should%20call%20base%20class%20finalizer.md)|Finalization must be propagated through the inheritance hierarchy. To guarantee this, types must call their base class Finalize method in their own Finalize method.|  
|[CA2221: Finalizers should be protected](../vs140/CA2221--Finalizers-should-be-protected.md)|Finalizers must use the family access modifier.|  
|[CA2222: Do not decrease inherited member visibility](../vs140/CA2222--Do-not-decrease-inherited-member-visibility.md)|You should not change the access modifier for inherited members. Changing an inherited member to private does not prevent callers from accessing the base class implementation of the method.|  
|[CA2223: Members should differ by more than return type](../vs140/CA2223--Members-should-differ-by-more-than-return-type.md)|Although the common language runtime allows the use of return types to differentiate between otherwise identical members, this feature is not in the Common Language Specification, nor is it a common feature of .NET programming languages.|  
|[CA2224: Override equals on overloading operator equals](../vs140/CA2224--Override-equals-on-overloading-operator-equals.md)|A public type implements the equality operator, but does not override Object.Equals.|  
|[CA2225: Operator overloads have named alternates](../vs140/CA2225--Operator-overloads-have-named-alternates.md)|An operator overload was detected, and the expected named alternative method was not found. The named alternative member provides access to the same functionality as the operator, and is provided for developers who program in languages that do not support overloaded operators.|  
|[CA2226: Operators should have symmetrical overloads](../vs140/CA2226--Operators-should-have-symmetrical-overloads.md)|A type implements the equality or inequality operator, and does not implement the opposite operator.|  
|[CA2227: Collection properties should be read-only](../Topic/CA2227:%20Collection%20properties%20should%20be%20read%20only.md)|A writable collection property allows a user to replace the collection with a different collection. A read-only property stops the collection from being replaced but still allows the individual members to be set.|  
|[CA2228: Do not ship unreleased resource formats](../vs140/CA2228--Do-not-ship-unreleased-resource-formats.md)|Resource files that were built by using pre-release versions of the .NET Framework might not be usable by supported versions of the .NET Framework.|  
|[CA2229: Implement serialization constructors](../Topic/CA2229:%20Implement%20serialization%20constructors.md)|To fix a violation of this rule, implement the serialization constructor. For a sealed class, make the constructor private; otherwise, make it protected.|  
|[CA2230: Use params for variable arguments](../Topic/CA2230:%20Use%20params%20for%20variable%20arguments.md)|A public or protected type contains a public or protected method that uses the VarArgs calling convention instead of the params keyword.|  
|[CA2231: Overload operator equals on overriding ValueType.Equals](../vs140/CA2231--Overload-operator-equals-on-overriding-ValueType.Equals.md)|A value type overrides Object.Equals but does not implement the equality operator.|  
|[CA2232: Mark Windows Forms entry points with STAThread](../Topic/CA2232:%20Mark%20Windows%20Forms%20entry%20points%20with%20STAThread.md)|STAThreadAttribute indicates that the COM threading model for the application is a single-threaded apartment. This attribute must be present on the entry point of any application that uses Windows Forms; if it is omitted, the Windows components might not work correctly.|  
|[CA2233: Operations should not overflow](../vs140/CA2233--Operations-should-not-overflow.md)|Arithmetic operations should not be performed without first validating the operands, to make sure that the result of the operation is not outside the range of possible values for the data types involved.|  
|[CA2234: Pass System.Uri objects instead of strings](../vs140/CA2234--Pass-System.Uri-objects-instead-of-strings.md)|A call is made to a method that has a string parameter whose name contains "uri", "URI", "urn", "URN", "url", or "URL".  The declaring type of the method contains a corresponding method overload that has a System.Uri parameter.|  
|[CA2235: Mark all non-serializable fields](../Topic/CA2235:%20Mark%20all%20non-serializable%20fields.md)|An instance field of a type that is not serializable is declared in a type that is serializable.|  
|[CA2236: Call base class methods on ISerializable types](../Topic/CA2236:%20Call%20base%20class%20methods%20on%20ISerializable%20types.md)|To fix a violation of this rule, call the base type GetObjectData method or serialization constructor from the corresponding derived type method or constructor.|  
|[CA2237: Mark ISerializable types with SerializableAttribute](../vs140/CA2237--Mark-ISerializable-types-with-SerializableAttribute.md)|To be recognized by the common language runtime as serializable, types must be marked with the SerializableAttribute attribute even if the type uses a custom serialization routine through implementation of the ISerializable interface.|  
|[CA2238: Implement serialization methods correctly](../Topic/CA2238:%20Implement%20serialization%20methods%20correctly.md)|A method that handles a serialization event does not have the correct signature, return type, or visibility.|  
|[CA2239: Provide deserialization methods for optional fields](../Topic/CA2239:%20Provide%20deserialization%20methods%20for%20optional%20fields.md)|A type has a field that is marked with the System.Runtime.Serialization.OptionalFieldAttribute attribute, and the type does not provide de-serialization event handling methods.|  
|[CA2240: Implement ISerializable correctly](../Topic/CA2240:%20Implement%20ISerializable%20correctly.md)|To fix a violation of this rule, make the GetObjectData method visible and overridable, and make sure that all instance fields are included in the serialization process or explicitly marked with the NonSerializedAttribute attribute.|  
|[CA2241: Provide correct arguments to formatting methods](../Topic/CA2241:%20Provide%20correct%20arguments%20to%20formatting%20methods.md)|The format argument passed to System.String.Format does not contain a format item that corresponds to each object argument, or vice versa.|  
|[CA2242: Test for NaN correctly](../Topic/CA2242:%20Test%20for%20NaN%20correctly.md)|This expression tests a value against Single.Nan or Double.Nan. Use Single.IsNan(Single) or Double.IsNan(Double) to test the value.|  
|[CA2243: Attribute string literals should parse correctly](../vs140/CA2243--Attribute-string-literals-should-parse-correctly.md)|An attribute's string literal parameter does not parse correctly for a URL, a GUID, or a version.|