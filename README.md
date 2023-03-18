# LuaPlus Module (class) Documentation

The LuaPlus module (class) provides a simple and easy-to-use class system for Lua, allowing you to create and inherit classes. This document explains how to use the module in your projects.

## Table of Contents

- [FindInstance](#findinstance)
- [GetDistance](#getdistance)
- [IsPlayerInRange](#isplayerinrange)
- [CreateBillboardGUI](#createbillboardgui)
- [DealDamage](#dealdamage)
- [FormatTime](#formattime)
- [Lerp](#lerp)
- [Tween](#tween)
- [IsCharacterOnGround](#ischaracteronground)
- [CloneToParent](#clonetoparent)
- [Installation](#installation)
- [Creating a Class](#creating-a-class)
- [Inheriting from a Class](#inheriting-from-a-class)
- [Initialization](#initialization)
- [Defining Methods](#defining-methods)

## Installation

1. Create a new Script in the `ServerScriptService` and name it `LuaPlus`.
2. Copy the contents of the `LuaPlus.lua` script provided above into the new Script.
3. Save the script.

## FindInstance

`LuaPlus:FindInstance(instanceType, parent)`

Finds an instance of a specific type within a parent instance.

**Parameters:**

- `instanceType` (string): The class name of the instance type you want to find.
- `parent` (Instance): The parent instance to search in.

**Returns:**

- (Instance) The first instance of the specified type found within the parent.

## GetDistance

`LuaPlus:GetDistance(position1, position2)`

Calculates the distance between two Vector3 positions.

**Parameters:**

- `position1` (Vector3): The first position.
- `position2` (Vector3): The second position.

**Returns:**

- (number) The distance between the two positions.

## IsPlayerInRange

`LuaPlus:IsPlayerInRange(player, position, range)`

Checks if a player is within a specific range of a position.

**Parameters:**

- `player` (Player): The player to check.
- `position` (Vector3): The position to check the range from.
- `range` (number): The range in studs.

**Returns:**

- (boolean) `true` if the player is within the specified range, `false` otherwise.

## CreateBillboardGUI

`LuaPlus:CreateBillboardGUI(text, object, size)`

Creates a Billboard GUI for an object.

**Parameters:**

- `text` (string): The text to display on the Billboard GUI.
- `object` (BasePart): The object to attach the Billboard GUI to.
- `size` (number): The size of the Billboard GUI.

**Returns:**

- (BillboardGui) The created Billboard GUI.

## DealDamage

`LuaPlus:DealDamage(character, damage)`

Deals damage to a character.

**Parameters:**

- `character` (Model): The character to deal damage to.
- `damage` (number): The amount of damage to deal.

## FormatTime

`LuaPlus:FormatTime(seconds)`

Converts seconds to a formatted time string.

**Parameters:**

- `seconds` (number): The number of seconds to format.

**Returns:**

- (string) The formatted time string in the format "MM:SS".

## Lerp

`LuaPlus:Lerp(a, b, alpha)`

Linearly interpolates between two values.

**Parameters:**

- `a` (number): The starting value.
- `b` (number): The ending value.
- `alpha` (number): The interpolation factor, where 0 represents the starting value and 1 represents the ending value.

**Returns:**

- (number) The interpolated value.

## Creating a Class

To create a new class, use the `LuaPlus.CreateClass(base)` function, where `base` is an optional base class to inherit from. If you don't want to inherit from any class, simply call the function without any arguments.

```lua
local LuaPlus = require(game.ServerScriptService.LuaPlus)
local MyClass = LuaPlus.CreateClass()
```

## Inheriting from a Class

To inherit from a base class, pass the base class as an argument when creating the new class.

```lua
local LuaPlus = require(game.ServerScriptService.LuaPlus)
local MyBaseClass = LuaPlus.CreateClass()
local MyDerivedClass = LuaPlus.CreateClass(MyBaseClass)
```

## Initialization

To initialize a class, define an `init` method inside the class. The `init` method will be called automatically when you create a new instance of the class. You can pass any number of arguments to the `init` method.
```lua
local MyClass = LuaPlus.CreateClass()
function MyClass:init(arg1, arg2)
    self.arg1 = arg1
    self.arg2 = arg2
end
```


## Defining Methods

To define a method for a class, create a new function inside the class using the following syntax:
```lua
function ClassName:methodName(args)
    -- Your code here
end
```

Here's an example:
```lua
local MyClass = LuaPlus.CreateClass()

function MyClass:sayHello()
    print("Hello, World!")
end
```

To call a method on an instance of a class, use the following syntax:
```lua
local myInstance = MyClass:new()
myInstance:sayHello()
```

Now you have all the information needed to use the LuaPlus module to create and inherit classes in your Lua projects.
