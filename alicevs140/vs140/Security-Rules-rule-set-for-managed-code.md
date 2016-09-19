---
title: "Security Rules rule set for managed code"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 564aeac6-03fa-41b0-b655-88179f0ab01b
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Security Rules rule set for managed code
You should include the Microsoft Security Rules rule set to maximize the number of potential security issues that are reported.  
  
|Rule|Description|  
|----------|-----------------|  
|[CA2100](../vs140/CA2100--Review-SQL-queries-for-security-vulnerabilities.md)|Review SQL queries for security vulnerabilities|  
|[CA2102](../Topic/CA2102:%20Catch%20non-CLSCompliant%20exceptions%20in%20general%20handlers.md)|Catch non-CLSCompliant exceptions in general handlers|  
|[CA2103](../vs140/CA2103--Review-imperative-security.md)|Review imperative security|  
|[CA2104](../Topic/CA2104:%20Do%20not%20declare%20read%20only%20mutable%20reference%20types.md)|Do not declare read only mutable reference types|  
|[CA2105](../Topic/CA2105:%20Array%20fields%20should%20not%20be%20read%20only.md)|Array fields should not be read only|  
|[CA2106](../vs140/CA2106--Secure-asserts.md)|Secure asserts|  
|[CA2107](../vs140/CA2107--Review-deny-and-permit-only-usage.md)|Review deny and permit only usage|  
|[CA2108](../vs140/CA2108--Review-declarative-security-on-value-types.md)|Review declarative security on value types|  
|[CA2109](../Topic/CA2109:%20Review%20visible%20event%20handlers.md)|Review visible event handlers|  
|[CA2111](../Topic/CA2111:%20Pointers%20should%20not%20be%20visible.md)|Pointers should not be visible|  
|[CA2112](../vs140/CA2112--Secured-types-should-not-expose-fields.md)|Secured types should not expose fields|  
|[CA2114](../vs140/CA2114--Method-security-should-be-a-superset-of-type.md)|Method security should be a superset of type|  
|[CA2115](../Topic/CA2115:%20Call%20GC.KeepAlive%20when%20using%20native%20resources.md)|Call GC.KeepAlive when using native resources|  
|[CA2116](../vs140/CA2116--APTCA-methods-should-only-call-APTCA-methods.md)|APTCA methods should only call APTCA methods|  
|[CA2117](../Topic/CA2117:%20APTCA%20types%20should%20only%20extend%20APTCA%20base%20types.md)|APTCA types should only extend APTCA base types|  
|[CA2118](../vs140/CA2118--Review-SuppressUnmanagedCodeSecurityAttribute-usage.md)|Review SuppressUnmanagedCodeSecurityAttribute usage|  
|[CA2119](../vs140/CA2119--Seal-methods-that-satisfy-private-interfaces.md)|Seal methods that satisfy private interfaces|  
|[CA2120](../Topic/CA2120:%20Secure%20serialization%20constructors.md)|Secure serialization constructors|  
|[CA2121](../vs140/CA2121--Static-constructors-should-be-private.md)|Static constructors should be private|  
|[CA2122](../vs140/CA2122--Do-not-indirectly-expose-methods-with-link-demands.md)|Do not indirectly expose methods with link demands|  
|[CA2123](../vs140/CA2123--Override-link-demands-should-be-identical-to-base.md)|Override link demands should be identical to base|  
|[CA2124](../vs140/CA2124--Wrap-vulnerable-finally-clauses-in-outer-try.md)|Wrap vulnerable finally clauses in outer try|  
|[CA2126](../vs140/CA2126--Type-link-demands-require-inheritance-demands.md)|Type link demands require inheritance demands|  
|[CA2130](../Topic/CA2130:%20Security%20critical%20constants%20should%20be%20transparent.md)|Security critical constants should be transparent|  
|[CA2131](../vs140/CA2131--Security-critical-types-may-not-participate-in-type-equivalence.md)|Security critical types may not participate in type equivalence|  
|[CA2132](../Topic/CA2132:%20Default%20constructors%20must%20be%20at%20least%20as%20critical%20as%20base%20type%20default%20constructors.md)|Default constructors must be at least as critical as base type default constructors|  
|[CA2133](../vs140/CA2133--Delegates-must-bind-to-methods-with-consistent-transparency.md)|Delegates must bind to methods with consistent transparency|  
|[CA2134](../vs140/CA2134--Methods-must-keep-consistent-transparency-when-overriding-base-methods.md)|Methods must keep consistent transparency when overriding base methods|  
|[CA2135](../vs140/CA2135--Level-2-assemblies-should-not-contain-LinkDemands.md)|Level 2 assemblies should not contain LinkDemands|  
|[CA2136](../vs140/CA2136--Members-should-not-have-conflicting-transparency-annotations.md)|Members should not have conflicting transparency annotations|  
|[CA2137](../Topic/CA2137:%20Transparent%20methods%20must%20contain%20only%20verifiable%20IL.md)|Transparent methods must contain only verifiable IL|  
|[CA2138](../Topic/CA2138:%20Transparent%20methods%20must%20not%20call%20methods%20with%20the%20SuppressUnmanagedCodeSecurity%20attribute.md)|Transparent methods must not call methods with the SuppressUnmanagedCodeSecurity attribute|  
|[CA2139](../vs140/CA2139--Transparent-methods-may-not-use-the-HandleProcessCorruptingExceptions-attribute.md)|Transparent methods may not use the HandleProcessCorruptingExceptions attribute|  
|[CA2140](../vs140/CA2140--Transparent-code-must-not-reference-security-critical-items.md)|Transparent code must not reference security critical items|  
|[CA2141](../Topic/CA2141:Transparent%20methods%20must%20not%20satisfy%20LinkDemands.md)|Transparent methods must not satisfy LinkDemands|  
|[CA2142](../vs140/CA2142--Transparent-code-should-not-be-protected-with-LinkDemands.md)|Transparent code should not be protected with LinkDemands|  
|[CA2143](../vs140/CA2143--Transparent-methods-should-not-use-security-demands.md)|Transparent methods should not use security demands|  
|[CA2144](../Topic/CA2144:%20Transparent%20code%20should%20not%20load%20assemblies%20from%20byte%20arrays.md)|Transparent code should not load assemblies from byte arrays|  
|[CA2145](../vs140/CA2145--Transparent-methods-should-not-be-decorated-with-the-SuppressUnmanagedCodeSecurityAttribute.md)|Transparent methods should not be decorated with the SuppressUnmanagedCodeSecurityAttribute|  
|[CA2146](../Topic/CA2146:%20Types%20must%20be%20at%20least%20as%20critical%20as%20their%20base%20types%20and%20interfaces.md)|Types must be at least as critical as their base types and interfaces|  
|[CA2147](../vs140/CA2147--Transparent-methods-may-not-use-security-asserts.md)|Transparent methods may not use security asserts|  
|[CA2149](../Topic/CA2149:%20Transparent%20methods%20must%20not%20call%20into%20native%20code.md)|Transparent methods must not call into native code|  
|[CA2210](../Topic/CA2210:%20Assemblies%20should%20have%20valid%20strong%20names.md)|Assemblies should have valid strong names|