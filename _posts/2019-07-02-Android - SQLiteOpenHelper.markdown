---
layout: post
title: Android SQLiteOpenHelper
date: 2019-07-02 00:53:00
description: How to use SQLiteOpenHelper?
---

There should be careful when you use "SQLiteOpenHelper" in Android program.
The "onCreate" function exists as other class, but it is called only once for program life time.

When getWritableDatabase() or getReadableDatabase() is called and there is no database,
the "onCreate" is executed!

After the "onCreate" is executed, a database is created.
So the "onCreate" will not executed because database already exists.


