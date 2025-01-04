<img src="https://github.com/user-attachments/assets/866e4c9e-5359-4415-be30-a632a4094bb4" width="500" />
<header>

# Xtray for the Original Xbox

_Xtray for the Original Xbox_ is a replacement bracket for the DVD drive, with an embedded LED strip that is powered by the DVD's socket in the motherboard. The main purpose for this project are to 
- Provide a visually appealing alternative (for some users anyway) to existing methods
- Easy of installation with no requirement for soldering i.e. to power the LED
- Provide a self-contined solution with no additional external requirements 

</header>

# Requirements for building your own Xtray

The main things you need to build your own Xtray are as follows:

1. The Xtray 3D printed bracket that allows you to route the LED strip and supports the Xtray PCB 
2. The Xtray PCB providing all the (very simple) electronics to power and control the LED
3. The LED strip itself
4. A cable to connect the Xtray PCB to the power socket in the Xbox motherboard
5. 2x screwes to fix the Xtray PCB to the Xtray 3D printed bracket-   

## 1 - The Xtrax 3D printed bracket
_The Xtray 3D printed bracket_ is a variation of the [Xbox DVD Elimination Bracket](https://www.printables.com/model/206888-xbox-dvd-elimination-bracket) by RubyRoid. 
The main difference are two small holes to thread the LED strip to the back of the bracket, and some simple additions to support the mounting of the Xtray PCB to the 
back of the bracket. These additions include two hollow poles for 2 screws so that the PCB is secured in place. 

You can find the model for the Xtray bracket in the [appropriate project directory](https://github.com/topvint/xtray/tree/main/xtray_v1_3D). 
Please note the LICENSE file explaining the connection between the GPL 3.0 licnese for this project and the CC BY-SA license of the original bracket. 

## 2 - The Xtrax PCB

Gerber files for the PCB are included in the [appropriate project directory](https://github.com/topvint/xtray/tree/main/xtray_v1_gerbers) You should be able to use these files in your favourite PCB manufacturer, although 
I have only used PCBWay. In my case, I didn't have to change any of the default options.

The circuit is designed to use the DVD power socket in the Xbox motherboard. This socket can output 12v and 5v in multiple pins. The Xtray PCB v1 uses 5V.

This is the Bill of Materials you need to build the Xtray v1:
- 1x PHD 2.0 double row (2x7p) socket. [These are the ones](https://www.aliexpress.com/item/1005007314635111.html?spm=a2g0o.order_list.order_list_main.35.6f8d180213O5Cc) I have used before.
- 1x RM-065 100Ohm variable resistor to control the intensity of the LED. You can test different values but I tested higher values and I didn't like the control range they provided. [These are the ones](https://www.aliexpress.com/item/1005006046392789.html?spm=a2g0o.order_list.order_list_main.11.76361802tLf6zl) I used before.
- 1x 2512 SMD 22ohm resistor. This resistor provides base protection for the LED to ensure that it never gets more intensity that it can handle, regardless of the value of the variable resistor. My calculations indicated that peak power going through the resitor could reach circa 700mW, so I went for a 1W resitor, which requires a 2512 form factor. I might be wrong, but better safe than sorry. [These are the ones](https://www.aliexpress.com/item/32750817685.html?spm=a2g0o.order_list.order_list_main.41.76361802tLf6zl) I have used before.

_A word on attribution:_ While you are welcome, as per the license, to modify the PCB to suit your needs, **please maintain attribution in the silk screen** by keeping the Topvint name, website and logo. I'd prefer for it to be kept visible once installed,
but if you would like to add your own logo or name, and there is no apace, I'm happy with moving the logo or website to the back of the PCB as long as some form of attribution is visible in the front of the PCB.

## 3 - The LED strip

These are sometimes referred as LED filament, LED noodles, etc. They are available in multiple colours. The main thing here is that it needs to be 300mm long and needs to take 3 volts. That lenght is just enough to reach around the 
faceplate ticht enough so that it is self-supporting, and thread into the back of the bracket through the provided holes. Please note the positive and negative pins of the LED strip when you thread it and solder it to the Xtray PCB. 
In all the products I have used, the positive side is denoted by a small hole in the pin.

You can find these LED strips anywhere these days and but [these are an example](https://www.aliexpress.com/item/1005006707119591.html?spm=a2g0o.order_list.order_list_main.16.76361802tLf6zl) of the ones I have used before. 

## 4 - The cable

The Xtray is powered by the DVD power socket in the Xbox motherboard, and so the cable needs to be compatible with that. I used the same socket in the Xtray PCB for simplicity, but theoretically you could put any socket you wanted at
that end. Only the 5v and ground pins are used, so that's a lot of cables that you don't need. You could build your own cable and only use two wires, but if you prefer to buy pre-made cables (as I do), look for PHD2.0, double row, with
7 pins in each row (sometimes referred as 2x7P). I use "same direction" at both ends, but it doesn't really matter that much as the cable is long and can be twisted.

In terms of length, you need around 25cm to reach from the socket to the Xtray PCB, perhaps a bit less. I haven't found pre-made cables of 25cm so I use 30cm. They are a bit too long, but as there is a lot of space inside the Xbox now that
the drive is gone, it is completely fine. Obviously if you make your own cables, make sure to meassure the distance and do whatever suit best. 

If you are going to buy the cable pre-made, [this is an example](https://www.aliexpress.com/item/1005007668822342.html?spm=a2g0o.order_list.order_list_main.23.76361802tLf6zl) of the ones I have used before. 

## 5 - The screws

The Xtray bracket is designed to hold the bottom part of hte Xtray PCB in place, but in order to be secured at the top, there are two small screw holes which are there to screw the PCB to the bracket. This is not a perfect method,
and ideally you would want to have metal inserts, pre-threaded plastic studs, etc. However, right now it works with 2x M2 self-tapping screws of 5mm length. [These are the ones](https://www.aliexpress.com/item/1005007607752228.html?spm=a2g0o.order_list.order_list_main.99.76361802tLf6zl) I have used before. 

# Assembly

The assembly of the Xtray PCB just requires you to solder 4 components i.e. 
- The socket (throgh hole). The only difficuly here is to make sure that you position this in the PCB in the right way, as that would dictate which pin gets the 5V power. Please check the photos but essentially, the indentation of the plastic needs to be closest to the bottom of the Xtray PCB. That will ensure that, when inserted, the 5V comes out in the right pin. 
- The variable resitor (through hole). Again, please make sure you orient the component in the right location for the variable resistive path to be in the right pins. Check out the photos, but when the resistor is turned to its middle possition, the top pin in the PCB should align with the number in the resistor (i.e. 101 for 100Ohm), which will dictate the position of the other two pins. 
- The 22ohm resistor (SMD). It doesn't matter how you solder this component. 
- The LED strip (SMD). As mentioned above, just make sure you solder the positive pin to the pad marked with a "+" in the Xtray PCB.

Once the PCB is assembled and you have printed the bracket, thread the two ends of the LED strip through teh right holes i.e. looking at the bracket from the back, leftmost hole for the possitive end of the LED strip (the one with a small hole), and rightmost hole for the negative side of the strip. Thread most of the LED strip so that you have space to manouver your PCB and soldering iron. Pre-tin the LED pads in the PCB as it will make your lef easier when soldering the LED strip terminals. Solder each LED terminal to around half way of its length, as this will give you just enough space for ensuring the PCB sits confortably in its allocated place and can also help the LED terminal flex slightly if necessary. Screw the PCB using the two self-tapping screws, but do not tighten it too much as it will need to be unscrewed again for installation. 

# Installation 

The Xtray still needs the original faceplate of the Xbox DVD drive, which slids in place thanks to the design of the bracket. The LED strip is long enough to sit tight around the faceplate, but in order to have enough room to loop it around teh faceplate once installed, is best to unscrew the PCB from the bracket first. Alternatively you could install the faceplate first, then thread the LED strip and then solder it to the PCB. In any case, if you decide to put the faceplate at the end (for example, because you are preparing this for somebody else who has to provide their own faceplate but don't want to do teh soldering), or you have been provided a pre-soldered Xtray without a faceplate, please follow these instructions: 

- _To get to the DVD Drive:_
  - Open up your Xbox using a T20 TORX screw driver. There are 4 screws under the rubber feet, and two additional screws under the stickers.
  - With the console in the upright positions, remove the top part of the shell by just pulling upwards
  - With a T9 TORX screw driver, uncrew the screw joining up the HDD and DVD trays, as well as the two screws holding the DVD drive tray to the front part of the console
  - Unplug the grey IDE flat cable and yellow power cable from the DVD drive. Unplug the yellow power cable also from the motherboard.
  - Unplug the power Molex cable from the HDD drive and unthread it from the HDD tray so that you can lift up the HDD tray
  - Once the HDD tray is partially lifted, you will have enough room to lift the DVD drive tray. Remove the DVD drive from the console
  - Re-sit back the HDD tray to the original position, threading back the power cable on the side, and pluging back the Molex power cable into the HDD
- _To harvest the faceplate from your DVD drive and install it into the Xtray:_
  - Remove the DVD drive face plate by pulling gently from the bottom of the faceplate while pushing upwards. If its more confortable, you can use a tool to help you. The faceplate is secured in place by a couple of plastic clips which hold it in the tray. It will be obvious once you take a look.
  - In order to insert the faceplate in the Xtray bracket, unscrew the Xtray PCB to ensure there is as much slack as possible of the LED strip. Move the strip to one side and carefully slide the faceplate from the top until it clips in place. - Then loop the LED strip around the inserted faceplate. The kit is designed to keep the LED strip tight around the faceplate while giving just the right amount of slack to loop it while the Xtray PCB is unscrewed. Therefore is a tight fit but it is not difficult. However please be careful as the LED strip is delicate.
  - Make sure the LED strip is tight around the faceplate so that the Xtray PCB can sit in the right place in order to be screwed back
- _To install the Xtray into the Xbox:_ 
  - Screw the Xtray bracket in place of where the DVD drive used to sit before you removed it, using the same screws to secure it in place
  - Connect the provided power cable to both the Xtray PCB and the DVD drive power connector in the Xbox motherboard.
  - Turn on the console and adjust the brightness of the LED by inserting a flat screw driver in the potentiometer installed in the Xtray PCB. The circuit is designed not to exceed the maximum power that the LED strip can handle (100mA) no matter how much you turn it.
  - When you are happy with the britghness level, put back the top of shell and screw it back in place.
  - Turn off the lights during gameplay and enjoy your OG Xbox!
