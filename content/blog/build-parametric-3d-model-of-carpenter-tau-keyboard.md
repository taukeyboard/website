---
title: "Build Parametric 3d Model of Carpenter Tau Keyboard"
date: 2023-11-26T10:14:41+08:00
---

In this blog post, we will be constructing the complete 3D model of a keyboard. While we won't delve into all the intricate details necessary for production, we will provide you with the final 3D model in STP format. This will give you a good overview of the keyboard's appearance. When it comes time for production, we will revisit this topic and provide a step-by-step guide to help you accurately build a keyboard that can be manufactured.

# Find the keycap metrics


To find the keycap metrics, we can explore the various keyboard models available on the internet. It's quite convenient to obtain the metrics or the geometric details by downloading and importing a STP format model. I would choose OEM sized key and use [this one](https://www.thingiverse.com/thing:4542301) as the the reference metrics. 

Then we are going to import the STP format model in a parametric 3D CAD software. The reason of doing so, you can create a parametric version of the keycap that allows for adjustments such as the thickness of the border. This ensures a perfect fit for the keyboard while ensuring sufficient strength with the wooden material. Also, this can make our live easier when carving the wood. In this post, I will be using Creo Parametric as the CAD software.

# Build the keycaps

Import the STP model and create a solid extrusion. Then, carefully trim the solid extusion with curved objects until they match the exact shape of the STP file.

![Single key](/images/1u_r1_keycap.jpg)

Note that each row in the keyboard has a slightly varying height, specifically referred to as R1, R2, R3, and R4. It is important to draw each of the R1-R4 as a seperate 3D model. [This one](https://www.thingiverse.com/thing:4542301) provide the STP models for each row. Additionally, keys such as `Shift`, `Space`, and others are wider in size. By utilizing parametric design, we have the flexibility to easily adjust their width according to the desired specifications. We will be constructing the standard 61, 87, and 104 key models, so it's quite easy to find which key is which R and what it's the width:

![Reference layout](/images/104key-layout.webp)

# Build the keyboard plate

Now we need a plate to hold all the keys. Since we are building the standard layout keyboard, this can also be found online, for example, download and import [this plate](https://www.thingiverse.com/thing:5322836) and import to Creo.

# Build the case

The process is simpler and more relaxed compared to the keycap. You have the flexibility to adjust it according to your preferences and create an aesthetically pleasing rectangular box that can accommodate the keyboard plate therefore all the keys. It's important to note that the case is designed to be taller at the back for added comfort, and you can take inspiration from any keyboard at hand to determine the appropriate angle.

![Case](/images/case.jpg)

# Assemble

Before comming to assemble all the parts, we need a key switch to attach keycap onto the plate. We'll use pretty standard MX type switch. We can find an [open source MX switch model in OpenSCAD format](https://gitlab.com/gcb/3dump/). Since we don't need to customize it, so we just download a [STP version](https://www.thingiverse.com/thing:421524) and import it to Creo.
Now, we have the ability to generate an assembly file within Creo Parametric and accurately position all the keycaps on the plate. Then plate on the case. And we're done!

![Assembled](/images/assemble.jpg)

# Build the optional palm rest
Optionally, we can also build the option a palm rest, which is essentially a rectangular box with a curved surface designed to provide a comfortable resting place for your palm.

![Palm rest](/images/palmrest.jpg)

# Render it
Import the file into a rendering software, like KeyShot, and apply the desired wood material. Then, proceed to render it to achieve a realistic representation.

![61 key 3D Rendering](/images/keyboard61.jpg)

# 87 key and 104 key model

The 87 key and 104 key variants are essentially same as the 61 key one, but comes with a larger case and more keys. Also we need to create a upper case because these models don't have keys fully covered the keyboard plate.

![87 key 3D Rendering](/images/keyboard87.jpg)

![104 key 3D Rendering](/images/keyboard104.jpg)



