# Black hole theory - Research Project

## Introduction
Black holes have fascinated people along of years now, both within the scientific community and among the general public.

But what exactly is a black hole?

It is an object in space with such an enormous mass compressed into a microscopic core that its gravitational force becomes stronger than the speed of light itself. What we usually perceive as its size is actually the surface beyond which light can no longer travel fast enough to escape the black hole’s gravity. This boundary is called the **Event Horizon**.

The goal here is not to pretend to be an astrophysicist, but simply to make it easier to understand how a black hole affects its surroundings through its ultra-dense mass.

## State of the Art
### Little point of history :

<img width="800" height="2000" alt="Black hole" src="https://github.com/user-attachments/assets/33136f12-1985-4d85-a478-83adfe58db17" />

### Different type of black hole :
How do black holes work?

The core of a black hole is called the **Singularity**. The distance at which matter becomes distorted is known as the **Schwarzschild radius**. Then comes the **Event Horizon**, which is the boundary beyond which light is completely absorbed by the black hole. Around it lies the **Accretion disk**, a mass of particles and gas orbiting around the black hole. Finally, there are the **Quasars**, which are the ejection of the accumulated gas.

<img width="736" height="408" alt="image" src="https://github.com/user-attachments/assets/e151442b-7d38-4036-9a9f-74933660f5a7" />

| Black hole type| Characteristic                                                                                                 | Creation |
|----------------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| Primordial     | Black hole, formed at the big bang, which evaporates step by step. It is often associated with the dark matter.|Intense pressure and temperature caused by the big bang.                |
| Supermassive   | Found at the center of galaxies which gives them this spiral shape. They have a mass between 1 million and 40 billion solar masses.|Appear after the explosion of a supernova produced by a massive star.|
| Intermediate   | Refers to a black hole of a few thousand solar masses. Causes the creation of stars clusters.                  |Formed by accretion of stellar objects at the center of stars clusters. |
| Stellar        | With a solar mass between 3M and 14M, they would be the most common in the different galaxies.                 |Collapse of a star on itself upon its death.                            |


### Focus on Sagittarius A* :
Sagittarius A* is the supermassive black hole located at the center of our galaxy. However, observing it directly would normally require a telescope the size of the Earth. That is why, in 2017, a Swedish researcher came up with a revolutionary idea: linking together all the radio telescopes on Earth in order to greatly increase their observational power.

This network became the Event Horizon Telescope, whose objective is to produce a high-resolution image of the accretion disk surrounding a black hole.

<img width="1280" height="956" alt="image" src="https://github.com/user-attachments/assets/e7f431b8-fabd-4525-bb49-37699768a5eb" />

It took almost perfect weather conditions for nearly four days in order to capture the image. The data was then analyzed by three different laboratories, all of which reached the same result, revealing in 2019 the first-ever photograph of a black hole, followed by a clearer version in 2022.

<img width="480" height="480" alt="image" src="https://github.com/user-attachments/assets/13ac6b1d-eaf2-4c94-a10d-96c2d7f453be" /> <img width="480" height="480" alt="image" src="https://github.com/user-attachments/assets/dde538c9-14f8-4358-a6a3-f9a4f97eff14" />


### Midpoint :
It is important to note, even today, many mysteries still around black holes, since they are located at distances that are currently unreachable. In addition, no material could withstand the extreme conditions required to build a machine capable of being sent inside a black hole to study it more deeply, not to mention the enormous amount of power that would be needed to transmit a signal back. However, it is still possible to study black holes by observing the different celestial core and phenomena that around them.

## Approach
Originally, I was supposed to have help from my father, who has a doctora in quantum mechanics, to better understand the different advanced mathematic. Unfortunately, that was not possible due to various health complications.

I therefore had to rely on more accessible versions of these calculations, such as Newtonian mechanics (developed by Isaac Newton) rather than general relativity (developed by Albert Einstein).

Many people before me have explored this subject, whether through simulations written in C++ or through even more advanced scientific studies. However, I primarily wanted something accessible and visual, this is why I chose to create a simulation using Unreal Engine.

After reading several scientific articles and watching a few videos, I decided to focus on four distinct approaches for the simulation of my black hole:
- The Doppler effect on light distortion.
- What would we see if we sent someone into a black hole?
- What would happen to us if we went in there?
- Created a mini galaxy around the black hole.


## Analysis:
### 1. Black hole material
The first step was obviously to create the visual of the black hole around which I would be able to carry out all my experiments. Here is the configuration :

**`MI_Blackhole_Demo :`**

<img width="508" height="624" alt="image" src="https://github.com/user-attachments/assets/931929dc-fc90-425e-8fe6-c8018e7bce31" />

**`BP_BaseBlackhole :`**

