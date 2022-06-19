# Coding Challenge
## How to run the app

Requires an installation of Node.js: https://nodejs.org/en/

Inside the /imagecolourchallenge directory run the following commands  

>`npm install`  
>`npm start`

Visit http://localhost:3000
## Process

The first thing I did was research the challenge which led me to this thread where people had completed the challenge in 2014: https://codegolf.stackexchange.com/questions/22144/images-with-all-colors  

At first glance the algorithms were difficult to understand, so I decided to start very simple with some rough code. In other words applying the KISS principle - the aim being to get all the colours generating and an image appearing with a jsfiddle, but not much happening in terms of an actual algorithm generating a unique image: https://jsfiddle.net/jimorey/m35e2b1h/40/.

Once I had this I then took that rough code and made a simple web app with Node.js and Express which is what this repository is for. From this point I and started working with the standard array sort function to see if I could get some cool effects going. I was getting some cool effects, but this still wasn't a proper algorithm that was generating a unique image every time.

Now that I had learnt quite a bit and had a better understanding I came up with an idea for my own algorithm. Here are the rough notes for the algorithm:

>Colours array - red, green, blue  
>Pixels array - x, y
>
>Pick a random pixel and a random colour  
>Add that to image  
>Remove those from arrays  
>  
>Find the next closest colour to colour that was used before
>  
>Find pixels adjacent to current pixel and add to an array  
>-1x?  
>+1x?  
>-1y?  
>+1y?  
>-1x-1y?  
>-1x+1y?  
>+1x-1y?  
>+1x+1y?  
>
>Pick pixel at random from available adjacent
>
>If no adjacent pixel found and pixel array has remaining pick a pixel at random from available and go again from there  
>
>Add colour to image at that pixel
>
>Remove colour and pixel from arrays
>
>Repeat  

I went ahead and implemented the algorithm and ended up with something that generates rivers of similar colours until all the pixels and colours available are used. At this point I was happy with what I had and cleaned the code. La Fin.
