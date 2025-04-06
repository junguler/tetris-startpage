# startpage with self playing tetris
this project started as a test of chat gpt 3o-mini capabilities and see if it can make a good convincing self playing tetris game

the answer is kind of, it does play but it's far far off from how a human could play

regardless of the quality of the code it's very amusing to have a tetris game being played in your start page so i've worked to create a whole tetries-themed start page around it

## customizations
i have added some variables to quickly change some settings if you like, here they are

| name | line number | effect | range of numbers |
| -- | -- | -- | -- |
| GAME_SPEED | line 141 | setting the speed of the game | tested with 10-500 (lower is faster) |
| BACKGROUND_TETROMINO_COUNT | line 143 | setting the number of random tetris shapes in the moving background | tested with 1-200 (lower means less tetris blocks) |
| tetrisModes | lines 146-152 | the dimensions of the tetris game | change as you want, defaults are 'normal 10w x 20h' 'square 20w x 20h' 'tall 5w x 40h' |

## the buttons on the startpage
the default layout is two columns of 7 links for each side of the tetris game, changing this value is easy depending on how you want to design your page

look at line 29 and change ```grid-template-columns: repeat(2, auto);```

if you like the current setup but need less columns just change it to `repeat(1, auto)` and remove half of the links from each side, left side starting at line 88 and right side starting at line 108

making more buttons is just as easy, just change the columns to 3 and add 7 more buttons to each side etc

completely changing the layout is also possible but some manual intervention with the css is required since i've hardcoded the height of the game to always match 7 buttons in a column