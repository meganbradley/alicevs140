---
title: "Extended Design Guidelines Rules rule set for managed code"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a338caf2-b75d-4f23-a0f9-3024fa0bceac
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Extended Design Guidelines Rules rule set for managed code
The Microsoft Extended Design Guideline Rules rule set expands on the basic design guideline rules to maximize the usability and maintainability issues that are reported. Extra emphasis is placed on naming guidelines. You should consider including this rule set if your project includes library code or if you want to enforce the highest standards for writing code that is easy to maintain.  
  
 The Extended Design Guideline Rules include all of the Microsoft Basic Design Guideline Rules. The Basic Design Guideline Rules include all of the Microsoft Minimum Recommended Rules. For more information, see [Microsoft Basic Design Guideline Rules Code Analysis Rule Set](../vs140/Basic-Design-Guideline-Rules-rule-set-for-managed-code.md) and [Microsoft Minimum Recommended Rules Code Analysis Rule Set](../vs140/Managed-Recommended-Rules-rule-set-for-managed-code.md)  
  
 The following table describes all the rules in the Microsoft Extended Design Guideline Rules rule set.  
  
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
|[CA1000](../vs140/CA1000--Do-not-declare-static-members-on-generic-types.md)|Do not declare static members on generic types|  
|[CA1002](../Topic/CA1002:%20Do%20not%20expose%20generic%20lists.md)|Do not expose generic lists|  
|[CA1003](../Topic/CA1003:%20Use%20generic%20event%20handler%20instances.md)|Use generic event handler instances|  
|[CA1004](../vs140/CA1004--Generic-methods-should-provide-type-parameter.md)|Generic methods should provide type parameter|  
|[CA1005](../vs140/CA1005--Avoid-excessive-parameters-on-generic-types.md)|Avoid excessive parameters on generic types|  
|[CA1006](../vs140/CA1006--Do-not-nest-generic-types-in-member-signatures.md)|Do not nest generic types in member signatures|  
|[CA1007](../Topic/CA1007:%20Use%20generics%20where%20appropriate.md)|Use generics where appropriate|  
|[CA1008](../vs140/CA1008--Enums-should-have-zero-value.md)|Enums should have zero value|  
|[CA1010](../vs140/CA1010--Collections-should-implement-generic-interface.md)|Collections should implement generic interface|  
|[CA1011](../Topic/CA1011:%20Consider%20passing%20base%20types%20as%20parameters.md)|Consider passing base types as parameters|  
|[CA1012](../vs140/CA1012--Abstract-types-should-not-have-constructors.md)|Abstract types should not have constructors|  
|[CA1013](../vs140/CA1013--Overload-operator-equals-on-overloading-add-and-subtract.md)|Overload operator equals on overloading add and subtract|  
|[CA1014](../Topic/CA1014:%20Mark%20assemblies%20with%20CLSCompliantAttribute.md)|Mark assemblies with CLSCompliantAttribute|  
|[CA1017](../Topic/CA1017:%20Mark%20assemblies%20with%20ComVisibleAttribute.md)|Mark assemblies with ComVisibleAttribute|  
|[CA1018](../vs140/CA1018--Mark-attributes-with-AttributeUsageAttribute.md)|Mark attributes with AttributeUsageAttribute|  
|[CA1019](../vs140/CA1019--Define-accessors-for-attribute-arguments.md)|Define accessors for attribute arguments|  
|[CA1023](../vs140/CA1023--Indexers-should-not-be-multidimensional.md)|Indexers should not be multidimensional|  
|[CA1024](../vs140/CA1024--Use-properties-where-appropriate.md)|Use properties where appropriate|  
|[CA1025](../Topic/CA1025:%20Replace%20repetitive%20arguments%20with%20params%20array.md)|Replace repetitive arguments with params array|  
|[CA1026](../vs140/CA1026--Default-parameters-should-not-be-used.md)|Default parameters should not be used|  
|[CA1027](../Topic/CA1027:%20Mark%20enums%20with%20FlagsAttribute.md)|Mark enums with FlagsAttribute|  
|[CA1028](../Topic/CA1028:%20Enum%20storage%20should%20be%20Int32.md)|Enum storage should be Int32|  
|[CA1030](../vs140/CA1030--Use-events-where-appropriate.md)|Use events where appropriate|  
|[CA1031](../Topic/CA1031:%20Do%20not%20catch%20general%20exception%20types.md)|Do not catch general exception types|  
|[CA1032](../vs140/CA1032--Implement-standard-exception-constructors.md)|Implement standard exception constructors|  
|[CA1034](../vs140/CA1034--Nested-types-should-not-be-visible.md)|Nested types should not be visible|  
|[CA1035](../Topic/CA1035:%20ICollection%20implementations%20have%20strongly%20typed%20members.md)|ICollection implementations have strongly typed members|  
|[CA1036](../Topic/CA1036:%20Override%20methods%20on%20comparable%20types.md)|Override methods on comparable types|  
|[CA1038](../vs140/CA1038--Enumerators-should-be-strongly-typed.md)|Enumerators should be strongly typed|  
|[CA1039](../Topic/CA1039:%20Lists%20are%20strongly%20typed.md)|Lists are strongly typed|  
|[CA1041](../vs140/CA1041--Provide-ObsoleteAttribute-message.md)|Provide ObsoleteAttribute message|  
|[CA1043](../vs140/CA1043--Use-integral-or-string-argument-for-indexers.md)|Use integral or string argument for indexers|  
|[CA1044](../vs140/CA1044--Properties-should-not-be-write-only.md)|Properties should not be write only|  
|[CA1046](../vs140/CA1046--Do-not-overload-operator-equals-on-reference-types.md)|Do not overload operator equals on reference types|  
|[CA1047](../vs140/CA1047--Do-not-declare-protected-members-in-sealed-types.md)|Do not declare protected members in sealed types|  
|[CA1048](../vs140/CA1048--Do-not-declare-virtual-members-in-sealed-types.md)|Do not declare virtual members in sealed types|  
|[CA1050](../vs140/CA1050--Declare-types-in-namespaces.md)|Declare types in namespaces|  
|[CA1051](../vs140/CA1051--Do-not-declare-visible-instance-fields.md)|Do not declare visible instance fields|  
|[CA1052](../vs140/CA1052--Static-holder-types-should-be-sealed.md)|Static holder types should be sealed|  
|[CA1053](../vs140/CA1053--Static-holder-types-should-not-have-constructors.md)|Static holder types should not have constructors|  
|[CA1054](../vs140/CA1054--URI-parameters-should-not-be-strings.md)|URI parameters should not be strings|  
|[CA1055](../vs140/CA1055--URI-return-values-should-not-be-strings.md)|URI return values should not be strings|  
|[CA1056](../vs140/CA1056--URI-properties-should-not-be-strings.md)|URI properties should not be strings|  
|[CA1057](../Topic/CA1057:%20String%20URI%20overloads%20call%20System.Uri%20overloads.md)|String URI overloads call System.Uri overloads|  
|[CA1058](../Topic/CA1058:%20Types%20should%20not%20extend%20certain%20base%20types.md)|Types should not extend certain base types|  
|[CA1059](../Topic/CA1059:%20Members%20should%20not%20expose%20certain%20concrete%20types.md)|Members should not expose certain concrete types|  
|[CA1064](../vs140/CA1064--Exceptions-should-be-public.md)|Exceptions should be public|  
|[CA1500](../vs140/CA1500--Variable-names-should-not-match-field-names.md)|Variable names should not match field names|  
|[CA1502](../vs140/CA1502--Avoid-excessive-complexity.md)|Avoid excessive complexity|  
|[CA1708](../vs140/CA1708--Identifiers-should-differ-by-more-than-case.md)|Identifiers should differ by more than case|  
|[CA1716](../vs140/CA1716--Identifiers-should-not-match-keywords.md)|Identifiers should not match keywords|  
|[CA1801](../vs140/CA1801--Review-unused-parameters.md)|Review unused parameters|  
|[CA1804](../vs140/CA1804--Remove-unused-locals.md)|Remove unused locals|  
|[CA1809](../vs140/CA1809--Avoid-excessive-locals.md)|Avoid excessive locals|  
|[CA1810](../vs140/CA1810--Initialize-reference-type-static-fields-inline.md)|Initialize reference type static fields inline|  
|[CA1811](../Topic/CA1811:%20Avoid%20uncalled%20private%20code.md)|Avoid uncalled private code|  
|[CA1812](../Topic/CA1812:%20Avoid%20uninstantiated%20internal%20classes.md)|Avoid uninstantiated internal classes|  
|[CA1813](../Topic/CA1813:%20Avoid%20unsealed%20attributes.md)|Avoid unsealed attributes|  
|[CA1814](../vs140/CA1814--Prefer-jagged-arrays-over-multidimensional.md)|Prefer jagged arrays over multidimensional|  
|[CA1815](../Topic/CA1815:%20Override%20equals%20and%20operator%20equals%20on%20value%20types.md)|Override equals and operator equals on value types|  
|[CA1819](../Topic/CA1819:%20Properties%20should%20not%20return%20arrays.md)|Properties should not return arrays|  
|[CA1820](../Topic/CA1820:%20Test%20for%20empty%20strings%20using%20string%20length.md)|Test for empty strings using string length|  
|[CA1822](../vs140/CA1822--Mark-members-as-static.md)|Mark members as static|  
|[CA1823](../vs140/CA1823--Avoid-unused-private-fields.md)|Avoid unused private fields|  
|[CA2201](../Topic/CA2201:%20Do%20not%20raise%20reserved%20exception%20types.md)|Do not raise reserved exception types|  
|[CA2205](../Topic/CA2205:%20Use%20managed%20equivalents%20of%20Win32%20API.md)|Use managed equivalents of Win32 API|  
|[CA2208](../vs140/CA2208--Instantiate-argument-exceptions-correctly.md)|Instantiate argument exceptions correctly|  
|[CA2211](../vs140/CA2211--Non-constant-fields-should-not-be-visible.md)|Non-constant fields should not be visible|  
|[CA2217](../Topic/CA2217:%20Do%20not%20mark%20enums%20with%20FlagsAttribute.md)|Do not mark enums with FlagsAttribute|  
|[CA2219](../vs140/CA2219--Do-not-raise-exceptions-in-exception-clauses.md)|Do not raise exceptions in exception clauses|  
|[CA2221](../vs140/CA2221--Finalizers-should-be-protected.md)|Finalizers should be protected|  
|[CA2222](../vs140/CA2222--Do-not-decrease-inherited-member-visibility.md)|Do not decrease inherited member visibility|  
|[CA2223](../vs140/CA2223--Members-should-differ-by-more-than-return-type.md)|Members should differ by more than return type|  
|[CA2224](../vs140/CA2224--Override-equals-on-overloading-operator-equals.md)|Override equals on overloading operator equals|  
|[CA2225](../vs140/CA2225--Operator-overloads-have-named-alternates.md)|Operator overloads have named alternates|  
|[CA2226](../vs140/CA2226--Operators-should-have-symmetrical-overloads.md)|Operators should have symmetrical overloads|  
|[CA2227](../Topic/CA2227:%20Collection%20properties%20should%20be%20read%20only.md)|Collection properties should be read only|  
|[CA2230](../Topic/CA2230:%20Use%20params%20for%20variable%20arguments.md)|Use params for variable arguments|  
|[CA2234](../vs140/CA2234--Pass-System.Uri-objects-instead-of-strings.md)|Pass System.Uri objects instead of strings|  
|[CA2239](../Topic/CA2239:%20Provide%20deserialization%20methods%20for%20optional%20fields.md)|Provide deserialization methods for optional fields|  
|[CA1020](../Topic/CA1020:%20Avoid%20namespaces%20with%20few%20types.md)|Avoid namespaces with few types|  
|[CA1021](../Topic/CA1021:%20Avoid%20out%20parameters.md)|Avoid out parameters|  
|[CA1040](../vs140/CA1040--Avoid-empty-interfaces.md)|Avoid empty interfaces|  
|[CA1045](../vs140/CA1045--Do-not-pass-types-by-reference.md)|Do not pass types by reference|  
|[CA1062](../vs140/CA1062--Validate-arguments-of-public-methods.md)|Validate arguments of public methods|  
|[CA1501](../vs140/CA1501--Avoid-excessive-inheritance.md)|Avoid excessive inheritance|  
|[CA1504](../vs140/CA1504--Review-misleading-field-names.md)|Review misleading field names|  
|[CA1505](../vs140/CA1505--Avoid-unmaintainable-code.md)|Avoid unmaintainable code|  
|[CA1506](../vs140/CA1506--Avoid-excessive-class-coupling.md)|Avoid excessive class coupling|  
|[CA1700](../vs140/CA1700--Do-not-name-enum-values--Reserved-.md)|Do not name enum values 'Reserved'|  
|[CA1701](../vs140/CA1701--Resource-string-compound-words-should-be-cased-correctly.md)|Resource string compound words should be cased correctly|  
|[CA1702](../vs140/CA1702--Compound-words-should-be-cased-correctly.md)|Compound words should be cased correctly|  
|[CA1703](../vs140/CA1703--Resource-strings-should-be-spelled-correctly.md)|Resource strings should be spelled correctly|  
|[CA1704](../vs140/CA1704--Identifiers-should-be-spelled-correctly.md)|Identifiers should be spelled correctly|  
|[CA1707](../vs140/CA1707--Identifiers-should-not-contain-underscores.md)|Identifiers should not contain underscores|  
|[CA1709](../vs140/CA1709--Identifiers-should-be-cased-correctly.md)|Identifiers should be cased correctly|  
|[CA1710](../vs140/CA1710--Identifiers-should-have-correct-suffix.md)|Identifiers should have correct suffix|  
|[CA1711](../Topic/CA1711:%20Identifiers%20should%20not%20have%20incorrect%20suffix.md)|Identifiers should not have incorrect suffix|  
|[CA1712](../Topic/CA1712:%20Do%20not%20prefix%20enum%20values%20with%20type%20name.md)|Do not prefix enum values with type name|  
|[CA1713](../vs140/CA1713--Events-should-not-have-before-or-after-prefix.md)|Events should not have before or after prefix|  
|[CA1714](../vs140/CA1714--Flags-enums-should-have-plural-names.md)|Flags enums should have plural names|  
|[CA1715](../vs140/CA1715--Identifiers-should-have-correct-prefix.md)|Identifiers should have correct prefix|  
|[CA1717](../vs140/CA1717--Only-FlagsAttribute-enums-should-have-plural-names.md)|Only FlagsAttribute enums should have plural names|  
|[CA1719](../vs140/CA1719--Parameter-names-should-not-match-member-names.md)|Parameter names should not match member names|  
|[CA1720](../vs140/CA1720--Identifiers-should-not-contain-type-names.md)|Identifiers should not contain type names|  
|[CA1721](../vs140/CA1721--Property-names-should-not-match-get-methods.md)|Property names should not match get methods|  
|[CA1722](../vs140/CA1722--Identifiers-should-not-have-incorrect-prefix.md)|Identifiers should not have incorrect prefix|  
|[CA1724](../vs140/CA1724--Type-Names-Should-Not-Match-Namespaces.md)|Type Names Should Not Match Namespaces|  
|[CA1725](../vs140/CA1725--Parameter-names-should-match-base-declaration.md)|Parameter names should match base declaration|  
|[CA1726](../vs140/CA1726--Use-preferred-terms.md)|Use preferred terms|  
|[CA2204](../Topic/CA2204:%20Literals%20should%20be%20spelled%20correctly.md)|Literals should be spelled correctly|