<img width="600" height="398" alt="image" src="https://github.com/user-attachments/assets/f909c730-b6a6-4a5c-9749-7c9223f1deee" />

**Result :**

<img width="1152" height="648" alt="download (3)" src="https://github.com/user-attachments/assets/bdd514a6-32cf-444f-81d6-d3285b459ab7" />

### 2. Doppler effect
At the beginning I was really afraid of this part, it seemed complex to me to modify in order to localize the transmission of light in a convincing way on Unreal engine, but for that I have to explain to you how the Doppler effect works or rather the gravitational lens :

To put it more simply, since light is attracted by the black hole at forces that can exceed its speed, the more the passage of the latter is aborted by the black hole, the more the trajectory will be impacted, this can cause the image to be distorted, distorted or even duplicated. Particularly thanks to this, and this is what makes them difficult to spot in space, we can see what is happening behind the black hole. We call it the gravitational lens but it works like the Doppler effect, you know this distortion of the sound depending on whether it is more or less close to you.

<img width="1152" height="648" alt="download (4)" src="https://github.com/user-attachments/assets/4c8c8998-bdf7-41cb-ae57-684e2ebba0e4" />

In reality, I'm just taking the problem the other way around, given that in Unreal Engine materials we can influence refraction and thus recreate a similar effect of distortion of the image that the light sends back to us.
In order to achieve a convincing gravitational lens effect I went through two different materials using refraction.

**`M_Lenssing :`**

<img width="1199" height="551" alt="image" src="https://github.com/user-attachments/assets/3b4e9fc6-2b62-46d1-af05-b98ac5bfa465" />

**`MI_Lenssing :`**

<img width="1509" height="700" alt="image" src="https://github.com/user-attachments/assets/5c47b844-b40f-45ce-87f4-4a6e4b98a179" />


**`M_Distortion :`**

<img width="1709" height="662" alt="image" src="https://github.com/user-attachments/assets/1a2a7fd3-10e1-4271-b0ee-5096d35e1644" />

**Result :**

https://github.com/user-attachments/assets/42e06168-a4c3-4f06-9c99-833c520f9b13

And in particular the light bends so much that it would be possible to see you even if you got close enough to a black hole.

https://github.com/user-attachments/assets/ee4c4032-3e4c-40ad-bf8b-8001e6f2ec7e


### 3. Lunch in black hole

Okay, but so what happens if someone is sent into the black hole? What do we see? Well, as said previously, the light is absorbed by the black hole which will have two major effects:
- The person will appear to be slowing down as they accelerate in their fall, this is because the light takes longer to reach our eyes.
- The light it emits will shift more and more towards the red before completely disappearing.

To apply this affezct I nee to modifie a little bit th master material of character :

<img width="1071" height="761" alt="image" src="https://github.com/user-attachments/assets/1524b9b0-8f12-4300-a7df-5a1b94d5b2bf" />

And for the sake of our experience we will greatly speed up the process and use a timeline to reproduce the desired effect.

<img width="1481" height="700" alt="image" src="https://github.com/user-attachments/assets/007e950c-b8da-4ed7-8500-1d7c48b3dcd3" />

**Result :**

https://github.com/user-attachments/assets/a07a15b6-7990-4106-9aef-21336b12b25e

### 4. Enter in black hole

So for this part we will have to start from several principles if we want to see something: firstly our character must have eyes capable of seeing beyond the speed of light, otherwise he will not even see himself once in the black hole, we will call them Quantum eyes;
then it is important that our character is invincible to resist the force that he will experience once the event horizon passes but especially the heat emitted at the level of the acretion disk.

After which I must tell you about another of my discoveries: the Schwarzschild radius.

The Schwarzschild radius is more precisely the distance where the world light ray can no longer escape and can be written mathematically :

Such as :
- `R` = The Schwarzschild radius
- `G` = Gravitational constant (which for simplification of calculation will in our case be = 1)
- `M` = Mass of balck hole
- `c` = The light speed

<img width="1024" height="720" alt="image" src="https://github.com/user-attachments/assets/64c8763d-9e17-4e52-9c6a-5e8a82679758" />

The problem then arises that the force applied to our feet will be extremely different from that applied to our head. This is what we call the Tidal forces, and when we are subjected to them our body would find itself stretching into a sort of gigantic spaghetti which gave it its name spaghettification.
However, these Tidal forces correspond to 1/M² (the mass of the black hole) which means that the more massive the black hole, the more spaghetification will occur later in the fall.

<img width="1859" height="691" alt="image" src="https://github.com/user-attachments/assets/858cba38-b97c-4b9f-80fa-9857f9769e30" />

**Result :**

https://github.com/user-attachments/assets/3d0ff8a2-f34c-4b20-90db-bb2470ed094d

### 5. Create small galaxy

