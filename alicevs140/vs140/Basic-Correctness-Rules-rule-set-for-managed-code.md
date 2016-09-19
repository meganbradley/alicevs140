---
title: "Basic Correctness Rules rule set for managed code"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 631f0daf-1d42-4c90-a7dc-1a6a9de64c93
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Basic Correctness Rules rule set for managed code
The Basic Correctness Rules rule set focuses on logic errors and common mistakes in the usage of framework APIs. The Basic Correctness Rules include the rules in the Minimum Recommended Rules rule set. For more information, see [Minimum Recommended Rules Code Analysis Rule Set](../vs140/Managed-Recommended-Rules-rule-set-for-managed-code.md) You should include this rule set to expand on the list of warnings that the minimum recommended rules report.  
  
 The following table describes all the rules in the Microsoft Basic Correctness Rules rule set.  
  
|Rule|Description|  
|----------|-----------------|  
|[CA1001](../vs140/CA1001--Types-that-own-disposable-fields-should-be-disposable.md)|Types that own disposable fields should be disposable|  
|[CA1009](../Topic/CA1009:%20Declare%20event%20handlers%20correctly.md)|Declare event handlers correctly|  
|[CA1016](../Topic/CA1016:%20Mark%20assemblies%20with%20AssemblyVersionAttribute.md)|Mark assemblies with AssemblyVersionAttribute|  
|[CA1033](../vs140/CA1033--Interface-methods-should-be-callable-by-child-types.md)|Interface methods should be callable by child types|  
|[CA1049](../Topic/CA1049:%20Types%20that%20own%20native%20resources%20should%20be%20disposable.md)|Types that own native resources should be disposable|  
|[CA1060](../vs140/CA1060--Move-P-Invokes-to-NativeMethods-class.md)|Move P/Invokes to NativeMethods class|  
|[CA1061](../vs140/CA1061--Do-not-hide-base-class-methods.md)|Do not hide base class methods|  
|[CA1063](../vs140/CA1063--Implement-IDisposable-correctly.md)|Implement IDisposable correctly|  
|[CA1065](../Topic/CA1065:%20Do%20not%20raise%20exceptions%20in%20unexpected%20locations.md)|Do not raise exceptions in unexpected locations|  
|[CA1301](../Topic/CA1301:%20Avoid%20duplicate%20accelerators.md)|Avoid duplicate accelerators|  
|[CA1400](../Topic/CA1400:%20P-Invoke%20entry%20points%20should%20exist.md)|P/Invoke entry points should exist|  
|[CA1401](../vs140/CA1401--P-Invokes-should-not-be-visible.md)|P/Invokes should not be visible|  
|[CA1403](../Topic/CA1403:%20Auto%20layout%20types%20should%20not%20be%20COM%20visible.md)|Auto layout types should not be COM visible|  
|[CA1404](../Topic/CA1404:%20Call%20GetLastError%20immediately%20after%20P-Invoke.md)|Call GetLastError immediately after P/Invoke|  
|[CA1405](../Topic/CA1405:%20COM%20visible%20type%20base%20types%20should%20be%20COM%20visible.md)|COM visible type base types should be COM visible|  
|[CA1410](../vs140/CA1410--COM-registration-methods-should-be-matched.md)|COM registration methods should be matched|  
|[CA1415](../vs140/CA1415--Declare-P-Invokes-correctly.md)|Declare P/Invokes correctly|  
|[CA1821](../vs140/CA1821--Remove-empty-finalizers.md)|Remove empty finalizers|  
|[CA1900](../vs140/CA1900--Value-type-fields-should-be-portable.md)|Value type fields should be portable|  
|[CA1901](../vs140/CA1901--P-Invoke-declarations-should-be-portable.md)|P/Invoke declarations should be portable|  
|[CA2002](../Topic/CA2002:%20Do%20not%20lock%20on%20objects%20with%20weak%20identity.md)|Do not lock on objects with weak identity|  
|[CA2100](../vs140/CA2100--Review-SQL-queries-for-security-vulnerabilities.md)|Review SQL queries for security vulnerabilities|  
|[CA2101](../vs140/CA2101--Specify-marshaling-for-P-Invoke-string-arguments.md)|Specify marshaling for P/Invoke string arguments|  
|[CA2108](../vs140/CA2108--Review-declarative-security-on-value-types.md)|Review declarative security on value types|  
|[CA2111](../Topic/CA2111:%20Pointers%20should%20not%20be%20visible.md)|Pointers should not be visible|  
|[CA2112](../vs140/CA2112--Secured-types-should-not-expose-fields.md)|Secured types should not expose fields|  
|[CA2114](../vs140/CA2114--Method-security-should-be-a-superset-of-type.md)|Method security should be a superset of type|  
|[CA2116](../vs140/CA2116--APTCA-methods-should-only-call-APTCA-methods.md)|APTCA methods should only call APTCA methods|  
|[CA2117](../Topic/CA2117:%20APTCA%20types%20should%20only%20extend%20APTCA%20base%20types.md)|APTCA types should only extend APTCA base types|  
|[CA2122](../vs140/CA2122--Do-not-indirectly-expose-methods-with-link-demands.md)|Do not indirectly expose methods with link demands|  
|[CA2123](../vs140/CA2123--Override-link-demands-should-be-identical-to-base.md)|Override link demands should be identical to base|  
|[CA2124](../vs140/CA2124--Wrap-vulnerable-finally-clauses-in-outer-try.md)|Wrap vulnerable finally clauses in outer try|  
|[CA2126](../vs140/CA2126--Type-link-demands-require-inheritance-demands.md)|Type link demands require inheritance demands|  
|[CA2131](../vs140/CA2131--Security-critical-types-may-not-participate-in-type-equivalence.md)|Security critical types may not participate in type equivalence|  
|[CA2132](../Topic/CA2132:%20Default%20constructors%20must%20be%20at%20least%20as%20critical%20as%20base%20type%20default%20constructors.md)|Default constructors must be at least as critical as base type default constructors|  
|[CA2133](../vs140/CA2133--Delegates-must-bind-to-methods-with-consistent-transparency.md)|Delegates must bind to methods with consistent transparency|  
|[CA2134](../vs140/CA2134--Methods-must-keep-consistent-transparency-when-overriding-base-methods.md)|Methods must keep consistent transparency when overriding base methods|  
|[CA2137](../Topic/CA2137:%20Transparent%20methods%20must%20contain%20only%20verifiable%20IL.md)|Transparent methods must contain only verifiable IL|  
|[CA2138](../Topic/CA2138:%20Transparent%20methods%20must%20not%20call%20methods%20with%20the%20SuppressUnmanagedCodeSecurity%20attribute.md)|Transparent methods must not call methods with the SuppressUnmanagedCodeSecurity attribute|  
|[CA2140](../vs140/CA2140--Transparent-code-must-not-reference-security-critical-items.md)|Transparent code must not reference security critical items|  
|[CA2141](../Topic/CA2141:Transparent%20methods%20must%20not%20satisfy%20LinkDemands.md)|Transparent methods must not satisfy LinkDemands|  
|[CA2146](../Topic/CA2146:%20Types%20must%20be%20at%20least%20as%20critical%20as%20their%20base%20types%20and%20interfaces.md)|Types must be at least as critical as their base types and interfaces|  
|[CA2147](../vs140/CA2147--Transparent-methods-may-not-use-security-asserts.md)|Transparent methods may not use security asserts|  
|[CA2149](../Topic/CA2149:%20Transparent%20methods%20must%20not%20call%20into%20native%20code.md)|Transparent methods must not call into native code|  
|[CA2200](../vs140/CA2200--Rethrow-to-preserve-stack-details.md)|Rethrow to preserve stack details|  
|[CA2202](../vs140/CA2202--Do-not-dispose-objects-multiple-times.md)|Do not dispose objects multiple times|  
|[CA2207](../vs140/CA2207--Initialize-value-type-static-fields-inline.md)|Initialize value type static fields inline|  
|[CA2212](../vs140/CA2212--Do-not-mark-serviced-components-with-WebMethod.md)|Do not mark serviced components with WebMethod|  
|[CA2213](../Topic/CA2213:%20Disposable%20fields%20should%20be%20disposed.md)|Disposable fields should be disposed|  
|[CA2214](../vs140/CA2214--Do-not-call-overridable-methods-in-constructors.md)|Do not call overridable methods in constructors|  
|[CA2216](../Topic/CA2216:%20Disposable%20types%20should%20declare%20finalizer.md)|Disposable types should declare finalizer|  
|[CA2220](../Topic/CA2220:%20Finalizers%20should%20call%20base%20class%20finalizer.md)|Finalizers should call base class finalizer|  
|[CA2229](../Topic/CA2229:%20Implement%20serialization%20constructors.md)|Implement serialization constructors|  
|[CA2231](../vs140/CA2231--Overload-operator-equals-on-overriding-ValueType.Equals.md)|Overload operator equals on overriding ValueType.Equals|  
|[CA2232](../Topic/CA2232:%20Mark%20Windows%20Forms%20entry%20points%20with%20STAThread.md)|Mark Windows Forms entry points with STAThread|  
|[CA2235](../Topic/CA2235:%20Mark%20all%20non-serializable%20fields.md)|Mark all non-serializable fields|  
|[CA2236](../Topic/CA2236:%20Call%20base%20class%20methods%20on%20ISerializable%20types.md)|Call base class methods on ISerializable types|  
|[CA2237](../vs140/CA2237--Mark-ISerializable-types-with-SerializableAttribute.md)|Mark ISerializable types with SerializableAttribute|  
|[CA2238](../Topic/CA2238:%20Implement%20serialization%20methods%20correctly.md)|Implement serialization methods correctly|  
|[CA2240](../Topic/CA2240:%20Implement%20ISerializable%20correctly.md)|Implement ISerializable correctly|  
|[CA2241](../Topic/CA2241:%20Provide%20correct%20arguments%20to%20formatting%20methods.md)|Provide correct arguments to formatting methods|  
|[CA2242](../Topic/CA2242:%20Test%20for%20NaN%20correctly.md)|Test for NaN correctly|  
|[CA1008](../vs140/CA1008--Enums-should-have-zero-value.md)|Enums should have zero value|  
|[CA1013](../vs140/CA1013--Overload-operator-equals-on-overloading-add-and-subtract.md)|Overload operator equals on overloading add and subtract|  
|[CA1303](../Topic/CA1303:%20Do%20not%20pass%20literals%20as%20localized%20parameters.md)|Do not pass literals as localized parameters|  
|[CA1308](../vs140/CA1308--Normalize-strings-to-uppercase.md)|Normalize strings to uppercase|  
|[CA1806](../vs140/CA1806--Do-not-ignore-method-results.md)|Do not ignore method results|  
|[CA1816](../Topic/CA1816:%20Call%20GC.SuppressFinalize%20correctly.md)|Call GC.SuppressFinalize correctly|  
|[CA1819](../Topic/CA1819:%20Properties%20should%20not%20return%20arrays.md)|Properties should not return arrays|  
|[CA1820](../Topic/CA1820:%20Test%20for%20empty%20strings%20using%20string%20length.md)|Test for empty strings using string length|  
|[CA1903](../vs140/CA1903--Use-only-API-from-targeted-framework.md)|Use only API from targeted framework|  
|[CA2004](../vs140/CA2004--Remove-calls-to-GC.KeepAlive.md)|Remove calls to GC.KeepAlive|  
|[CA2006](../Topic/CA2006:%20Use%20SafeHandle%20to%20encapsulate%20native%20resources.md)|Use SafeHandle to encapsulate native resources|  
|[CA2102](../Topic/CA2102:%20Catch%20non-CLSCompliant%20exceptions%20in%20general%20handlers.md)|Catch non-CLSCompliant exceptions in general handlers|  
|[CA2104](../Topic/CA2104:%20Do%20not%20declare%20read%20only%20mutable%20reference%20types.md)|Do not declare read only mutable reference types|  
|[CA2105](../Topic/CA2105:%20Array%20fields%20should%20not%20be%20read%20only.md)|Array fields should not be read only|  
|[CA2106](../vs140/CA2106--Secure-asserts.md)|Secure asserts|  
|[CA2115](../Topic/CA2115:%20Call%20GC.KeepAlive%20when%20using%20native%20resources.md)|Call GC.KeepAlive when using native resources|  
|[CA2119](../vs140/CA2119--Seal-methods-that-satisfy-private-interfaces.md)|Seal methods that satisfy private interfaces|  
|[CA2120](../Topic/CA2120:%20Secure%20serialization%20constructors.md)|Secure serialization constructors|  
|[CA2121](../vs140/CA2121--Static-constructors-should-be-private.md)|Static constructors should be private|  
|[CA2130](../Topic/CA2130:%20Security%20critical%20constants%20should%20be%20transparent.md)|Security critical constants should be transparent|  
|[CA2205](../Topic/CA2205:%20Use%20managed%20equivalents%20of%20Win32%20API.md)|Use managed equivalents of Win32 API|  
|[CA2215](../vs140/CA2215--Dispose-methods-should-call-base-class-dispose.md)|Dispose methods should call base class dispose|  
|[CA2221](../vs140/CA2221--Finalizers-should-be-protected.md)|Finalizers should be protected|  
|[CA2222](../vs140/CA2222--Do-not-decrease-inherited-member-visibility.md)|Do not decrease inherited member visibility|  
|[CA2223](../vs140/CA2223--Members-should-differ-by-more-than-return-type.md)|Members should differ by more than return type|  
|[CA2224](../vs140/CA2224--Override-equals-on-overloading-operator-equals.md)|Override equals on overloading operator equals|  
|[CA2226](../vs140/CA2226--Operators-should-have-symmetrical-overloads.md)|Operators should have symmetrical overloads|  
|[CA2227](../Topic/CA2227:%20Collection%20properties%20should%20be%20read%20only.md)|Collection properties should be read only|  
|[CA2239](../Topic/CA2239:%20Provide%20deserialization%20methods%20for%20optional%20fields.md)|Provide deserialization methods for optional fields|