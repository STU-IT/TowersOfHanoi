Towers of Hanoi
===============

- is a game-puzzle where you are supposed to solve the riddle of moving disk under certian restrictions, from one pin to another.
- It is also a programming execise designed to teach the use of simple data structures in arrays and simple objects, used as mere structs.

__Your mission__, should you choose to accept it, is to make the game mecanics work with the GUI (Graphical User Interface):

To finish the game, implement and finish the functions [`isValidMove()`](./docs/global.html#isValidMove), [`moveDisc()`](./docs/global.html#moveDisc) and [`gameWin()`](./docs/global.html#gameWin).


1. When the user drags a disc, an drops it on a stack, you shold update the data model, so the model reflects, 
the movement of discs.  
You should this in function [`moveDisc()`](./docs/global.html#moveDisc). This function takes two arguments `fromStack` and `toStack`
    + Once dropped, and after your updates to the datamodel, the system will re-`draw` the user interface, 
    so that the current changes are made visible to the user.
    The system also reassigns the  `draggable` attribute to the discs on top of each stack.
  
    _Hint:_ Moving elements form one array to another can be done with `pop()` and `push()` 
    or in this case `shift()` and `unshift()`.  
    _Bonus question:_ Can you explain the difference between `pop()` versus `shift()` 
    or `unshift()` versus `shift()`?  
    See [Ben Nadals Blog, Javascript Array Methods: Unshift(), Shift(), Push(), And Pop()](https://www.bennadel.com/blog/1796-javascript-array-methods-unshift-shift-push-and-pop.htm)

2. Before actually moving discs we need to check if a move is valid. Your job is to finish the function [`isValidMove()`](./docs/global.html#isValidMove). 
This function checks if its ok to move the top element from `fromStack` onto `toStack`. You should virify this by observing these rules:  
     + A disc must never be on top of a smaller disc
        + in other words: a disc can only be on top of larger disc or on an empty stack.
     + You can only move one disk at the time (but that is taken care of by the GUI funktionality. Only the top disks have the dragable property)
     
    _Hint:_ Just focus on the first rule here, and `isValidMove` will work fine.

3. `gameWin()` is the function that checks if the game is solved. Meaning that all the discs have been mooved to the rightmost stack, and is in proper order.
Implement this feature by finishing the function.


## References
[Wikipedia](https://en.wikipedia.org/wiki/Tower_of_Hanoi)  
[Khan Academy](https://www.khanacademy.org/computing/computer-science/algorithms/towers-of-hanoi/a/towers-of-hanoi)

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" href="http://purl.org/dc/dcmitype/Text" property="dct:title" rel="dct:type">Towers Of Hanoi - Array exercise</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="https://github.com/STU-IT/TowersOfHanoi" property="cc:attributionName" rel="cc:attributionURL">Søren Magnusson</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.
