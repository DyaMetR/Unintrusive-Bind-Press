# Unintrusive bind press

![](https://img.shields.io/github/v/release/DyaMetR/unintrusive-bind-press)
![](https://img.shields.io/github/issues-raw/DyaMetR/unintrusive-bind-press)
![](https://img.shields.io/github/license/DyaMetR/unintrusive-bind-press)

## A solution to breaking other addons using the mouse wheel

### How to install

Place the script file inside a Lua environment folder (such as the `lua` folder or a game mode folder).

Then, include the file **client-side wise** as the _PlayerBindPress_ hook is _client-side only_. In case of manual inclusion, make sure your implementation is included _after_ you've included this script.

Alternatively, you can place it into `lua/autorun/client` for it to be included automatically.

### How to use

`UnintrusiveBindPress.add(id, func, priority)`

Hooks a function to the PlayerBindPress event.

+ **id**: unique function identifier.
+ **func**: function to run.
+ **priority** _(optional)_: sets a priority (1 being top priority)

### Other functions

`UnintrusiveBindPress.remove(id)`

Removes a function hooked to the PlayerBindPress event.

+ **id**: unique function identifier.

`UnintrusiveBindPress.getTable(priority)`

Returns the list of functions hooked to the PlayerBindPress via this system.

+ **priority** _(optional)_: the priority of the functions we want to get.
