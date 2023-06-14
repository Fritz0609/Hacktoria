# @author:Fritz0609

_**Contract: Undercover Hunt**_

June 2023

Link: https://hacktoria.com/contracts/undercover-hunt/


![instructions](https://hacktoria.com/wp-content/uploads/2023/06/undercover-hunt-1536x1024.jpg)

_**Briefing**_

Greetings, Special Agent K.

You have been assigned the task to help the SISU with geolocating the pictures provided by Styx. We have little information about the criminal organization, but we believe they might want to stage an attack against sites located in western Europe.

As always, Special Agent K. The Contract is yours, if you choose to accept.



_**Materials and Answer Instruction**_


For each image, write the city in lowercase with no whitespace and no accent on letters.

Answer Format	  city1_country1_city2_country2_city3_country3_city4_country4
Answer Example	kiev_ukraine_london_unitedkingdom_saopaulo_brazil_istanbul_turkey

The following 4 pictures where provided:

image 1: ![image1](https://hacktoria.com/wp-content/uploads/2023/06/undercover-hunt-Image1-1536x1152.jpg)  
image 2: ![image1](https://hacktoria.com/wp-content/uploads/2023/06/undercover-hunt-Image2-1536x1152.jpg)  
image 3: ![image1](https://hacktoria.com/wp-content/uploads/2023/06/undercover-hunt-Image3-1536x1152.jpg)  
image 4: ![image1](https://hacktoria.com/wp-content/uploads/2023/06/undercover-hunt-Image4-1536x1152.jpg)  




_**Approach**_

Since there were no hidden messages in the briefing, it should be a classical geolocation challenge. 
First, I took a look at all 4 pictures and a first work thesis came up right away. It looked like all 4 pictures were taken from a passenger seat on the right side of a commercial flight. The small parts of the airplane that are in the picture, looked alike, so I guessed that the pictures were made during one and the same flight. Since the flight altitude was lower on images 1 and 4, my thesis was that the sequence of the images fit the flight.
Image 1 probably taken shortly after departure, and image 4 was taken during the landing approach.


I started to take a closer look at image 1, turned it 90 degrees and made a reverse image search without any results. I noted the golf resort, close to the beach, in front of a city (probably with an airport, which is not in the picture) and the highway. There should not be too many locations with that setting. I started a normal Google Maps discovery.
In the briefing, Western Europe was mentioned, so I started to look at the Canaries and after that, at the Iberian Peninsula. I searched for airports first on one screen:

![airport](https://github.com/Fritz0609/Hacktoria/assets/133924856/d0450dd1-fe06-4131-ba3e-6dbde81eded7)


zoomed in on the airports starting at Lisbon and searching for golf courses around the airport, going counterclockwise from airport to airport. In Malaga, Spain I found the golf resort from the picture right next to the airport and had the geolocation for image 1. 

![golf](https://github.com/Fritz0609/Hacktoria/assets/133924856/1467495c-3047-45b1-a2ae-72b43a00f19e)


I checked the destinations from Malaga airport, noticed that there are 150 in all directions. So that won't help much for now.

I then took on image2 and had a closer look there. 
The city is in the red square, with a big canyon right in front of it and four white spots around. I thought that the white stuff should be quarries and that you would see them on sat images from Google Maps much better than the canyon. So I tried to find those. 
The surroundings looked like mountains, and there was not much green in the picture. My guess was the mountain line north of Malaga: the Sierra Nevada.

Since there are a lot of quarries there, it didn't work to scroll over Google Maps, therefore I switched to Overpass Turbo and looked for a pattern of multiple quarries close to a city. Checked a couple of spots on Google Maps, but couldn't find the location from the image.

![overpass](https://github.com/Fritz0609/Hacktoria/assets/133924856/a985001e-ab3a-4801-b013-f7ee062ded03)

After maybe 30 minutes looking around, I decided to go on to the next picture.


I reversed image searched the wild rivers with a lot of bends and checked multiple rivers and I learned that there are a lot more rivers that have not been straightened than I thought.

I decided to go on to image 4 without losing more time.

![image4](https://github.com/Fritz0609/Hacktoria/assets/133924856/06a619da-10b9-4119-90cd-72bf153c339c)

As you can see in the image, several things caught my attention. And I worked them through one after the other. 
1. There seems to be a 180 degree river bend behind the city, or maybe there are two rivers coming together. From the image you can't really tell. But the river and the city seemed to be big, so I manually took a look at big cities with a big river that came to my mind. Like Paris, London, Florence, Prague, Budapest, ... None of those were a fit. I googled for "180 degree river bend city" and "horseshoe bend city" but had no luck there.
2. I noticed 5-7 bridges. So I googled  "city with 7 bridges" (Porto), "city with 6 bridges" (Kaliningrad) and "city with 5 bridges" (Ljubljana) and checked the results. No luck.
3. The big white building structure gave me no clue, but I noticed the lake with a bridge over it, or was it a forest? I googled and even asked ChatGPT what cities have a lake with a bridge. Tons of results, but no luck here either.
4. Next I noticed the stadium, thought about it as a normal sports stadium, but wondered why the tracks were not round. So I had the idea it might be a horse racecourse and searched for that. That did the trick, and the hippodrome in Bordaeux, France matched. The part in the red square was Cubzac-Les-Ponts, France.



![horse](https://github.com/Fritz0609/Hacktoria/assets/133924856/e0cd8d49-18e4-438b-80cc-11087e346a8d)

      

Knowing the departure and arrival airports now it was quite easy to geolocate image 2 and 3. I went to flightradar24.com, opened a replay of a flight from AGP to BOD, zoomed in on the flight route and looked on the side of the route for the specific landmarks.

![flightradar](https://github.com/Fritz0609/Hacktoria/assets/133924856/2858fdda-3d77-4df5-a0b2-6f8f6b7174a7)

There was the city of image 2 with the big canyon next to it and a quarry on the other hand: Villacañas, Spain.

![foundimage2](https://github.com/Fritz0609/Hacktoria/assets/133924856/a61110b2-3aec-4a25-9fbc-5969e4c323d4)


And there was the small town in the river bend: La Estación, Spain!

![foundimage3](https://github.com/Fritz0609/Hacktoria/assets/133924856/3b366029-c1bc-4ffb-88e2-2e03820070eb)

Now I had everything I needed to build together the passcode for the flagfile and it worked:

![Contract Card - Undercover Hunt](https://github.com/Fritz0609/Hacktoria/assets/133924856/c81f1462-cda3-4db1-98d4-4454b6862d66)


_**My socials:**_ <br>@ twitter: twitter.com/Fritz0609
