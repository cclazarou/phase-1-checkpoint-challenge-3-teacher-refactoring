# Super Crazy Bonus Release

Edit this file to answer the following questions. Give examples. You may need to do a bit of research. :)

1. Why is Hash.fetch useful?
Not only does it allow you to find values by index, but if used on a hash that was passed as a method argument, it returns a value if specified (by key) OR a default value.  This contrasts to the more "direct" mode of giving optional values in the method argument itself, where what you can pass as an argument to the method is less flexible:
'def method_thing(name = "Dummy", age = -49)'
you can provide a name, but no age
you can't provide no name, but an age
while
'def method_thing(options = {})
   @name = options.fetch(:name,"Dummy")
   @age = options.fetch(:age, -49)'
could take single parameter and assign its value to the appropriate instance variable

2. What is the disadvantage of single inheritance, and what's a possible solution to that problem?
It is less extensible than inheriting from multiple classes where appropriate - in this exercise, there may be more kinds of teachers added to staff, or they may want to add mentors - which are not teachers,students,seniorteachers,or apprenticeteachers, and therefore should inherit from Person.

3. Why are these classes initialized with an options hash?

4. What is the purpose of the private keyword in a class? What does it protect you from and why is that valuable?

private keeps methods from being called from outside the class, which is helpful in cases that you do not want users to do whatever the methods are doing (i.e. destroying/manipulating data they shouldn't have access to)

5. Why are concepts like encapsulation, single responsibility, and abstraction important? Now that you've been programming for a while, have you seen any advantages for yourself, or can you imagine them in the future?
