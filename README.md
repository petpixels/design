# Pet Pixels
### The Pet Rock of Our Generation

## What is a Pet Pixel?

A pet pixel is a portable frosted plastic cube that lights up with a selected color, similar to a smart light bulb, except it’s portable and contains its own power source. The pixel can be “trained” by holding it over a color swatch or natural element to learn the color of that item or it can learn by either WIFI, Bluetooth, or USB, whichever is the cheapest for the pixel developer or most convenient for the pixel owner. Pixels can be grouped together or used independently, and while there is no theoretical limit to the number of pixels that can be grouped together, there are practical limits. Equally there is also no theoretical size limit to how large or small a pixel can be, but there are practical limits. For example my 3D printer can print a maximum size of 12cm3 so that’s as big as they’re going to get right now. 

## Why should I want a Pet Pixel?

Well, you shouldn’t. You should want a whole flock of pixels because they get lonely by themselves. In the wild, pixels tend to come together in groups of 8, 16, 32, 64, 128 and even 256. However in captivity, you can have any number of pixels you want, even just one… It will be a sad, lonely little pixel and it will live a life of solitude, but it will be your pixel and that will make it happy. 

## What good is a Pet Pixel? What can I do with it?

For starters, you can teach it a color, and since pixels of a feather flock together, you can teach lots of pixels lots of colors. Light up pixel art displays can be created by training individual pixels and then arranging them in order. Individual pixels can be controlled by IFTTT (If this then that) so that they light up in certain patterns based on weather conditions, such as gloomy and overcast for rain, or warm and yellow and green for sunny days. Create a night light for each room by putting a pixel anywhere you want a light, then teach the pixel to only turn on at night. Change your pixels by the season. Have pink and blue pixels for spring, red and orange pixels for fall. Your pixels can dance along to your favorite songs on Spotify or Pandora (I have no idea how) or hang them on strings and hang them on your family’s Christmas tree. Make really big pixels and create your own pixel juggling circus act. Make even bigger pixels and take them to a sports game and make a screen out of the fans in your section. Make really small pixels and turn your entire back yard into a television. Really, the possibilities are endless. 

## Pixel Perfect Design

There is no perfect pixel. There are only perfect pixels. Each individual pixel is very simple and self contained. One pixel can learn one color (or a sequence of colors) and remember it until it learns a new color or sequence. Then it can shine, shine, shine that color out until it’s little pixelly battery dies and it becomes a “dead” pixel. When it either charges up (solar?) or gets new batteries, it goes back to shine shine shine shine shine shine. You know come to think of it we should probably give it an off switch too. 

#### How to build a 3D pixel, a really bad 2D ASCII art rendering:

<pre>
-----------------------
|                     |
|    3D PRINTED       |
|    TRANSLUCENT      |
|        BOX          |
|                     |
|     [RGB LED]       |
-----------------------
Battery | Battery | Battery
Microprocessor with WiFi/Bluetooth
-----------------------
Light Sensor, USB, Button 
...
On/Off Switch
-----------------------
</pre>

Since each pixel is fundamentally identical to every other pixel, the magic happens in the software. Pixels can be trained individually or in groups. They can learn colors from their neighbors, from the internet through APIs, or from mobile phones or other Bluetooth devices. They can display single colors or streams of colors either by live feed, or by memory, and they can be synchronized to timers across the pixel flock. Memory works offline but cannot be updated and will be erased the next time the pixel is trained. It would be nice if these colors were stored in a form of memory that is not lost when power is interrupted (pixel death) so that the pixel does not need to be retrained when it is revived. 

### Micro interactions

Pixels are very simple creatures and interacting with them should be just as simple. Each interaction should be simple, well-defined and self-contained. Introducing a new pixel into the flock should be as simple as adding a record to a table and all pixels should be able to be controlled at once or individually. Untrained pixels display white which can be adjusted in brightness, at least from software, if not hardware (it would be nice to have a knob to adjust it with).

### On/Off

Pixels should have a manual on/off as well as a software wake/sleep that can be triggered from the network. An untrained pixel displays white until it is trained. 

### Training

Training can be done manually with the light sensor or remotely from the network. Pixels can learn colors by being placed over a color and minicking it, they can learn from their peers on the network, or from a “leader” pixel that once trained, broadcasts out to other pixels who then “follow” that pixel when they receive the broadcast. 

### Flocking

Pixels of a feather flock together. By creating and distributing timed sequences of colors, pixels can appear to “flock” into different patterns such as color waves or animations. Emergent behaviors could include creating a “screen” out of pixels which displays an image or video clip, creating a mirror out of pixels that uses a camera to show images on the pixels as a display. Pixels could also create strings of colors using timed sequences, which could be used to guide people along a path or trail. Pixels could then be replaced or revived as needed without disrupting the overall trail markings. The best way to handle all of these cases is to simply write a flocking API and make it available with the pixels so that developers can write any flocking algorithm they want to. 

## You mentioned that they don’t exist yet...

Pet Pixels are open source, so it’s up to you to help them exist. You can do that by donating (the easy way) or rolling up your sleeves and helping to develop them (the hard way) but at all stages of the process, it will be open source. Pixel progress will be documented here as well as whatever website you donated money to when you tried to get out of this the easy way, plans will be shared on Thingiverse and other websites. All products will be licensed by Creative Commons and allowed to be sold by others commercially— since there won’t be a way to stop people from doing it anyway. Small stipends, like bounties will be paid during the early phases of development to get things going, but as we are an open source project, fundamentally this will rely on community support much more than it relies on money. 

The next steps for production are to create a prototype of a pixel that can do the things described in this document, or at least most of them. Most likely this will involve a raspberry pi, a 3D printed cube, a few LEDs and a bunch of mistakes. After creating one successful pixel, the next obvious step is to create another one. At this point we have a major software problem which means that we will then solve that problem with MORE software. Lots more. Basically once the pixels are developed that moves onto becoming a manufacturing problem which we will probably need to crowdsource the funding for. Hopefully by then there is some community interest in the DIY crowd, but if not we will forge ahead and just do this as cheaply as possible. 

I will post progress here until there are more people working on it and then they can post their progress here too. 
