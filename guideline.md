---
layout: page
title: Coding Guidelines
permalink: /guideline/
---

## General
* Indentation: code is indented according to best practices. If possible do not indent with tabs but with 2 spaces [see here](http://programmers.stackexchange.com/questions/57/tabs-versus-spaces-what-is-the-proper-indentation-character-for-everything-in-e)
* Avoid redundancy. If you are doing copy-paste, there is probably a nicer way to solve it :) [Copy-paste-programming](https://en.wikipedia.org/wiki/Copy_and_paste_programming)

## FrontEnd
* CSS should always be in the header section. Not in the body
* It is ok to put JS in body but at the end of the body and if possible all code between

## Versioning
* All code is versioned - no exception
* Since everything is versioned no need to pollute files with unnecessary meta information like author, date_created and so on
* Everytime something new has been done and the code compiles - commit
* Work on a separate branch, when happy with the result create a pull-request. Do not merge onto `master` without having code reviewed
* Don't commit on `master` if code does not compile
* Never stop working without having pushed. If code does not compile, create a new branch

## BackEnd
* Scala coding: check out [naming conventions](http://docs.scala-lang.org/style/naming-conventions.html)
* All functions documented unless already documented in underlying trait or abstract class
* When writing a class/object/case class, avoid using the name of the class in the methods. E.g. Object Movie should not contain a method getMovie but rather simpy get()
* Use functional style whenever possible; i.e. favor `map` over `for`-loops etc.
* Use dynamic reference to link whenever possible; i.e. @routes...
* When defining a model, use a simple english with the first Letter Capitalized. The associated controller will have the same name with the suffix `-Ctrl`
Case class bear the same name as the class they are associated to. If there are more than one case class associated with the object, add a suffix, and make sure to document. case class do not have underscore. If injecting model as service into controller the name suffixed with `Service`
* functions are tested unless trivial