For the sake of simplify mathematical and optimization limitations, I limited myself to spawning 2000 stars around the black hole using the Newtonian mechanics (developed by Isaac Newton) rather than general relativity (developed by Albert Einstein).

<img width="1592" height="393" alt="image" src="https://github.com/user-attachments/assets/9f8fac69-c84f-43c7-ae69-5be8ddee9ead" />

<img width="1411" height="513" alt="image" src="https://github.com/user-attachments/assets/5e9a722c-2a69-4c68-ab90-86b03024e775" />

Here we calculate the acceleration that the star obtains by subjecting the gravitational forces of the stars around it as well as that of the black hole.

Such as :
- `F` = Acceleration
- `G` = Gravitational constant (which for simplification of calculation will in our case be = 1)
- `M1` and `M2` = Mass of the landing and attracted object
- `d²` = The distance between the two objects squared

<img width="640" height="480" alt="image" src="https://github.com/user-attachments/assets/3b272fc0-d179-4766-bf15-7805dac7b4e4" />

If we whill use general relativity by Einstein we need to use this calculation :

<img width="450" height="112" alt="image" src="https://github.com/user-attachments/assets/9d666a76-d893-4674-bf41-7374db8d8ba9" />

And I optain this result...

https://github.com/user-attachments/assets/337ba106-1e19-4522-9b2d-4fe95399a4c3

I kept turning the question over and over in my head and I didn't understand why it would eject my stars like that. So I dove back into my research and then I found it. I had missed a basic principle: the way in which we are today able to detect the presence of black holes, observing the movement of stars.

https://github.com/user-attachments/assets/a17ce4c5-580d-4bb9-9103-f4461e1622dd

By trying to simulate a galaxy on a small scale and failing, I simply came across something equally persistent in its behavior in a simulation: what happens to stars that survive the absorption of black holes despite being in the close presence of the latter.

Still, my project to simulate a mini galaxy is a failure and here is what could help me in the future to go further:
- Simulate the galaxy in larger proportions to leave more space with the black hole
- Go through the Niagara system so that the stars and their movement are managed by the CPU and thus be able to learn more : https://youtu.be/O674AZ_UKZk?si=aY4cuxLn5en6E1_g
- Use general relativity by Einstein

## Mediagraphy :
### Fun video :
https://www.youtube.com/watch?v=G9KqYVS3OBk _(What happens if you fall into a black hole)_

https://youtu.be/bP1yjgqMA7U?si=Do_4ewcoaM689ygf _(Destroy black hole)_

### Serious video :
https://vm.tiktok.com/ZNRggG5nC/ _(Schwarzschild radius)_

https://youtu.be/IAtObnbdLoY?si=UU9zEzTFT1jXCqgA _(What happens if you fall into a black hole)_

https://youtu.be/dFqjqRUWCus?si=mDF1rR4TzxFlNT8W _(Galaxy simulation)_

https://youtu.be/O674AZ_UKZk?si=aY4cuxLn5en6E1_g _(Galaxy simulation)_

https://www.youtube.com/watch?v=vI4pfWU_zd8 _(What a black hole)_

https://youtu.be/jmXM07nHoQg?si=knlwITwmpJwfZe5l _(Black hole render)_

https://youtu.be/8-B6ryuBkCM?si=EkaDMEZ3vo1rn-rh _(Black hole render)_

### Documentary :
https://www.youtube.com/watch?v=_AR-yX_GIuc

https://www.arte.tv/fr/videos/095857-001-A/le-cosmos-et-les-origines-de-la-vie/ 

https://www.youtube.com/watch?v=R5SD0JtvBDo 

### Articles :
https://www.ias.u-psud.fr/ama09/doc/conf_Riazuelo_AMA09.pdf

https://cnes.fr/dossiers/trous-noirs

https://fr.wikipedia.org/wiki/Trou_noir

https://arxiv.org/search/?query=Black+hole&searchtype=all&source=header

https://link.springer.com/article/10.1007/s00159-024-00154-z?utm_source=chatgpt.com

https://fr.martincid.com/science-2/des-horizons-de-levenement-au-rayonnement-de-hawking-une-exploration-des-trous-noirs

https://www.nasa.gov/universe/what-are-black-holes/

### Scientific publications :
https://blogs.futura-sciences.com/luminet/2026/05/08/la-pertinence-physique-et-mathematique-des-trous-noirs-est-elle-en-question/

https://zelmanov.progress-in-physics.com/papers/zj-2008-03.pdf

https://www.nature.com/articles/248030a0

https://hal.science/hal-02404865v1/file/Akiyama_2019_ApJL_875_L1.pdf

https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.116.061102

https://www.mdpi.com/2073-8994/14/11/2276

### Github : 
https://github.com/achael/eht-imaging

https://github.com/angeluriot/Galaxy_simulation 
