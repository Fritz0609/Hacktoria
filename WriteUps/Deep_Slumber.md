# @author:Fritz0609

_**Operation: Deep Slumber**_

June 2023

Link: https://hacktoria.com/operations/operation-deep-slumber/


![instructions](https://hacktoria.com/wp-content/uploads/2023/06/operation-deep-slumber-v6-1536x1024.jpg)

_**Briefing**_

Greetings, Special Agent K,

We stand on the precipice of an immensely serious situation. The encrypted file in our custody is a proverbial Pandora’s box, filled to the brim with undisclosed dangers. According to Maksim, it harbors Ahemait’s sinister plans, including a location off one of the African coasts.

Your expertise in cryptanalysis has repeatedly proven invaluable to our intelligence division. In this pressing scenario, your distinct abilities are crucial. The stakes are towering, and time is a commodity we’re running short of.

The mission ahead of you is daunting. You are being asked to identify the location and decrypt the file. Each strand you unravel will surely lead us closer to exposing Ahemait’s scheme. It’s imperative that we unearth their intentions and neutralize any threats in advance.

Once we have tangible intelligence, we can mobilize our field agents to circumvent any looming attack. Your deductions will be critical to this counter-operation. Remember, according to Maksim the lives of many are at stake, and that Ahemait’s plan will bring with it potential destabilization of unknown magnitude.

Utilize all your resources. Any algorithm or strategy you can think of or create to unravel this plan should be used. We are here to collaborate with your teams as needed.

As always, Special Agent K. Best of luck with this operation.



_**Materials and Answer Instruction**_


1 – Figure out the answer to the Operation

2 – Construct the password using instruction below to unlock the “flagfile”

3 – Use the “answer code” from “flagfile” to submit your score via the “answer submission form”

Download the FLAGFILE

Download the MATERIAL


Answer Format	  businessname-industry-name-of-street

Answer Example	exxon-petrochemical-iguana-general-way



_**Approach - Day 1**_

I started late in the evening on the first day of the operation, so I would not have had to much time, but I wanted to get started anyway. First I read the prologue and the assignment and wrote down some keywords in my notes:
"corrupt document", "get-out-of-jail-free card", "Ahemait",  "African Coast", "the enemy of my enemy is my friend",  "cryptanalysis".

Second step was to extract the ZIP file and start to look at the material:
![Screenshot 2023-06-04 003255](https://github.com/Fritz0609/Hacktoria/assets/133924856/a0ba431b-7a22-43c7-afda-1843a6b87060)

1. Breach Plan.pdf did not open in Adobe Reader, so I figured there is something going on with the file.
2. checksum hold the MD5 checksums of the other 2 files. Since I haven't seen that before in a material ZIP file, I figured it would be part of the solution (which it wasn't)
3. sat_016231.png showed a screenshot from a satelliet image of an location. I thought it would be out of Google Maps (which it wasn't -> that was a bad mistake, since I compared a lot of Google Maps locations later on to the picture and dismissed them because of not matching colours of the enviornment. I figured out a lot later, that the colours in Google Maps where totaly different)

So where to start? I decided to have a look at the PDF first and opend it in an HEX Editor:
![HxD1](https://github.com/Fritz0609/Hacktoria/assets/133924856/aa91393d-5765-444c-a597-f700528aea4d)

I recognized it as an ZIP file due to the "PK" Flag at the beginning, so I changed the file extension to .zip and was able to extract the file "Breach Plan.png" which showed a hand behind frosted glass. So I added "hand" and "frosted glass" to my notes. 

![hand](https://github.com/Fritz0609/Hacktoria/assets/133924856/2d2845c7-07a3-489d-ad8e-33edf72fbb80)


After that I wanted to do a reverse image search with Yandex and dragged the file into the Yandex search bar. Nothing happend. I tried again and it didn't work. So I did the reverse image search with a screenshot and found the original picture source from Ilona Panych, Sacramento CA on unsplash.com. Didn't seem related to our operation, but I wrote it down in my notes. 

But why didn't the file work in the picture search? Something strange still going on with that picture. So I wanted to have a look, made a copy and opend it in the HEX editor but it looked like a normal png file on the first sight. Than I wanted to check the meta data and opend it in ExifTool.

![ExifTool](https://github.com/Fritz0609/Hacktoria/assets/133924856/0231daf1-eeea-453a-b164-b99b5093315a)

I noticed the warning about Trailer data after the PNG IEND chunk. Ok there is some hidden data behind the PNG so that is probaly a rabbit hole to go down. But since it got late I didn't want to go on there and decided to have a deeper look at the sat_016231.png before going to bed.

![SAT](https://github.com/Fritz0609/Hacktoria/assets/133924856/34d05839-5c9e-454a-a568-f38b56737991)

I wrote down:

"white industry building" 

"second building next to it"

"river with strange islands" "river is big but not navigable"

"small street between building and river" 

"big street next to it with exit and right-hand traffic"

"other industry buildings on bottom"

"village or mine in bottom left"

"a lot of small agricultural parcels"

"green" 

"buildings not looking like Africa, maybe a former colony"

So quite a lot to get started with. Since I allready had "African coast" in my note I thought there would propably not beeing to much big rivers at the African coast, so I started Google Maps and looked around. 
I started in the nil delta zommed in and out and went west from there, basicly around the continent. Zooming in on light green-brown areas with rivers and looking for structures like those small agricultural parcels. Even if I would have found the area at that time I would have gone over it without recognizing. My approach was made on the consumption that I was looking on a Google Maps screenshot, and that it would look the same on my second screen. 

I searched longer than I intended without a result and went to bed late. 




_**Capture the flag - Day 2**_


I has some time in my lunch break so I decided to have a look at the operation again. I wanted to examin the hidden data in the PNG file, but first I checked my notes and reread the briefing. I highly recommend that step whenever you got your head clear, e.g. due to a break, to reread the briefing and your notes. In this case I stumbled over the expression "a location off one of the African coasts". Since I'm no native English speaker I wonderd if I got the African coast thing wrong. What means "off the coast"? I googled and regreted immediately that I searched the hole continent the night before. 

So the PNG file was out of my mind again and I was into Google Maps again and searched for Islands around Africa.  
In the north mainly the European Islands like Malta, Crete, Cypress didn't seem to fit the story. The ones close to Africa are to small. In the west the Canary Islands don't have big rivers. Cape Verdes and some Archipelagoes are to small - no big roads. In the east I exluded Mauritius (no big rivers) and Reunion (to much mountains), so what was left was Madagascar. I zoomed in and was stunded how many rivers there seemed to be. So I switched to OpenStreetMap since you can spot the rivers there better. Since the whole island is covered with rivers I quit the plan I had to check in Google Maps all the rivers:

![river](https://github.com/Fritz0609/Hacktoria/assets/133924856/44ac2d00-9e29-4900-912a-f2cfd3a5b0ef)

Instead of the rivers I cecked for the big roads in Madagascar and found out that there are way less big roads than rivers:

![roads](https://github.com/Fritz0609/Hacktoria/assets/133924856/9fb7b669-4cb3-462f-8ce1-068e0d74d9a9)

So what now? I thought for a moment to write an overpass turbo query to check industry buildings, close to big roads, close to rivers in Madagascar, but that would take more time, than I had left in the lunch break.
Manually checking the big roads would be time consuming as well. And than there was still the hidden data behind the hand png. 

Thats when I thought maybe the hand picture gave away a clue already, so I googled for "hand" in Madagascar and than for "frosted glass". That gave me three pins, all in the same area:

![maps1](https://github.com/Fritz0609/Hacktoria/assets/133924856/9d15e30a-98c2-4865-b378-4a89c1331916)

So I zoomed in and on first sight I saw the Ikopa river with the same stange island in it, exactly like in the picture of our location.  

![maps2](https://github.com/Fritz0609/Hacktoria/assets/133924856/d78a7b89-d1a7-4503-b8cc-2bbafa965695)

So i followed the river and found the location I was looking for in seconds:

![maps3](https://github.com/Fritz0609/Hacktoria/assets/133924856/3f0de421-08dd-4a80-8efb-932d7d26f85a)

So I tried to extract the Flagfile, comitted the code on the Hacktoria website and went back to work, allready knowing I would come back, because it did feel that I took a shortcut and that there would be more to the PNG file. 
![Operation Card - Deep Slumber](https://github.com/Fritz0609/Hacktoria/assets/133924856/b8896674-a8c6-4dea-9050-6af3f4895153)


_**Follow Up - Day 3**_





I did it and got the contract card:





_**My socials:**_ <br>@ twitter: twitter.com/Fritz0609
