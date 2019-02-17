# Pet Pixels
### The Pet Rock of Our Generation

## What is a Pet Pixel?

A pet pixel is a portable frosted plastic cube that lights up with a selected color, similar to a smart light bulb, except it’s portable and contains its own power source. The pixel can be “trained” by holding it over a color swatch or natural element to learn the color of that item or it can learn by either WIFI, Bluetooth, or USB, whichever is the cheapest for the pixel developer or most convenient for the pixel owner. Pixels can be grouped together or used independently, and while there is no theoretical limit to the number of pixels that can be grouped together, there are practical limits. Equally there is also no theoretical size limit to how large or small a pixel can be, but there are practical limits. For example my 3D printer can print a maximum size of 12cm3 so that’s as big as they’re going to get right now. 

## Fungible displays

While Pet Pixels are cute on their own, what they allow is fungibility in displays. (Expand more later)

## Individual Pixel Design

[Pixel Sketch](https://user-images.githubusercontent.com/43132136/52911577-6ede0400-325a-11e9-8a68-5b328a711ef9.jpeg)

Parts:

  Arduino
  RGB LED
  Battery & Power Management
  Color Sensor
  Input button
  3D Printed Form Factor
  Acrylic Diffuser

Functionality

  Receive and store color values via
    USB input
    Color sensor input
    
  Color Sensor
    Press Button
      Light Sensor Input Routes to LED Output
    Button Release
      Store Last Input
      Output on loop
      
    Press button twice to store another color (3, 4, etc up to device capacity)
    When colors are input with the button, the interval is fixed instead of variable (based on config or default value)
    
  USB Input
    Accept RGB Value
    Accept File of Looped Values (RGB, Interval)
    Accept Current Time and Set System Clock
    Accept Start Time
    Charge Battery
    
  USB Disconnect
    Play Looped File (if available)
    Hold last value if no file
    
  ## Pixel Hub Design
    
  Parts:
    Raspberry Pi
    Powered USB Hub (# of pixels + 1)
    Power splitter for 16 pixel model

  Functionality: 
    
    Assigned a block number and downloads data for a set number of pixels
    Controls groups of 4, 7, 9, or 16 pixels
    Manages pixels via USB
    Connects to other controllers via WiFi Mesh
    Connects to image server via WiFi
    Syncs with time server and sets clocks on pixels
    If pixels are missing, those pixels are ignored but the data is still requested as if it were there
    
  Software:
      
    As a hub comes online, it requests 
      Find image server (config)
      Current time from the server
      RGB and duration values for the total number of pixels that it manages
      If a group number is assigned, it requests the pixels for its assigned group number
      If no group number is specified, the server will send one along with the data for the pixels
    File is confirmed as received (checksum)  or re-requested 
    If this fails, re-boot the box and try again
    All the data for the stream should be downloaded before the success code is sent to the server
    Set clocks on all connected pixels 
    Set clock on pixel plug/unplug
    Send data to all pixels
    Poll server for start time
    Send start time to all pixels
    
    Request:
      Hub UUID
      Number of Pixels
      Hub Number (optional)
        Hub numbers are initially assigned by the server but can be set via config
      
    Response:
      Pixel data for the hub number
      Start time (if available)
      The next available hub number (if unspecified)      
    
    Start:
    
      Set clock
      Send time to USB
      Send color values to USB
      Send start time to USB
      Wait for interrupt
      
