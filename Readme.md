# PriorityQueue for Unity C#

A Unity-compatible port of the official .NET `PriorityQueue` implementation.

This repository provides a script adapted from the official .NET library so it can be used in Unity projects, while preserving the original API style as closely as possible.

**.NET official syntax compatible**  
**Updated for C# 13 compatibility**

---

## Overview

Depending on the Unity version and runtime environment, newer .NET collection types may not be available out of the box.  
This repository fills that gap by porting the official .NET `PriorityQueue<TElement, TPriority>` for use in Unity.

It is intended for developers who want to use the modern .NET priority queue API in Unity without switching to a different third-party interface or rewriting existing usage patterns.

---

## Features

- Unity-compatible port of the official .NET `PriorityQueue`
- Designed to preserve the official .NET API syntax as closely as possible
- Useful for migrating or sharing code patterns between .NET and Unity projects
- Updated for C# 13-compatible usage

---

## Official Documentation

.NET official documentation:  
https://learn.microsoft.com/dotnet/api/system.collections.generic.priorityqueue-2

---

## Example

```csharp
PriorityQueue<string, int> testQueue = new PriorityQueue<string, int>(10);

testQueue.Enqueue("World", 2);
testQueue.Enqueue("Hello", 1);
testQueue.Enqueue("!", 3);

while (testQueue.TryDequeue(out var element, out var priority))
    Debug.Log(element);

// Result:
// Hello
// World
// !
```

---

## Why use this?

This repository is useful when:

* You want to use the official .NET `PriorityQueue` style in Unity
* You need a priority queue without adopting a completely different API
* You want smoother migration between standard .NET code and Unity codebases

---

## Notes

* The goal of this port is to preserve the official .NET usage experience as closely as possible.
* This repository focuses on practical compatibility for Unity development.
* It is intended as a Unity-usable adaptation of the official `System.Collections` implementation.

---

## Repository Summary

A Unity-ready port of the official .NET `PriorityQueue<TElement, TPriority>` with official-style API compatibility.
