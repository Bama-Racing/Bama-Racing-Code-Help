//NOTICE: It is possible these files are outdated. Last updated on July 1, 2020.


//#Backend Code
//So, arguably the most important feature the Pi has for us are the GPIO pins. These allow us to take in data from different breakout boards. Most of these breakout boards, as I mentioned before, most of these communicate with the Pi by either sending high or low voltage.

//Now the question is, what language are we going to use to decode what is coming through those pins and display them to a GUI?

//This was a question that took me a long time to figure out and I'm not sure how long it will take before I change my mind again (hence the notice at the top of all these documents). Since I am somewhat familiar with HTML/CSS which are usually used for websites, I decided to use them to quickly build a GUI. These two languages work together, the HTML defines the what text is going on the page and in what order. Then, by giving each block of text a class, you can then reference it's class in CSS and decide things like font, font size, color and a lot more.

//However, these two languages have another sibling, JavaScript, which is used for a lot outside web development, but in the case of web development, it is used to make the site move. At this very early stage in development, the only thing that changes are the numerical values of speed and RPM, but this is the language that handles that.

//Most languages also have addons that bring more features called Libraries. JavaScript is no different. This is useful to us because it just so happens that JavaScript has a Library allowing access to the GPIO pins on the RasPi.

//Then, the only question that remains are the mathematics behind turning pulses from a Hall Effect Sensor into an RPM.

//This starts with us counting these pulses.

//What we use is called an interrupt. What this does is while everything else is running, the interrupt grabs the attention of the computer and says hey, you need to come deal with this. Then, the interrupt hands the computer a list of instructions in the form of a function. Then, the computer goes back to what it was doing and waits for another interrupt.

//So, lets say you attach a button to a pin so that whenever you push the button it lets voltage through and attach that to an interrupt. You tell the interrupt to watch pin number 6, for example and you map it to the function buttonPush. Then, in that function, you can say print("Button was pushed") and every time you push that button, you will print out: Button was pushed.

//Now, if we map this to a timer, we can keep track of how many milliseconds pass between each button push. Then, if we divide 60 seconds by the amount of time it takes to complete one rotation, and swap out the button for a Hall Effect Sensor, we can calculate how many rotations will happen in 1 minute. Then, if you multiply that by the circumference of the wheels and you can calculate speed.

//Once we do this, we can tell the RasPi to print it to the screen and record it to a file (later, some of the other subteams will be able to access this file and use it for various calculations).

//#Front End
//Currently, the front-end is (for the most part) very simple. Currently, instead of displaying any actual speed or RPM data, I am just creating random numbers and pasting them into the HTML.

//To do this, I use a function. You can tell JavaScript you want to create a function with the following:
function functionName () {
  //Write code to be executed when the function is called here...
  console.log('Hello There');
}

//In JavaScript console.log() is like print() in Python or Arduino C so this function will print "Hello There" into the Console.

//There are a few things to note.
  //- One is the semicolon ; at the end of the line. At the end of any line in JavaScript, you need a semicolon.

  //- You should also be aware that functionName can be anything you want, as long as it is the only function with that name in the code.
    //- However, you could have a function named Banana, and another function named Banana2. Just so long as the  two strings of characters are different.

  //- Then, the next thing to note is the first pair of brackets (). Inside these brackets you can tell the function to expect variables. These variables can then be referred to in your function.

      //For example:
      function functionName2 (Banana) {
        console.log(Banana);
      }

      //Then, if you call your function later in your code, you must pass something for it to pass into Banana.

      functionName2("Roll Tide");

      //The above line will result in 'Roll Tide' being printed into the Console.

//This explanation should help you decode the following which is what I use to update the Speed Variable on the HTML page:

  function changeHeading (speedID, newSpeed) {
    const speedTagUpdate = document.getElementById(speedID);
    speedTagUpdate.textContent = newSpeed;
  }

  changeHeading('speed', randomNumber);

  //So, this function takes two arguments, speedID and newSpeed. Then we create a constant variable with const and call it speedTagUpdate. We set it equal to document.getElementById(speedID). This looks really scary but what it is doing is telling the JavaScript that it can find the text that we want to update in a variable called speedTagUpdate.

  //On the next line, we take that variable and change the textContent to newSpeed.

  //If we look again at the bottom where we called our changeHeading() function, and match it to the variables we told JavaScript to expect, we see that we set newSpeed equal to a randomNumber which is a variable that is defined somewhere else in the code.

  //We then put this function inside an infinite do {} while () loop:

        do {
          //Write your code that you want JavaScript to do here...
        }
        while (this condition is true)

  //So, if you write:

      let i = 0; //let is how you create a variable. Here we are creating a variable named i with the value zero

      function setup () {
        setTimeout(loop, 250); //setTimeout is a function that requires two variables. A function you want to   execute, and then the amount of timeout time until you want it to execute.
      }

      function loop () {
          do {
            console.log('Hello there.');
            setup(); //calls the setup function again, starting the loop over
          }

          while(i = 0)
      }

  //JavaScript will write "Hello there" in console every 1/4 second until your computer dies.

  //I hope this has helped. I know I can't cover everything here, but I will start working on some videos explaining the code as soon as it is finished. 
