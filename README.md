# The Kore Programming Language
-----------------
The programming language designed to make developing big web applications easier.Kore enforces types, scopes, and structure at compile time so bugs are caught before the browser ever sees your code.
------------------------------------------------------------------------------------------------------------
# NOTICE:
This tutorial mainly documents developing Kore applications on Windows since it is mainly available on there!
----------------------------------------------------------------------------------------------
# A basic hello, world program in Kore that outputs 'Hello, World!' to the browser console:
```
uses 'io'

public safe void func main() {
    io:print("Hello, World!");
}
```
----------------------------------------------------------------------------------------------
# What is Kore?
Kore is a statically typed, verbose, intuitive programming language and superset of JavaScript.
# How does Kore run?
Kore's CLI compiler takes a .kore as a command-line argument input and it will generate a .kgc file containing JavaScript in the same directory, which can be directly put into a HTML file with the `<script>` tag or changed into a .js file at release, though keeping it as a .kgc file is recommended during development.
---------------------------------------------------------------------------------------------
# Getting started
To get started, make sure you have installed The Kore Compiler (a zip file) from this repository's releases. Once you get it on your machine, make sure to extract it, put it in an important folder such as Program Files (On Windows). Then, it is good practice to set up an environment path variable. This can be done by creating a new environment path variable, for example: Kore -> OS\Example\Kore (and make sure that you only include the folder that contains only the main files, not any file sitting in it), and then edit the existing 'Path' variable, click 'New' and add %YOUR_VARIABLE_NAME%, for example, it can be: Kore, so you do %Kore%. To check if Kore is successfully set up, go to a command-line/terminal and type out: `kore version`.
# Syntax
Kore has an unique syntax, especially when compared to other languages that transpile to JavaScript (for example: TypeScript, CoffeeScript...), to make a program in Kore we first need to initialize a main function, that can be done by:
```
public safe void func main() {
    # This is a comment!
}
```
As you may have noticed, it's is quite verbose! Don't worry, we will tackle this together. When making a function the first step is telling the scope to the compiler, it can be `public` or `local`, public means it is available to everything in our program while local means that it is only available to the things inside the object where it is declared (AKA only available in the current scope), in this example we are using `public`. The second thing we need to tell is if the function is safe or unsafe, this is mainly for readability, but we will mostly put `safe`. Next is the return type, it is the data type of the value that the function returns, here in the example we use `void` because the function doesn't return a value. Next is `func` which is a mandatory keyword we should always put when declaring a function, and lastly is the name of the function, every non-module `.kore` file must include a main function so the function is named main. You also may have noticed that there is a hashtag and some text after it, don't worry that is just a comment and it is ignored by the compiler, the use of comments is reaching higher code readability.

---------------------------------------------------------------------------------------------------------

Now that you understand the core of the language, instead of reading long paragraphs of text, you can read from the cheatsheet provided below. The documentation of the Kore programming language may include more things in the feature but currently this is everything.

-------------------------------------------------------------------------------------------------------------

# CHEATSHEET

## Comments
`#` `#* *#`

## Variable Declaration
`public` `local` `safe` `unsafe` `variable` `constant`

## Types
`int` `string` `bool` `char` `array` `void`

## Bool Literals
`true` `false` `prob` `both`

## Char Literals
`|A|` `|z|` `|9|`

## String Interpolation
`#{expr}`

## Increment / Decrement
`i+++` `i---`

## Operators
`==` `!=` `<` `>` `<=` `>=` `&&` `||` `!`

## typeof
`typeof x`

## Functions
`public` `local` `safe` `unsafe` `void` `int` `string` `bool` `char` `array` `func` `retr`

## Control Flow
`precise safe if` `precise safe else if` `precise safe else`

## Loops
`loop safe (init; condition; increment)` `loop safe while`

## Approx If
`approx safe(ms) if` `killReceiver(n)`

## Selectors
`$name` `drop($name)`

## Modules
`uses 'filename'`

## Colon Syntax
`object:method()`

## io
`io:print()` `io:input()` `io:warn()` `io:verify()`

