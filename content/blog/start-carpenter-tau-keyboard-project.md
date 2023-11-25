---
title: "Crafting Cool: Unveil the Carpenter Tau Keyboard Project!"
date: 2023-11-24T08:41:11+08:00
---

There is a wide range of high-quality mechanical keyboards available that offer an exceptional typing experience. Personally, I have a particular fondness for keyboards made from carved wood. However, there is a drawback when it comes to the software and connectivity options that these keyboards provide. None of them offer all three features: open source capability, Tri-mode connectivity, and programmability. To address this issue, I took the initiative to create a prototype keyboard that combines the elegance of wood, Tri-mode connectivity, and plan to open source it as I continue enhance the programmable software aspect.

**Why wooden**
Now, you might wonder why I specifically chose wood as the material for this keyboard. As a modern-era worker who spends hours typing each day, it's much more enjoyable to type on a keyboard with a natural solid wood touch rather than a plastic keycap surface. Just like how you prefer writing on a solid wood desk over synthetic materials, this keyboard is designed to cater to those who share the same sentiment.

Hard wood cases and keycaps are solid and as precise as metal objects. Paint it with wood wax oil can protect it from mold, moist and decay that make it durable for many years just like your wooden house and furniture.

Additionally, wood is an environmentally friendly material. Even when it eventually worn out, it is naturally disposable and doesn't harm the environment.

**Tri-mode, Open Source Programmable: Let's Get Fancy**

Now, let's talk about the exciting features of this keyboard: Tri-mode connectivity, open source capability, and programmability. When you purchase a high-end proprietary keyboard from renowned manufacturers like Logitech and Razer, they often come with Tri-mode connectivity, which includes wired, Bluetooth, and 2.4GHz options. However, open source keyboards on the market only offer wired and Bluetooth connectivity, lacking the 2.4GHz option. The key difference lies in latency. Bluetooth has a heavier stack, resulting in a minimum 10ms latency even for the fastest Bluetooth keyboards. Open source hobby projects can have higher latency. This difference becomes noticeable, especially for gaming purposes. With the fastest 2.4GHz keyboard, the latency can be reduced to 1ms, allowing for 1000 keystrokes per second, which is on par with a wired keyboard.

![Unique feature of Tau Keyboard](/images/taukeyboard-feature.png)

Apart from latency, other factors such as battery life and the absence of a Bluetooth receiver in some desktop computers also contribute to the preference for 2.4GHz connectivity. While major open source keyboard firmware claims doesn't offer 2.4GHz connectivity is based on a proprietary keyboard, as a software engineer, I can assure you that implementing a fast, single-purpose protocol on top of raw 2.4GHz data transmission is not as difficult as it may seem. It's comparable to developing an efficient messaging protocol on top of UDP or QUIC. In my prototype experiment, I was able to achieve a stable 1ms transmission latency using two low-cost 2.4GHz chips, without relying on any proprietary RF protocol. As a high-quality keyboard, I believe it's important not to compromise in this aspect.

Now, you might wonder why you should choose an open source keyboard over a big brand one that also offers Tri-mode connectivity. Well, apart from the obvious benefits of Tri-mode connectivity, open source keyboards provide enhanced security, configurability, and programmability, thanks to the contributions of the open source community. There are already excellent high-level abstractions such as QMK, VIA, and ZMK projects available.

**The name Carpenter Tau Keyboard**

Let's move on to the name of this keyboard: Carpenter Tau Keyboard. During my travels, I had the opportunity to meet some incredibly skilled carpenters who demonstrated their ability to craft well-built keyboard cases, keyplates, and even precise objects as small as keycaps. This inspired me to explore the idea of using hardwood as the ideal material for creating a durable and comfortable keyboard. Combining their craftsmanship with my coding and electronics skills, I successfully built a prototype. To my surprise, it gained significant popularity among my colleagues and friends after several weeks of testing. Encouraged by their positive feedback, I decided to make these keyboards available to a wider audience, hence the name Carpenter Tau. 

![Prototype Carpenter Tau Keyboard](/images/61key.jpg)

As for the name "Tau", it is derived from the sound of one of the best carpenters, Mr. Tao, in my town. I chose to associate it with the Greek letter "Tau" to symbolize the ancient history and wisdom of carpentry, while also ensuring it is easy to pronounce for English speakers.

**The name Carpenter Tau Keyboard**

Finally, I am excited to announce the Carpenter Tau Keyboard project. In addition to the advantages of 2.4GHz and Tri-mode connectivity, as well as open source programmability, I have separated the wooden design from the firmware/PCB design for the Tri-mode keyboard. The underlying firmware/PCB design is named Tau Keyboard and is also open sourced to meet the common needs of a Tri-mode programmable keyboard. This allows anyone in the keyboard community to build their own keyboard directly from it, make modifications, or reference its good parts. If you're interested in learning how a professional-grade keyboard is built, I encourage you to follow this project. You'll witness the entire process of creating the first open source Tri-mode keyboard, from start to finish!

You can stay updated on the project's progress through the accompanying blog series. Whether you choose to build one yourself or wait for a [pre-built option on Crowd Supply](https://www.crowdsupply.com/fangbo/carpenter-tau-keyboard), I hope you'll find the Carpenter Tau Keyboard project intriguing and worthwhile!
