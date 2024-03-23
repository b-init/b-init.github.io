<!-- NEED MORE PICS -->

# 1st Prototype - Built Sept 2022

![flub2](https://gist.github.com/assets/55803927/42a8431e-66c0-463b-959e-4c950159043e)

The idea of making a custom split mechanical keyboard is not new. There are a LOT of designs available on the internet you can build [awesome-split-keyboards](https://github.com/diimdeep/awesome-split-keyboards). But I wanted to design one specific to my needs and opinions, with the physical placements of the keys being according to my hands and the key layout being in line with how I use my computer.

Another perk of having a keyboard like this is that you don't have to worry when using other people's keyboard, you can carry your layout with you (as long as its portable).

## The building process
<!-- software -->

![flub_layout](https://gist.github.com/assets/55803927/b0b9fa16-0e35-475f-a9a3-8adc0bbfc932)

After deciding the key layout (which is inspired from my old [PinkyProtector layout](https://github.com/b-init/Chest_o_AutoHotKey_Scripts?tab=readme-ov-file#the-pinkyprotector)), I started building a firmware using qmk and programming in the keymap. A few more modifications to ensure proper operation on the microcontroller I used and only defining the pins was remaining, which had to wait until I actually built and wired everything up.

<!-- hardware -->

![canvas_layout](https://gist.github.com/assets/55803927/1de772d2-258d-407a-98d5-8d2cb944e2cf)

I started by tracing my natural finger movements onto a piece of paper, clicking a picture and importing the imgae into Fusion360 and scaling it to match its real size using reference measurements. The sockets for the mechanical keys were then added according to the traced image. After keeping space for the microcontroller screw sockets, wires and so, multiple designs were made before I finalized this round design with a appealing sharp chamfer.

![flub_cad](https://gist.github.com/assets/55803927/46baf627-3a53-4899-8e2b-357002935629)


Now the printing... I had to print several iterations to get the dimensions just right for the switches to fit snugly, even had to sand down some sockets since they were not all the same due to my slightly distorted printing bed. 

![flub3](https://gist.github.com/assets/55803927/9bc1f292-523c-4af3-9594-f5c0dc85a068)

Next was soldering, slightly challenging but really fun! there's something meditative about soldering. 

Defining the pins, compiling and uploading the firmware was next and then the first prototype was done! it worked just as expected (this half anyway).

![flub4](https://gist.github.com/assets/55803927/aa0531d8-542c-4d52-8d9d-700f0e5bf026)


## About the other half...

A significant step while designing split keyboards is deciding how the two halves will communicate. All the wires from the switches can be extended directly to the other half but there are a lot of wires and it would be pretty easy to mess the wiring up pulling on those wires. So generally, another microcontroller is used to manage the other side and i2c or some other form of communication is used between the halves. 

The only problem with this is that you have to use two microcontrollers, though this is a very popular method and it'll be pretty easy to set up. I didn't have another pico at the time (and maybe even communication between 2 picos wasn't supported in qmk yet) so I wanted to use some io expanders (or use a cheaper, smaller microcontroller as one) but I ended up taking a break from this project after making one half. 

I hope I will get back to this project sometime (or start building an entirely new split keyboard! I have some ideas)

<!-- --------------------------------------------- -->

<sup><sub> \*No AI was used in the making of this blog.</sub></sup>