## math
`math:add()` `math:sub()` `math:mul()` `math:div()` `math:mod()` `math:pow()` `math:sqrt()` `math:abs()` `math:floor()` `math:ceil()` `math:round()` `math:trunc()` `math:max()` `math:min()` `math:clamp()` `math:isEven()` `math:isOdd()` `math:isPositive()` `math:isNegative()` `math:isZero()` `math:isInt()` `math:log()` `math:log2()` `math:log10()` `math:sin()` `math:cos()` `math:tan()` `math:asin()` `math:acos()` `math:atan()` `math:atan2()` `math:random()` `math:randomInt()` `math:randomFloat()` `math:pi()` `math:e()` `math:tau()` `math:infinity()` `math:sum()` `math:avg()` `math:sign()` `math:hypot()` `math:factorial()` `math:gcd()` `math:lcm()` `math:isPrime()`

## string
`string:length()` `string:toUpper()` `string:toLower()` `string:capitalize()` `string:trim()` `string:trimStart()` `string:trimEnd()` `string:includes()` `string:startsWith()` `string:endsWith()` `string:indexOf()` `string:lastIndexOf()` `string:count()` `string:replace()` `string:replaceAll()` `string:reverse()` `string:repeat()` `string:slice()` `string:substring()` `string:charAt()` `string:charCodeAt()` `string:padStart()` `string:padEnd()` `string:center()` `string:split()` `string:join()` `string:lines()` `string:words()` `string:isEmpty()` `string:isBlank()` `string:isNumeric()` `string:isAlpha()` `string:isAlphaNumeric()` `string:toInt()` `string:toFloat()` `string:fromCharCode()` `string:template()`

## array
`array:length()` `array:isEmpty()` `array:first()` `array:last()` `array:get()` `array:push()` `array:pop()` `array:shift()` `array:unshift()` `array:insert()` `array:removeAt()` `array:remove()` `array:slice()` `array:take()` `array:drop()` `array:chunk()` `array:includes()` `array:indexOf()` `array:find()` `array:findIndex()` `array:filter()` `array:count()` `array:map()` `array:reduce()` `array:flat()` `array:flatMap()` `array:reverse()` `array:sort()` `array:sortBy()` `array:unique()` `array:compact()` `array:zip()` `array:flatten()` `array:sum()` `array:avg()` `array:min()` `array:max()` `array:union()` `array:intersect()` `array:difference()` `array:every()` `array:some()` `array:none()` `array:shuffle()` `array:fill()` `array:range()` `array:toObject()` `array:join()` `array:toString()`

## type
`type:isInt()` `type:isFloat()` `type:isNumber()` `type:isString()` `type:isBool()` `type:isArray()` `type:isObject()` `type:isFunction()` `type:isNull()` `type:isUndefined()` `type:isNaN()` `type:isInfinity()` `type:isChar()` `type:isSelector()` `type:of()` `type:toInt()` `type:toFloat()` `type:toString()` `type:toBool()` `type:toArray()` `type:equals()` `type:deepEquals()` `type:assertInt()` `type:assertString()` `type:assertBool()` `type:assertArray()` `type:assertChar()`

## time
`time:now()` `time:timestamp()` `time:date()` `time:year()` `time:month()` `time:day()` `time:hours()` `time:minutes()` `time:seconds()` `time:milliseconds()` `time:format()` `time:friendly()` `time:timeString()` `time:delay()` `time:nextFrame()` `time:after()` `time:every()` `time:stop()` `time:stopwatch()` `time:diff()` `time:diffSeconds()` `time:diffMinutes()` `time:diffHours()` `time:diffDays()` `time:isBefore()` `time:isAfter()` `time:isSameDay()` `time:addDays()` `time:addHours()` `time:addMinutes()` `time:addSeconds()`

## storage
`storage:set()` `storage:get()` `storage:remove()` `storage:has()` `storage:clear()` `storage:keys()` `storage:size()` `storage:all()` `storage:sessionSet()` `storage:sessionGet()` `storage:sessionRemove()` `storage:sessionHas()` `storage:sessionClear()` `storage:cookieSet()` `storage:cookieGet()` `storage:cookieRemove()` `storage:cookieHas()`

