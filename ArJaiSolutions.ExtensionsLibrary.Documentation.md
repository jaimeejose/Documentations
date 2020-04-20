
# ArJaiSolutions Extension Library

***ArJaiSolutions*** extension library contains some basic extensions for string, Objects and Mainly extension for Iquerable to create dynamic expressions.


## Dictionary Extensions
    DictionaryExtensions.TryReturnValue<TKey, TValue>(System.Collections.Generic.IDictionary<TKey, TValue>, TKey, TValue)
   To fetch the value directly from the dictionary for the provided key. else return the default value

## String Extensions

    string.ToBool()

Converts string to bool if not able to convert, It will return null. Possible values from string to bool are true/false, 0/1,yes/no, y/n.

    string.ToBool(bool)
Converts string to bool if not able to convert, It will return the default value provided or false. Possible values from string to bool are true/false, 0/1,yes/no, y/n

    string.ToDateTime(string, string)
Converts the given string to Datetime based on the format and culture provided or by Default the format is "ddMMyyyy" and culture is "en-GB"

    string.ToDateTime(string, System.Globalization.CultureInfo)
Converts the given string to Datetime based on the format and culture provided

    string.ToGuid(string)
Converts Given string and guid formats default guid format ='D' Guid formats can be - "N","D","B","P","X"

    string.ToInt()
Converts this string to int if unable to convert it returns null

    string.ToInt(int)
Converts this string to int if unable to convert it returns the default number Or 0 (if no default provided)

    string.Tolong()
Converts this string to long if unable to convert it returns null

    string.Tolong(long)
Converts this string to long if unable to convert it returns the default number Or 0 (if no default provided)

    string.ToUTCDateTime()
Converts the given string to UTCDatetime

    string.ToEnum<T>()
Converts string to any Enum of the Type "T"

    string.ToEnum<T>(T defaultValue)
Converts string to any Enum of the Type "T", with an default value of the Enum

## Object Extensions

    Object.ConvertToTheGivenType(System.Type)
Converts the object provided to the given type -> Except: DateTime - Which is converted to UTCDateTime , bool - Which is converted to bool from (true/false, 0/1, yes/no, y/n)

 string.ToBool()

Converts string to bool if not able to convert, It will return null. Possible values from string to bool are true/false, 0/1,yes/no, y/n.

    string.ToBool(bool)
Converts string to bool if not able to convert, It will return the default value provided or false. Possible values from string to bool are true/false, 0/1,yes/no, y/n

    string.ToInt()
Converts this string to int if unable to convert it returns null

    string.ToInt(int)
Converts this string to int if unable to convert it returns the default number Or 0 (if no default provided)

    string.Tolong()
Converts this string to long if unable to convert it returns null

    string.Tolong(long)
Converts this string to long if unable to convert it returns the default number Or 0 (if no default provided)

## Queryable Extensions
    IQueryable.PreadicateConditionBasedFiltering<TSource>(System.Linq.IQueryable<TSource>, string, ExtensionLibrary.PreadicateConditions, object)
To create expression for a source with the property and input value based on the condition provided 
> **Exceptions:**  **"ArgumentOutOfRangeException"** if the input value is not been able to convert to the same type of the property

    QueryableExtensions.GetNavigationPropertyExpression(System.Linq.Expressions.Expression, ExtensionLibrary.PreadicateConditions, object, string[])
Creates an expression for the property in the path provided. You could have an expression created for a sub properties child property 
e.g. object **school** has a property of **students** and you want to get a expression where students have their **firstname** started with 'A',
 you need to call this method with expression parameter which means *x=>* which you can make by doing *Expression.Paramter(type(ParentElement),"x")* (in our case parent element is school) once you have a parameter set up then call 
 ***GetNavigationPropertyExpression(parameter,preadicatecondition.condition, "A","students","firstname");***

## Helpers for Queryable Expression building

    QueryableExtensions.GreaterThan<TSource>(System.Linq.IQueryable<TSource>, System.Linq.Expressions.ParameterExpression, System.Linq.Expressions.Expression, System.Linq.Expressions.Expression)
Returns the Expression of "GreaterThan" for the source based on the property and target an example of what is build and returned e.g. (parameter => parameter.property>target) where parameter is of the type source

    QueryableExtensions.GreaterThanOrEqualTo<TSource>(System.Linq.IQueryable<TSource>, System.Linq.Expressions.ParameterExpression, System.Linq.Expressions.Expression, System.Linq.Expressions.Expression, bool)
Returns the Expression of "GreaterThan" for the source based on the property and target an example of what is build and returned e.g. (parameter => parameter.property>=target) where parameter is of the type source

    QueryableExtensions.LessThan<TSource>(System.Linq.IQueryable<TSource>, System.Linq.Expressions.ParameterExpression, System.Linq.Expressions.Expression, System.Linq.Expressions.Expression)
Returns the Expression of "LessThan" for the source based on the property and target an example of what is build and returned e.g. (parameter => parameter.property<target) where parameter is of the type source

    QueryableExtensions.LessThanOrEqualTo<TSource>(System.Linq.IQueryable<TSource>, System.Linq.Expressions.ParameterExpression, System.Linq.Expressions.Expression, System.Linq.Expressions.Expression, bool)
Returns the Expression of "LessThanOrEqual" for the source based on the property and target an example of what is build and returned e.g. (parameter => parameter.property=<target) where parameter is of the type source

    QueryableExtensions.NotEqual<TSource>(System.Linq.IQueryable<TSource>, System.Linq.Expressions.ParameterExpression, System.Linq.Expressions.Expression, System.Linq.Expressions.Expression)
Returns the Expression of "NotEqual" for the source based on the property and target an example of what is build and returned e.g. (parameter => parameter.property!=target) where paramter is of the type source

    QueryableExtensions.MakePreadicateCondition(ExtensionLibrary.PreadicateConditions, System.Linq.Expressions.Expression, System.Linq.Expressions.Expression)
this method makes an Expression for Preadicate Condition.


### Preadicate conditions Enum
/// Equals (=)
Equals,

/// Equals (!=)
NotEqual,

/// Contains as in Type.Contains()
Contains,

/// GreaterThan (>)
GreaterThan,

/// GreaterThanOrEqual (>=)
GreaterThanOrEqual,

/// LessThan (&lt;)
LessThan,

/// LessThan (=&lt;)
LessThanOrEqual,

/// StartsWith like Type.StartsWith()
StartsWith,

/// EndsWith like Type.EndsWith()
EndsWith
