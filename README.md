# MongoDB $inc operator error with string value
This example demonstrates an uncommon error when using the `$inc` operator in MongoDB update queries. The error occurs when providing a string value instead of a numeric value to increment the field. The correct usage involves passing an integer, not a string.

## Bug
The bug is in the `updateOne` method call where the `$inc` operator is used with a string value.  This will cause MongoDB to throw an error because it expects a numeric value to increment the field.

## Solution
The solution is to change the value passed to the `$inc` operator to an integer value. 
