# Unexpected Behavior When Directly Modifying Instance Variables in Ruby

This repository demonstrates a subtle bug in Ruby related to directly modifying instance variables using `instance_variable_set`.

## The Problem

Directly manipulating instance variables using methods like `instance_variable_set` and `instance_variable_get` can bypass the intended encapsulation of a class. This makes debugging and maintaining code more difficult and can lead to unexpected behavior because class invariants may be violated.

The provided example shows how modifying an instance variable directly can lead to values deviating from what might be expected based on the class's public interface.

## Solution

The recommended approach is to always use accessor methods (getters and setters) to interact with instance variables.  This ensures controlled access and modification, preserving data integrity and improving code maintainability.  This approach also promotes better encapsulation and facilitates the implementation of validation or other logic within the setter method.