# Creative-Making-Final-Project
## Week 5 Project Proposal
### Concept
I owned a cat back in Taiwan but couldn’t bring him here, whenever I feel lonely I would think about him. I think it’s better for me to have a pet here to keep my company but sometimes I travel around so I couldn’t take care of it all the time. It’s better to create a mechanical pet rather than owning a real one.<br>
[C++ code](https://git.arts.ac.uk/20032092/Creative-Making-Final-Project/blob/main/221207finalCode.ino)<br>
[Youtube Video](https://www.youtube.com/watch?v=bXSrquHCi6g&ab_channel=hanhsunshih)
<!--![IMG_5681](https://git.arts.ac.uk/storage/user/604/files/6c6fcad7-b8fb-4d0d-b7fe-4fbc4602f0e8)-->
<!--![IMG_6582](https://git.arts.ac.uk/storage/user/604/files/b29acf7b-bc1d-4315-921b-3a4d054a79d5)-->
<img src="https://git.arts.ac.uk/storage/user/604/files/6c6fcad7-b8fb-4d0d-b7fe-4fbc4602f0e8" width="600">

I like a calm pet as my cat so a mechanical pet combined with both plant and animal‘s characteristic might be great.

 ![Untitled_Artwork](https://git.arts.ac.uk/storage/user/604/files/a6b3e383-e150-497a-a18d-f42a6888aafe)
In my riginal idea, I wanted to make an interactive pet that could be placed next to a computer or a windowsill. The base is a heavy cuboid, and an object similar to a flower bud is suspended by an elastic steel wire. It will change its shape with the light. When it detects someone nearby with an infrared sensor, it will emit light of different colors and have A motor drives him to spin.

![Untitled_Artwork 2](https://git.arts.ac.uk/storage/user/604/files/016eabf8-af61-4a30-84e6-e98d945f419a)


## Week 6(11/7-11/11)
### confirm the housing and order materials
This week I identified all the materials I would end up using and then designed the base according to the space they would take up. After I went to school and borrowed all related tools and components, I made the following adjustments:
- I decided to change the base into a larger cuboid, because it will be much larger if all the components are assembled together and the wires are added.
The linear actuator itself is too long, and its size is larger than I expected, so I changed it from the original fishing shape to a flower that grows upright.
- The servo motor was used to rotate the whole device, but it was too small to drive enough, so it was changed to design a smaller object next to the original main flower bud, and the servo motor would respond when a person was detected.
- I wanted to use an infrared sensor to detect whether there are people around, but later I changed it to a sound sensor to detect the volume of the surrounding area, and then change the color of the light and drive the servo motor under certain conditions.
![Untitled_Artwork 3](https://git.arts.ac.uk/storage/user/604/files/ab0b2cd0-6294-40ff-b832-32fdc5c9ca9a)
- INPUTS: light detect sensor, sound detect sensor
- OUTPUTS: linear actuator, neopixcel strips, servo motor

## Week 7(11/14-11/18)
### L289N Motor Driver
I used L289N Motor Driver to control if the linear actuator should stretch or curtail by some simple function.
Before that, I try to motivated a AC motor first.
I used L289N Motor Driver to control if the linear actuator should stretch or curtail by some simple function
![w7L289NMotor](https://git.arts.ac.uk/storage/user/604/files/172a5eca-fe6f-4c9e-9a5b-152dda23f9c6)
https://www.youtube.com/watch?v=PZqGPCIGEM0&ab_channel=hanhsunshih


### laser cutter
I booked an induction to learn how to use laser cutter and cut some components for making housing
![w7laserCutter](https://git.arts.ac.uk/storage/user/604/files/fa32b7c5-9b63-4678-8b25-5b16f760676f)
![IMG_5733](https://git.arts.ac.uk/storage/user/604/files/a0d3822a-0f38-4c88-a38f-9021e3a0c51e)
![IMG_5734](https://git.arts.ac.uk/storage/user/604/files/1a16815f-2203-4773-855d-957c3bc5e0c6)


## Week 8(11/21-11/25)
### sound detection sensor to ultrasonic sensor
This week I changed my mind from using sound detector into using ultrasonic sensor since I found that sound detection sensor was not accurate as ultrasonic sensor
![w8L289N_pushActuator](https://git.arts.ac.uk/storage/user/604/files/88923f60-20c6-4935-b792-3ec7457e77bc)
- https://youtu.be/PZqGPCIGEM0?t=13
For the coding, I classify different distance it detects into 5 categories, and use switch statement to change the light colour.
```
for(int i=0; i<NUMPIXELS; i++) { 

     switch(scale)
  {
    
    case 0:
      pixels.setPixelColor(i, pixels.Color(255, 0, 0));//red
      pixels.show();
      break;
    case 1:
      pixels.setPixelColor(i, pixels.Color(255, 128, 0));//orange
      pixels.show();
      break;
    case 2:
      pixels.setPixelColor(i, pixels.Color(255, 255, 0));//yellow
      pixels.show();
      break;
    case 3:
      pixels.setPixelColor(i, pixels.Color(0, 255, 0));//green
      pixels.show();
      break;
    case 4:
      pixels.setPixelColor(i, pixels.Color(0, 0, 255));//blue
      pixels.show();
      break;
    
    }
    
  }
```


### colorMixingLamp
I would like to install lights on my machenical pet and was trying to figure out if it's better to install RGB LED or neopixcel strips
- https://youtu.be/PZqGPCIGEM0?t=6
- https://youtu.be/PZqGPCIGEM0?t=26
```

```

- https://youtu.be/PZqGPCIGEM0?t=36

### challenges overcome
After tasking using L289N to motivate AC motor, I tried to use it to motivate lineat actuator.
Also this week I spent lots of time on coding which has a purpose to control how long should linear actuator stretch or curtail due to light data.
- I first write down the process of how it might work and also the structure of the code.

<img width="618" alt="截圖 2022-12-06 18 29 12" src="https://git.arts.ac.uk/storage/user/604/files/fc31d16a-8975-48bd-84ee-5091a076ab94">

- then I did some calculate to understand the reletivity between datas

![IMG_5648](https://git.arts.ac.uk/storage/user/604/files/a07e7fd0-0269-4908-b8f5-5b945ab696a9)
<img width="540" alt="截圖 2022-12-06 18 29 23" src="https://git.arts.ac.uk/storage/user/604/files/1912ecec-fcd7-475d-a135-3558dc57c246">

At the beginning, I can only use the simplest function to control its elongation or shortening.
Later I added the concept of time. I set the initial straight to let it stretch at the beginning, and then calculate the length change through subtraction, use the positive and negative numbers to judge whether it should be stretched or shortened, and then convert it into the corresponding running time, and finally use the map method to correspond to the correct running value.
<img width="625" alt="截圖 2022-12-09 11 26 54" src="https://git.arts.ac.uk/storage/user/604/files/f905766a-0517-42be-96d9-77c169f30fe5">



### Circuit diagram
I had confirm the circuit disgram this week!
![circuit](https://git.arts.ac.uk/storage/user/604/files/3586c014-96b1-4a05-b55c-2781511c9692)

## Week 9(11/28-12/2)
### solder
![IMG_5643](https://git.arts.ac.uk/storage/user/604/files/161282b8-b809-41f0-a49c-6bffbcc07d50)

![IMG_5647](https://git.arts.ac.uk/storage/user/604/files/5f13f3e7-f68b-47ee-a599-942df02021da)

### Neopixcel test
![w9material_neopixcelStrips](https://git.arts.ac.uk/storage/user/604/files/1c2d9563-f824-4508-84ab-4f4cad038384)
https://youtu.be/PZqGPCIGEM0?t=46

### Servo test
https://youtu.be/PZqGPCIGEM0?t=57

### Material test
![w9materialTest1](https://git.arts.ac.uk/storage/user/604/files/29f69ecf-9bc6-475c-807a-d73636b9be41)
- I ordered a PVC material with polarized refraction, which will produce rainbow-like and colorful refraction according to the viewer's viewing angle, which is more varied and exciting than other materials.
![w9materialTest2](https://git.arts.ac.uk/storage/user/604/files/7971aab8-aa8a-4fe8-85f2-4feeb68cc436)
- I also used this material to make the smaller object besides the main object, the idea was inspired by lawn
![w9materialTest3](https://git.arts.ac.uk/storage/user/604/files/45b499d1-bb8e-4573-a768-3575aa992d40)
https://youtu.be/PZqGPCIGEM0?t=52


## Week 10(12/5-12/9)
### housing 
I prefer clay then plastic materials as my base since organic meterail has more connection to nature. I made a short fence along the edge of the base plate, and made a lot of clay curved surfaces on the cover part. They have more organic vitality than flat surfaces. When you touch them, your fingers fit right into the concave surface, like a fluffy envelope when I touch my cat.
In addition, I also considered that when the Arduino and L289N are plugged in, they will light up red and yellow respectively, and the gap in the base allows those lights to pass through, presenting a charming light and shadow.
![w10housing1](https://git.arts.ac.uk/storage/user/604/files/0ce85000-6f65-4c69-ad96-4905fcfc8ae6)
![w10housing2](https://git.arts.ac.uk/storage/user/604/files/d4525b52-2cd6-4706-bb0b-ceec6273883f)
![IMG_5650](https://git.arts.ac.uk/storage/user/604/files/3b0e420f-adc5-4670-a19c-e57025bafe33)
![IMG_5652](https://git.arts.ac.uk/storage/user/604/files/9da20984-462c-4f55-b3b8-1b1558d6cd93)
![IMG_5653](https://git.arts.ac.uk/storage/user/604/files/59112f94-9c10-4220-bdcb-d730f6339b06)
![IMG_5668](https://git.arts.ac.uk/storage/user/604/files/29590d68-f7c6-4b8f-ae5f-a59305c84d79)




### Final outcome
![IMG_5681](https://git.arts.ac.uk/storage/user/604/files/6c6fcad7-b8fb-4d0d-b7fe-4fbc4602f0e8)
Last but not least, light colour is the thing I can carefully consider so when the light inflect from the transparent rainbow film it comes different effects. Instead of pure red, yellow, blue, etc, I found out that slightly adjust every peremeter in RGB will make the light softer, lower satuation cause more comfortable environment for human eyes.
```
Color(75, 10, 0));//red 
Color(75, 30, 0));//orange
Color(75, 30, 0));//yellow
Color(10, 75, 15));//green
Color(35, 10, 50));//blue
```

![IMG_5697](https://git.arts.ac.uk/storage/user/604/files/8f1a3df1-cd06-4f4c-afb7-f21eace57df3)
![IMG_5710](https://git.arts.ac.uk/storage/user/604/files/f4487531-eca0-4cea-814c-9d005cbae863)
