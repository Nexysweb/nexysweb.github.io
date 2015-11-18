---
layout: page
title: Coding Guidelines
permalink: /guideline/
---

## General
* Indentation: code is indented according to best practices. If possible do not indent with tabs but with 2 spaces [see here](http://programmers.stackexchange.com/questions/57/tabs-versus-spaces-what-is-the-proper-indentation-character-for-everything-in-e)

## FrontEnd
* CSS should always be in the header section. Not in the body
* It is ok to put JS in body but at the end of the body and if possible all code between

## Versioning
* All code is versioned - no exception
* Since everything is versioned no need to pollute files with unnecessary meta information like author, date_created and so on
* Everytime seomthing new has been done and the code compiles - commit
* Don't commit on master if code does not compile
* Never stop working without having pushed. If code does not compile, create a new branch

## BackEnd
* All functions documented unless already documented in underlying trait or abstract class
* Respect a strict MVC architecture
* When writing a class/object/case class, avoid using the name of the class in the methods. E.g. Object Movie should not contain a method getMovie but rather simpy get()
* For CRUD object use an abstract class, e.g. tCRUD
* When working with Anorm, table names are never stored in query, but in external variable. Ideally as a table variable in the associated object. This avoids running in big issues when changing table names etc.
* Use functional style whenever possible; i.e. favor map over for-loops etc.
* Use dynamic reference to link whenever possible; i.e. @routes...
* Indentation: not tabs, 2 spaces
* When defining a model, use a simple english with the first Letter Capitalized. The associated controller will have the same name with the suffix -Ctrl
Case class bear the same name as the class they are associated to. If there are more than one case class associated with the object, add a suffix, and make sure to document. case class do not have underscore. If injecting model as service into controller the name suffixed with `Service`