## http
`http:get()` `http:post()` `http:put()` `http:patch()` `http:delete()` `http:getText()` `http:status()` `http:ok()` `http:safe()`

## random
`random:int()` `random:float()` `random:between()` `random:bool()` `random:chance()` `random:char()` `random:charUpper()` `random:digit()` `random:string()` `random:hex()` `random:uuid()` `random:pick()` `random:pickMany()` `random:shuffle()` `random:sample()` `random:color()` `random:rgb()` `random:weighted()` `random:seeded()`

## validate
`validate:required()` `validate:notEmpty()` `validate:minLength()` `validate:maxLength()` `validate:exactLength()` `validate:matches()` `validate:noSpaces()` `validate:min()` `validate:max()` `validate:range()` `validate:positive()` `validate:negative()` `validate:integer()` `validate:email()` `validate:url()` `validate:phone()` `validate:numeric()` `validate:alpha()` `validate:alphaNumeric()` `validate:hex()` `validate:ipv4()` `validate:date()` `validate:json()` `validate:passwordWeak()` `validate:passwordMedium()` `validate:passwordStrong()` `validate:form()` `validate:rule()`

## color
`color:parse()` `color:toHex()` `color:toRgb()` `color:toRgba()` `color:toHsl()` `color:fromHex()` `color:lighten()` `color:darken()` `color:mix()` `color:opacity()` `color:invert()` `color:grayscale()` `color:luminance()` `color:contrast()` `color:isReadable()` `color:bestTextColor()` `color:random()` `color:palette()` `color:complementary()` `color:triadic()` `color:red()` `color:green()` `color:blue()` `color:white()` `color:black()` `color:gray()` `color:yellow()` `color:cyan()` `color:magenta()`

## dom
`dom:get()` `dom:getAll()` `dom:body()` `dom:head()` `dom:root()` `dom:active()` `dom:title()` `dom:setTitle()` `dom:create()` `dom:make()` `dom:fragment()` `dom:clone()` `dom:append()` `dom:prepend()` `dom:before()` `dom:after()` `dom:remove()` `dom:empty()` `dom:replace()` `dom:wrap()` `dom:unwrap()` `dom:move()` `dom:getText()` `dom:setText()` `dom:getHtml()` `dom:setHtml()` `dom:getValue()` `dom:setValue()` `dom:clear()` `dom:getAttr()` `dom:setAttr()` `dom:removeAttr()` `dom:hasAttr()` `dom:toggleAttr()` `dom:getId()` `dom:setId()` `dom:getName()` `dom:addClass()` `dom:removeClass()` `dom:toggleClass()` `dom:hasClass()` `dom:setClass()` `dom:getClasses()` `dom:replaceClass()` `dom:getStyle()` `dom:setStyle()` `dom:setStyles()` `dom:removeStyle()` `dom:computed()` `dom:show()` `dom:hide()` `dom:toggle()` `dom:isVisible()` `dom:opacity()` `dom:fade()` `dom:fadeIn()` `dom:fadeOut()` `dom:width()` `dom:height()` `dom:rect()` `dom:top()` `dom:left()` `dom:scrollTop()` `dom:scrollTo()` `dom:scrollIntoView()` `dom:parent()` `dom:children()` `dom:firstChild()` `dom:lastChild()` `dom:next()` `dom:prev()` `dom:siblings()` `dom:closest()` `dom:contains()` `dom:index()` `dom:focus()` `dom:blur()` `dom:submit()` `dom:reset()` `dom:check()` `dom:uncheck()` `dom:isChecked()` `dom:enable()` `dom:disable()` `dom:isDisabled()` `dom:select()` `dom:getSelected()` `dom:exists()` `dom:tag()` `dom:matches()` `dom:dataset()` `dom:getDataset()` `dom:setDataset()`

## dom_events
`dom_events:buttonClicked()` `dom_events:hovered()` `dom_events:focused()` `dom_events:inputChanged()` `dom_events:getValue()` `dom_events:keyPressed()` `dom_events:keyJustPressed()` `dom_events:watch()`
