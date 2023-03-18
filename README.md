# LuaPlus Module (class) Documentation

The LuaPlus module (class) provides a simple and easy-to-use class system for Lua, allowing you to create and inherit classes. This document explains how to use the module in your projects.

## Table of Contents

- [Installation](#installation)
- [Creating a Class](#creating-a-class)
- [Inheriting from a Class](#inheriting-from-a-class)
- [Initialization](#initialization)
- [Defining Methods](#defining-methods)

## Installation

1. Create a new Script in the `ServerScriptService` and name it `LuaPlus`.
2. Copy the contents of the `LuaPlus.lua` script provided above into the new Script.
3. Save the script.

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
    `self.arg2 = arg2
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
