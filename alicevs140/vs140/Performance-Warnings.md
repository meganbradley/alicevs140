---
title: "Performance Warnings"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e014ac3a-02e6-46d9-942c-3491dd63782f
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Performance Warnings
Performance warnings support high-performance libraries and applications.  
  
## In This Section  
  
|Rule|Description|  
|----------|-----------------|  
|[CA1800: Do not cast unnecessarily](../vs140/CA1800--Do-not-cast-unnecessarily.md)|Duplicate casts decrease performance, especially when the casts are performed in compact iteration statements.|  
|[CA1801: Review unused parameters](../vs140/CA1801--Review-unused-parameters.md)|A method signature includes a parameter that is not used in the method body.|  
|[CA1802: Use literals where appropriate](../vs140/CA1802--Use-Literals-Where-Appropriate.md)|A field is declared static and read-only (Shared and ReadOnly in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)]), and is initialized with a value that is computable at compile time. Because the value that is assigned to the targeted field is computable at compile time, change the declaration to a const (Const in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)]) field so that the value is computed at compile time instead of at run time.|  
|[CA1804: Remove unused locals](../vs140/CA1804--Remove-unused-locals.md)|Unused local variables and unnecessary assignments increase the size of an assembly and decrease performance.|  
|[CA1806: Do not ignore method results](../vs140/CA1806--Do-not-ignore-method-results.md)|A new object is created but never used, or a method that creates and returns a new string is called and the new string is never used, or a Component Object Model (COM) or P/Invoke method returns an HRESULT or error code that is never used.|  
|[CA1809: Avoid excessive locals](../vs140/CA1809--Avoid-excessive-locals.md)|A common performance optimization is to store a value in a processor register instead of memory, which is referred to as "enregistering the value".  To increase the chance that all local variables are enregistered, limit the number of local variables to 64.|  
|[CA1810: Initialize reference type static fields inline](../vs140/CA1810--Initialize-reference-type-static-fields-inline.md)|When a type declares an explicit static constructor, the just-in-time (JIT) compiler adds a check to each static method and instance constructor of the type to make sure that the static constructor was previously called. Static constructor checks can decrease performance.|  
|[CA1811: Avoid uncalled private code](../Topic/CA1811:%20Avoid%20uncalled%20private%20code.md)|A private or internal (assembly-level) member does not have callers in the assembly, it is not invoked by the common language runtime, and it is not invoked by a delegate.|  
|[CA1812: Avoid uninstantiated internal classes](../Topic/CA1812:%20Avoid%20uninstantiated%20internal%20classes.md)|An instance of an assembly-level type is not created by code in the assembly.|  
|[CA1813: Avoid unsealed attributes](../Topic/CA1813:%20Avoid%20unsealed%20attributes.md)|The [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] class library provides methods for retrieving custom attributes. By default, these methods search the attribute inheritance hierarchy. Sealing the attribute eliminates the search through the inheritance hierarchy and can improve performance.|  
|[CA1814: Prefer jagged arrays over multidimensional](../vs140/CA1814--Prefer-jagged-arrays-over-multidimensional.md)|A jagged array is an array whose elements are arrays. The arrays that make up the elements can be of different sizes, which can result in less wasted space for some sets of data.|  
|[CA1815: Override equals and operator equals on value types](../Topic/CA1815:%20Override%20equals%20and%20operator%20equals%20on%20value%20types.md)|For value types, the inherited implementation of Equals uses the Reflection library and compares the contents of all fields. Reflection is computationally expensive, and comparing every field for equality might be unnecessary. If you expect users to compare or sort instances, or to use instances as hash table keys, your value type should implement Equals.|  
|[CA1816: Call GC.SuppressFinalize correctly](../Topic/CA1816:%20Call%20GC.SuppressFinalize%20correctly.md)|A method that is an implementation of Dispose does not call GC.SuppressFinalize, or a method that is not an implementation of Dispose calls GC.SuppressFinalize, or a method calls GC.SuppressFinalize and passes something other than this (Me in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)]).|  
|[CA1819: Properties should not return arrays](../Topic/CA1819:%20Properties%20should%20not%20return%20arrays.md)|Arrays that are returned by properties are not write-protected, even if the property is read-only. To keep the array tamper-proof, the property must return a copy of the array. Typically, users will not understand the adverse performance implications of calling such a property.|  
|[CA1820: Test for empty strings using string length](../Topic/CA1820:%20Test%20for%20empty%20strings%20using%20string%20length.md)|Comparing strings by using the String.Length property or the String.IsNullOrEmpty method is significantly faster than using Equals.|  
|[CA1821: Remove empty finalizers](../vs140/CA1821--Remove-empty-finalizers.md)|Whenever you can, avoid finalizers because of the additional performance overhead that is involved in tracking object lifetime. An empty finalizer incurs added overhead without any benefit.|  
|[CA1822: Mark members as static](../vs140/CA1822--Mark-members-as-static.md)|Members that do not access instance data or call instance methods can be marked as static (Shared in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)]). After you mark the methods as static, the compiler will emit nonvirtual call sites to these members. This can give you a measurable performance gain for performance-sensitive code.|  
|[CA1823: Avoid unused private fields](../vs140/CA1823--Avoid-unused-private-fields.md)|Private fields were detected that do not appear to be accessed in the assembly.|  
|[CA1824: Mark assemblies with NeutralResourcesLanguageAttribute](../Topic/CA1824:%20Mark%20assemblies%20with%20NeutralResourcesLanguageAttribute.md)|The NeutralResourcesLanguage attribute informs the ResourceManager of the language that was used to display the resources of a neutral culture for an assembly. This improves lookup performance for the first resource that you load and can reduce your working set.|