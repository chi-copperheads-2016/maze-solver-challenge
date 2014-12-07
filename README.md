# Theseus.rb

In this challenge you will use your knowledge of data structures and algorithms to build a maze solver.

## Release 1, Reading the Maze

Your maze will be defined in a text file that looks like this:

```
o#........
.#####.##.
.......##.
######.#*.
.......###
```

 * `#` is a wall
 * `.` is an open tile
 * `o` is your start point
 * `*` is your goal

You will need to read in the Maze file and model it in your program. The maze can be any dimension and in any configuration, but it will always have four sides, and corridors will always be 1 block wide (as shown above).

There's a saying, "90% of programming is choosing the right data structures." Pick something simple and flexible to start. You may refactor it as you develop your solver algorithm.

## Release 2, The Solver

Your task is to write an algorithm that walks the maze and determines if it is solvable or not. Your program can simply print out "Solvable" or "Unsolvable".

### Thinking it Through

 * How would _you_ solve it with pen and paper?
 * Can a computer do it the way you did?
 * If not, why? What kind of approach(es) might work for a computer?
 * Can you break them down to a pseudocode algorithm?
 * When you consider your possible solution, what data structures would help you model the problem or manage state in your algorithm?

### Design considerations

We'll be experimenting with different approaches in the coming releases, so think about how you will handle swapping different algorithms that direct your search. Your code should have an interface that lets you "drop in" a given strategy.

## Release 3, Show and Tell

Visualize the search pattern of your algorithm by clearing the terminal screen and reprinting the map at each stage of the exploration. Mark the explored areas as it progresses.

You can use this to clear the screen between print statements:

```ruby
def clear_screen
  print "\e[2J\e[f"
end
```

What does your algorithm's search pattern look like? Commit a description in `notes.md`.


## Release 4, Strategery
Develop two algorithms. One should look something like this:

![](assets/dfs.gif)

And the other should look like this:

![](assets/bfs.gif)

**Note**: The two approaches above are identical except for the data structure they use under the hood.

Release 3 should have made it easy to swap in approaches. In fact, you may have inadvertently implemented some form of the [strategy pattern](http://en.wikipedia.org/wiki/Strategy_pattern).

## Release 5, Inefficient Searches

Construct a map that triggers an exceptionally inefficient search with each algorithm. In other words, you should be able to see that your code (with either algorithm) is not searching at all optimally.

Why is this? What is your algorithm doing inefficiently? Don't refactor now, but brainstorm and describe some ideas (no matter how theoretical) that might speed things up.

Commit your thoughts in a file called `notes.md`. We'll look at some different approaches in the next challenge.
