## `AzureStorageExtensions`

Simple Azure Storage Extensions
```csharp
public static class ArJaiSolutions.ExtensionLibrary.AzureStorageExtensions

```

Static Methods

| Type | Name | Summary | 
| --- | --- | --- | 
| `String` | EscapeKeyString(this `String` keyStringToEscape) | Escapes a key string ensuring that is does not contain any characters not allowed in table storage key fields. | 
| `Task<T>` | TimedTask(this `Task<T>` task, `String` taskName, `Action<String>` logger, `Boolean` logTimings = True) | Logs the time taken to complete the task  By Default the It will log as Information log unless you in Debug Mode.  You can switch off the logging by setting <i>logTimings</i> to false. | 
| `String` | ToSafeContainerName(this `String` containerName) | Cleans the string to match the container naming conventions | 
| `String` | ToSafeTableName(this `String` tableName) | Cleans the string to match the table storage naming conventions | 
| `String` | UnescapeKeyString(this `String` keyStringToUnescape) | Unescapes a key string that was previously escaped by a call to [ArJaiSolutions.ExtensionLibrary.AzureStorageExtensions.EscapeKeyString(System.String)](ArJaiSolutions.ExtensionLibrary.AzureStorageExtensions.EscapeKeyString(System#string)). | 


## `CompareAndUpdateObjects`

To compare any objects and update the target object properties  from values from the source properties
```csharp
public class ArJaiSolutions.ExtensionLibrary.CompareAndUpdateObjects

```

Methods

| Type | Name | Summary | 
| --- | --- | --- | 
| `Object` | CompareAndUpdate(`Object` targetObject, `Object` sourceObject) | Compare the targetObject properties with the sourceObject properties  and copies the value from source into the target. | 


## `DictionaryExtensions`

Dictionary Extensions for easy Dictionary actions
```csharp
public static class ArJaiSolutions.ExtensionLibrary.DictionaryExtensions

```

Static Methods

| Type | Name | Summary | 
| --- | --- | --- | 
| `TValue` | TryReturnValue(this `IDictionary<TKey, TValue>` dictionary, `TKey` key, `TValue` defaultValue = null) | To fetch the value directly from the dictionary for the provided key.  else return the default value | 


## `EnumerableExtensionscs`

Extensions for Enumerable Objects
```csharp
public static class ArJaiSolutions.ExtensionLibrary.EnumerableExtensionscs

```

Static Methods

| Type | Name | Summary | 
| --- | --- | --- | 
| `IEnumerable<IEnumerable<TSource>>` | Batch(this `IEnumerable<TSource>` source, `Int32` size) | Batches the source sequence into sized buckets. | 
| `IEnumerable<TResult>` | Batch(this `IEnumerable<TSource>` source, `Int32` size, `Func<IEnumerable<TSource>, TResult>` resultSelector) | Batches the source sequence into sized buckets. | 


## `Expressions`

Expressions Enum
```csharp
public enum ArJaiSolutions.ExtensionLibrary.Expressions
    : Enum, IComparable, IFormattable, IConvertible

```

Enum

| Value | Name | Summary | 
| --- | --- | --- | 
| `0` | And | 'And' Expression, like <i>'Expression.And'</i> | 
| `1` | Or | 'Or' Expression, like <i>'Expression.Or'</i> | 


## `HttpRequestHeadersExtensions`

Http Request Header Extensions for easy conversions actions
```csharp
public static class ArJaiSolutions.ExtensionLibrary.HttpRequestHeadersExtensions

```

Static Methods

| Type | Name | Summary | 
| --- | --- | --- | 
| `HttpRequestHeaders` | WithBearerAuthorizationHeader(this `HttpRequestHeaders` request, `String` token) | Adds the bearer token to the Authorisation token | 


## `HttpResponseMessageExtensions`

Extensions for HttpResponseMessage object
```csharp
public static class ArJaiSolutions.ExtensionLibrary.HttpResponseMessageExtensions

```

Static Methods

| Type | Name | Summary | 
| --- | --- | --- | 
| `Task<T>` | Deserialize(this `HttpResponseMessage` httpResponseMessage) | To deserialze into an object from HttpResponseMessage | 


## `ObjectExtensions`

Convert Object to corresponding Type
```csharp
public static class ArJaiSolutions.ExtensionLibrary.ObjectExtensions

```

Static Methods

| Type | Name | Summary | 
| --- | --- | --- | 
| `Object` | ConvertToTheGivenType(this `Object` objectVariable, `Type` type) | Converts the object provided to the given type  -&gt; Except:  DateTime - Which is converted to UTCDateTime  , bool     - Which is converted to bool from  (true/false, 0/1, yes/no, y/n) | 
| `T` | ConvertToType(this `Object` objectVariable) | Converts the object provided to the given type T        /// | 
| `StringContent` | EncodeForPost(this `Object` objectToEncode, `Encoding` encoding, `String` mediaType) | To serialise an object using encoding and the media type provided it into a string content for Post Data | 
| `StringContent` | EncodeForPostAsJson(this `Object` objectToEncode) | To serialise an object using UTF8 and json mediatype into a string content for Post Data | 
| `Boolean` | ToBool(this `Object` boolObject, `Boolean` defaultValue = False) | Converts object to bool  if not able to convert, It will return the defaultbool provided or false.  Possible values from string to bool are  true/false, 0/1,yes/no, y/n | 
| `Nullable<Boolean>` | ToBool(this `Object` boolObject) | Converts object to bool  if not able to convert, It will return the defaultbool provided or false.  Possible values from string to bool are  true/false, 0/1,yes/no, y/n | 
| `Double` | ToDouble(this `Object` number, `Double` defaultNumber = 0) | Converts this object to double  if unable to convert it returns the defaultnumber Or 0.0 (if no default provided) | 
| `Nullable<Double>` | ToDouble(this `Object` number) | Converts this object to double  if unable to convert it returns the defaultnumber Or 0.0 (if no default provided) | 
| `T` | ToEnum(this `Object` value) | Converts object to any Enum of the Type "T" | 
| `T` | ToEnum(this `Object` value, `T` defaultValue) | Converts object to any Enum of the Type "T" | 
| `Int32` | ToInt(this `Object` number, `Int32` defaultNumber = 0) | Converts this object to int  if unable to convert it returns the defaultnumber Or 0 (if no default provided) | 
| `Nullable<Int32>` | ToInt(this `Object` number) | Converts this object to int  if unable to convert it returns the defaultnumber Or 0 (if no default provided) | 
| `Int64` | Tolong(this `Object` number, `Int64` defaultNumber = 0) | Converts this object to long  if unable to convert it returns the defaultnumber Or 0 (if no default provided) | 
| `Nullable<Int64>` | Tolong(this `Object` number) | Converts this object to long  if unable to convert it returns the defaultnumber Or 0 (if no default provided) | 


## `PreadicateConditions`

Preadicate Expressiong Conditions
```csharp
public enum ArJaiSolutions.ExtensionLibrary.PreadicateConditions
    : Enum, IComparable, IFormattable, IConvertible

```

Enum

| Value | Name | Summary | 
| --- | --- | --- | 
| `0` | Equals | Equals (=) | 
| `1` | NotEqual | Equals (!=) | 
| `2` | Contains | Contains as in Type.Contains() | 
| `3` | GreaterThan | GreaterThan (&gt;) | 
| `4` | GreaterThanOrEqual | GreaterThanOrEqual (&gt;=) | 
| `5` | LessThan | LessThan (&lt;) | 
| `6` | LessThanOrEqual | LessThan (=&lt;) | 
| `7` | StartsWith | StartsWith like Type.StartsWith() | 
| `8` | EndsWith | EndsWith like Type.EndsWith() | 


## `QueryableExtensions`

IQueryable Extensions to create Expressions
```csharp
public static class ArJaiSolutions.ExtensionLibrary.QueryableExtensions

```

Static Methods

| Type | Name | Summary | 
| --- | --- | --- | 
| `Expression` | Equal(`Expression` property, `Expression` target) | Returns the Expression of "Equal" for the source based on the property and target  an example of what is build and returned  e.g.  (parameter =&gt; parameter.property==target) where paramter is of the type source | 
| `Expression` | GetNavigationPropertyExpression(`Expression` parameter, `PreadicateConditions` preadicate, `Object` targetObjectValue, `String[]` properties) | Creates an expression for the property in the path provided.  You could have an expression created for asub properties child property  e.g. object school has a property of students and you want to get a expression  where students have their firstname started with 'A'  you need to call this method with expression parameter which means x=&gt;  which you can make by doing Expression.Paramter(type(ParentElement),"x") (in our case parent element is school)  once you have a parameter set up then call  GetNavigationPropertyExpression(parameter,preadicatecondition.condition, "A","students","firstname"); | 
| `Expression` | GetNavigationPropertyMultipleExpressions(`Expression` parameter, `PreadicateConditions[]` preadicate, `Expressions[]` expressions, `Object[]` targetObjectValue, `String[]` properties) | Creates an expression for the property in the path provided.  You could have an expression created for asub properties child property.  <br /><br />  e.g. object school has a property of students and you want to get a expression  where students have their Firstname started with 'A'  <br />  and the Lastname started with 'T'  <br />  and is Active equals 'true'  <br />  you need to call this method with expression parameter which means x=&gt;  <br />  which you can make by doing Expression.Paramter(type(ParentElement),"x") (in our case parent element is school)  once you have a parameter set up then call  <code>  GetNavigationPropertyExpression(parameter, new []{PreadicateConditions.startsWith, PreadicateConditions.startsWith, PreadicateConditions.Equals}  , new []{Expressions.And, Expressions.And}, new[]{"A","T",true}, new []{"students","Firstname,Lastname,Active"});  </code> | 
| `Expression` | GreaterThan(`Expression` property, `Expression` target) | Returns the Expression of "GreaterThan" for the source based on the property and target  an example of what is build and returned  e.g.  (parameter =&gt; parameter.property&gt;target) where paramter is of the type source | 
| `Expression` | GreaterThanOrEqualTo(`Expression` property, `Expression` target, `Boolean` inclusive = True) | Returns the Expression of "GreaterThan" for the source based on the property and target  an example of what is build and returned  e.g.  (parameter =&gt; parameter.property&gt;=target) where paramter is of the type source | 
| `Expression` | LessThan(`Expression` property, `Expression` target) | Returns the Expression of "LessThan" for the source based on the property and target  an example of what is build and returned  e.g.  (parameter =&gt; parameter.property&lt;target) where paramter is of the type source | 
| `Expression` | LessThanOrEqualTo(`Expression` property, `Expression` target, `Boolean` inclusive = True) | Returns the Expression of "LessThanOrEqual" for the source based on the property and target  an example of what is build and returned  e.g.  (parameter =&gt; parameter.property=&lt;target) where paramter is of the type source | 
| `Expression` | MakePreadicateCondition(`PreadicateConditions` condition, `Expression` left, `Expression` right) | this method makes an Expression for Preadicate Condition. | 
| `Expression` | NotEqual(`Expression` property, `Expression` target) | Returns the Expression of "NotEqual" for the source based on the property and target  an example of what is build and returned  e.g.  (parameter =&gt; parameter.property!=target) where paramter is of the type source | 
| `IQueryable<TSource>` | PreadicateConditionBasedFiltering(this `IQueryable<TSource>` source, `String` propertyName, `PreadicateConditions` condition, `Object` input) | To create expression for a source with the property and input value based on the condition provided    /*Exceptions*/    ArgumentOutOfRangeException if the input value is not been able to convert to the same type of the property | 
| `Expression` | PreadicateConditionExpression(this `IQueryable<TSource>` source, `ParameterExpression` parameter, `String` propertyName, `PreadicateConditions` condition, `Object` input) | To create expression for a source with the property and input value based on the condition provided    /*Exceptions*/    ArgumentOutOfRangeException if the input value is not been able to convert to the same type of the property | 


## `StringExtensions`

string Extensions for easy conversions actions
```csharp
public static class ArJaiSolutions.ExtensionLibrary.StringExtensions

```

Static Methods

| Type | Name | Summary | 
| --- | --- | --- | 
| `String` | RemoveAllWhiteSpaces(this `String` s) | Remove all white spaces from the string value | 
| `String` | SubstituteValuesFromtheDictionary(this `String` inputString, `IDictionary<String, String>` parameters, `Char` substituteStartChar, `Char` substituteEndChar) | Substitutes the values in the dictionary in the string  <br>eg:</br><br>we have string -&gt; "this is Yeterdays date is {yesterdaydate} and todays date {todaydate}"</br><code>var st = "this is todays {date}";</code><code>var param = new Dictionary&lt;string, string&gt;{{"yesterdaydate", DateTime.UtcNow.AddDay(-1).Date.ToString()}  ,{"todaydate", DateTime.UtcNow.Date.ToString()}};</code><code>var substitutedstring = st.SubstituteValuesFromtheDictionary(param,'{','}');</code> | 
| `Boolean` | ToBool(this `String` boolString, `Boolean` defaultValue = False) | Converts string to bool  if not able to convert, It will return the defaultbool provided or false.  Possible values from string to bool are  true/false, 0/1,yes/no, y/n | 
| `Nullable<Boolean>` | ToBool(this `String` boolString) | Converts string to bool  if not able to convert, It will return the defaultbool provided or false.  Possible values from string to bool are  true/false, 0/1,yes/no, y/n | 
| `Nullable<DateTime>` | ToDateTime(this `String` s, `String` format = ddMMyyyy, `String` cultureString = en-GB) | Converts the given string to Datetime based on the format and culture provided  or by Default the format is "ddMMyyyy" and culture is "en-GB" | 
| `Nullable<DateTime>` | ToDateTime(this `String` s, `String` format, `CultureInfo` culture) | Converts the given string to Datetime based on the format and culture provided  or by Default the format is "ddMMyyyy" and culture is "en-GB" | 
| `Decimal` | ToDecimal(this `String` decimalString) | Convert the provided Decimal string into a decimal value | 
| `Double` | ToDouble(this `String` number, `Double` defaultNumber = 0) | Converts this string to double  if unable to convert it returnsthe defaultnumber Or 0.0 (if no default provided) | 
| `Nullable<Double>` | ToDouble(this `String` number) | Converts this string to double  if unable to convert it returnsthe defaultnumber Or 0.0 (if no default provided) | 
| `T` | ToEnum(this `String` value) | Converts string to any Enum of the Type "T" | 
| `T` | ToEnum(this `String` value, `T` defaultValue) | Converts string to any Enum of the Type "T" | 
| `Nullable<Guid>` | ToGuid(this `String` guidString, `String` guidFormat = D) | Converts Given string and guid Formats  Default guidFormat ='D'  Guid Formats can be - "N","D","B","P","X" | 
| `Int32` | ToInt(this `String` number, `Int32` defaultNumber = 0) | Converts this string to int  if unable to convert it returnsthe defaultnumber Or 0 (if no default provided) | 
| `Nullable<Int32>` | ToInt(this `String` number) | Converts this string to int  if unable to convert it returnsthe defaultnumber Or 0 (if no default provided) | 
| `Int64` | Tolong(this `String` number, `Int64` defaultNumber = 0) | Converts this string to long  if unable to convert it returnsthe defaultnumber Or 0 (if no default provided) | 
| `Nullable<Int64>` | Tolong(this `String` number) | Converts this string to long  if unable to convert it returnsthe defaultnumber Or 0 (if no default provided) | 
| `String` | ToTitleCase(this `String` s) | Convert the provided string into a TitleCase string | 
| `Nullable<DateTime>` | ToUTCDateTime(this `String` s) | Converts the given string to UTCDatetime | 
| `Nullable<DateTime>` | ToUTCDateTimeExact(this `String` s) | Converts the given string to UTCDatetimeExact | 


