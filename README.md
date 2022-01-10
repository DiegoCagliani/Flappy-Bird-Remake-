# Flappy-Bird-Remake-
#### Video Demo:  <https://www.youtube.com/watch?v=9D7zOTu0xGk>
#### Description:
Flappy Bird was a side-scrolling mobile game featuring 2D retro style graphics. The objective was to direct a flying bird, named "Faby", who moves continuously to the right, between sets of Mario-like pipes. If the player touches the pipes, they lose. Faby briefly flaps upward each time that the player taps the screen; if the screen is not tapped, Faby falls because of gravity; each pair of pipes that he navigates between earns the player a single point, with medals awarded for the score at the end of the game. No medal is awarded to scores less than ten. A bronze medal is given to scores between ten and twenty. In order to receive the silver medal, the player must reach 20 points. The gold medal is given to those who score higher than thirty points. Players who achieve a score of forty or higher receive a platinum medal. Android devices enabled the access of world leaderboards, through Google Play.

There is no variation or evolution in gameplay throughout the game, as the pipes always have the same gap between them and there is no end to the running track, having only the flap and ding sounds and the rising score as rewards.
My goal was to try to completely redo the game using HTML, Java Script and Css.



To start, make a new folder, name it flappy bird and then open it in with brackets. Brackets is a text editor that makes it very easy to render a preview of what your website will look like.

Create three files: index.html, style.css, script.js. In the index.html file we’ll begin by creating a basic HTML layout, a head and a body and we’ll change the title to Flappy Bird. Next connect the css file and the script file. 

Create a game div which contains all the elements of flappy bird. Inside of that, create 3 more divs, the first with id=”block”, the next one with “hole” and the final div with “character”. 

Hop over to your CSS file and begin by removing the basic paddings and margins that are automatically added by the browser. Next start giving the game div some styles. A width and a height and a border so that we can see the outline of it. Also add margin: auto; so that it’s always centered. 

Next start styling the block div. We’ll add a width and a height and a background-color. Add left: 400px, because thats the width of the game, and that left property won’t work unless the div has position: relative.

Now create a keyframe animation that will start with the block on the right, and finish with it on the left. Add it to the block div with the animation property, and set it to be infinite. You’ll notice the block goes outside the game div, so just add overflow: hidden to the game div to make it look a lot better!

Next start adding properties to the hole div. Give it mostly the same properties as the block div, except the height will only be 150px and the background color will be white. Because the block and hole div are both position relative that means they come ontop of eachother, so add the property top: -500px to the hole to bring it down 500px, which is the height of the block! 

Next we’ll change the position of the hole after every animation.

Start by creating some variables for the block and hole so that we can use the right elements. Next create an event listener that runs a function after every hole “animationiteration”. Inside that function we’ll create a variable random. Math.random returns a random decimal between 0 and 1, multiply it by 300 so that it returns a number between 0 and 300. Also add 150 after, so that it returns a number between 150 and 450, and then also set that to be negative so that its between -150 and -450. Set the top position of the hole to that random number. Now every time the animation runs the hole will have a different position.

Now onto the character. Start by adding some css properties; width, height, background-color: red, position: absolute, top: 100px, and border-radius to make it a ball.

Next create a function that will act as gravity. Make an interval function that runs every 10 milliseconds. Create a new variable characterTop and its going to be equal to the current top position of the character div. We can get that by using “window.getComputedStyles()” and then the element we want the styles from, then “getPropertyValue()” and we want the top property. So now our variable characterTop will be equal to the css value of the top property of the character div. Next set a new top position for the character, and it’ll be the same amount as before except we’re going to add 3px to it. 

Next create another function named jump which will make the ball go up, basically the opposite of our gravity function. We’ll have to go back to our HTML and add an onclick to run our jump function, and we’ll put it on the html tag so that it works if the user clicks literally anything. 

Next go back to your javascript and create a new variable “jumping” and set it to zero.
Inside the jump function set our new variable to 1 and then when our function ends, set it back to 0. That means that if the jumping variable equals 1 then we are currently jumping, if it equals 0 then we’re not jumping. 

Now add an if statement so that the gravity function only changes the top if we’re not currently jumping, or else we would be moving the ball up and down at the same time and that just gets messy.

transcript etc...

Now our flappy bird game is fully functioning. But don’t stop there! Keep adjusting the code and properties and make the game more interesting! Maybe super wide blocks? Or slower or faster movements! Anything is possible!
