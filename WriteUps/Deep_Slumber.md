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

The second step was to extract the ZIP file and start to look at the material:
![Screenshot 2023-06-04 003255](https://github.com/Fritz0609/Hacktoria/assets/133924856/a0ba431b-7a22-43c7-afda-1843a6b87060)

1. Breach Plan.pdf did not open in Adobe Reader, so I figured there is something going on with the file.
2. checksum hold the MD5 checksums of the other 2 files. Since I haven't seen that before in a material ZIP file, I figured it would be part of the solution (which it wasn't)
3. sat_016231.png showed a screenshot from a satellite image of a location. I thought it would be out of Google Maps (which it wasn't -> that was a bad mistake, since I compared a lot of Google Maps locations later on to the picture and dismissed them because of not matching colors of the environment. I figured out a lot later, that the colors in Google Maps were totally different)

So where to start? I decided to take a look at the PDF first and opened it in an HEX Editor:
![HxD1](https://github.com/Fritz0609/Hacktoria/assets/133924856/aa91393d-5765-444c-a597-f700528aea4d)

I recognized it as an ZIP file due to the "PK" Flag at the beginning, so I changed the file extension to .zip and was able to extract the file "Breach Plan.png" which showed a hand behind frosted glass. To my notes I added "hand" and "frosted glass". 

![hand](https://github.com/Fritz0609/Hacktoria/assets/133924856/2d2845c7-07a3-489d-ad8e-33edf72fbb80)


After that, I wanted to do a reverse image search with Yandex and dragged the file into the Yandex search bar. Nothing happened. I tried again and it didn't work. I had to do the reverse image search with a screenshot and found the original picture source from Ilona Panych, Sacramento CA on unsplash.com. Didn't seem related to our operation, but I wrote it down in my notes. 

But why didn't the file work in the picture search? Something strange still going on with that picture. I wanted to take a look, made a copy and opened it in the HEX editor, but it looked like a normal PNG file on the first sight. Then I wanted to check the metadata and opened it in ExifTool.

![ExifTool](https://github.com/Fritz0609/Hacktoria/assets/133924856/0231daf1-eeea-453a-b164-b99b5093315a)

I noticed the warning about Trailer data after the PNG IEND chunk. Ok, there is some hidden data behind the PNG. Probably it would be quite a rabbit hole to go down. But since it got late, I didn't want to go on there and decided to take a deeper look at the sat_016231.png before going to bed.

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

"light green-brown landscape" 

"buildings not looking like Africa, maybe a former colony"

So quite a lot to get started with. Since I already had "African coast" in my note, I thought there would probably not being too many big rivers at the African coast. I started Google Maps and looked around. 
I started in the nil delta, zoomed in and out and went west from there, basically around the continent. Zooming in on light green-brown areas with rivers and looking for structures like those small agricultural parcels. Even if I would have found the area at that time, I would have gone over it without recognizing. My approach was made on the consumption that I was looking on a Google Maps screenshot, and that it would look the same on my second screen. 

I searched longer than I intended without a result and went to bed late. 




_**Capture the flag - Day 2**_


I had some time in my lunch break, so I decided to take a look at the operation again. I wanted to examine the hidden data in the PNG file, but first I checked my notes and reread the briefing. Highly recommend that step, whenever you got your head clear, e.g. due to a break, to reread the briefing and your notes. In this case, I stumbled over the expression "a location off one of the African coasts". Since I'm no native English speaker, I wondered if I got the African coast thing wrong. What means "off the coast"? I googled and regretted immediately that I searched the hole continent the night before. 

The PNG file was out of my mind again, and I was into Google Maps again and searched for Islands around Africa.  
In the north mainly the European Islands like Malta, Crete, Cypress didn't seem to fit the story. The ones close to Africa are too small. In the west, the Canary Islands don't have big rivers. Cape Verde and some Archipelagoes are too small - no big roads. In the east I excluded Mauritius (no big rivers) and Reunion (too much mountains), so what was left was Madagascar. I zoomed in and was stunned how many rivers there seemed to be. I switched to OpenStreetMap since you can spot the rivers there better. But the whole island is covered with rivers. I had to change the plan to check in Google Maps all the rivers:

![river](https://github.com/Fritz0609/Hacktoria/assets/133924856/44ac2d00-9e29-4900-912a-f2cfd3a5b0ef)

Instead of the rivers, I checked for the big roads in Madagascar and found out that there are way less big roads than rivers:

![roads](https://github.com/Fritz0609/Hacktoria/assets/133924856/9fb7b669-4cb3-462f-8ce1-068e0d74d9a9)

So what now? I thought for a moment to write an overpass turbo query to check industry buildings, close to big roads, close to rivers in Madagascar, but that would take more time, than I had left in the lunch break.
Manually checking the big roads would be time-consuming as well. And then there was still the hidden data behind the hand PNG. 

That's when I thought maybe the hand picture gave away a clue already, so I googled for "hand" in Madagascar and afterwards for "frosted glass". That gave me three pins, all in the same area:

![maps1](https://github.com/Fritz0609/Hacktoria/assets/133924856/9d15e30a-98c2-4865-b378-4a89c1331916)

I zoomed in and on first sight I saw the Ikopa river with the same strange island in it, exactly like in the picture of our location.  

![maps2](https://github.com/Fritz0609/Hacktoria/assets/133924856/d78a7b89-d1a7-4503-b8cc-2bbafa965695)

I followed the river and found the location I was looking for in seconds:

![maps3](https://github.com/Fritz0609/Hacktoria/assets/133924856/3f0de421-08dd-4a80-8efb-932d7d26f85a)

I tried to extract the flagfile, committed the code on the Hacktoria website and went back to work, already knowing I would come back, because it did feel that I took a shortcut and that there would be more to the PNG file. 
![Operation Card - Deep Slumber](https://github.com/Fritz0609/Hacktoria/assets/133924856/b8896674-a8c6-4dea-9050-6af3f4895153)



_**Follow Up - Day 3**_

I got the flagfile, but it was pretty obvious that I let out some steps that were intended by the creator. So I came back to check the hand PNG again. I already knew that there were some data behind the PNG. I opened the file in an editor and cut out everything after the PNG IEND chunk and pasted it in a new file. I supposed that it would be a ZIP file, so I tried with that extension but couldn't open it. Checked again and recognized it as a Base64 string. I opened an online tool and tried my luck. 
![base64](https://github.com/Fritz0609/Hacktoria/assets/133924856/0d91daa7-a53d-40e6-b455-f12ccfe56b49)

There we have our ZIP file and I could already see that there is a Breach_Plan.pdf inside. But to extract it I would need a password. I tried the stuff I had in my notes. Especially the jail-free-card stuff and the MD5 hashes seemed fitting for me. But non worked. 

Ok, there has to be a password somewhere. So I came back to the hand PNG and tried a couple of filters on that to see if there is hidden information. With Fotoforensics I found a hidden message: 

![fotoforensic](https://github.com/Fritz0609/Hacktoria/assets/133924856/14f39f2e-6572-45df-acb6-a919015f8145)

Ok, there we go. But what does it mean. I tried all those text strings as password for my ZIP file but non worked. I read some online articles about the Polly and its cracker, the Polybius arcade game (very interesting - never heard of it before) and the Greek historian. In the Wikipedia article of the Greek historian, I found information about his invention the Polybius Square for cryptography. That should be it. 

Then I studied the function of the square and tried all kind of variations with the two string lines in the picture to get a password that works. Since I only had text lines I tried to encode the text that I had to get a line of numbers to try as password. I was stuck here for quite some time, thinking decoding would make much more sense, but how without numbers. 

When you get stuck in an investigation, you should ask another person. Since it was in the middle of the night, I asked my buddy ChatGPT what he thought about the two text lines:

![chatgpt](https://github.com/Fritz0609/Hacktoria/assets/133924856/cd43d63b-ec19-4b55-9773-e1072def6ffe)

Oh man, this thing is so good. After ChatGPT opened my eyes and decoded the base64 line to numbers, it was quite easy to find the right password:

![dcode](https://github.com/Fritz0609/Hacktoria/assets/133924856/7f245502-8a42-474f-a074-c48b7f3cb38c)


Now I had a new PDF file, but I was not really satisfied. Knowing the location already, I studied the PDF and didn't find a lot, that would have helped me to figure out the location. 

![newpdf](https://github.com/Fritz0609/Hacktoria/assets/133924856/dd7a78d0-7b00-4eb2-a9cf-fa0f1d2ca9fd)

What jumped to me was the miles to travel - 125mi inland and 600mi NW. So i thought that would be the hint, that it is on a big island and the location is somewhere 600miles NW from the coast. But when I checked the distance in Google Maps, the farthest way to the coast would only be around 485mi.  And if I put a 600mi line from my location to the SE. I ended up somewhere in the Mozambique Channel.   

![distance](https://github.com/Fritz0609/Hacktoria/assets/133924856/686a8526-7266-45bf-ab18-9ba8399acf58)

The second thing was the container number. And I remembered the article on hacktoria.com on maritime OSINT (https://hacktoria.com/articles/maritime-osint-in-detail/) in which was described how to track containers. So I tried, but the result wasn't satisfying either. The container seems to belong to MSC but was located in Houston, US and in Pakistan. Both not related to my location:

![containers](https://github.com/Fritz0609/Hacktoria/assets/133924856/5c551e5a-4441-46cb-9606-35d84412dc9f)


Since I got the flag already. I decided to let the matter rest for now. But I'm looking forward to the end of the month when we can start to discuss the operation on Discord, or when I can read other users write-ups to see if I still missed something here. 

_**My socials:**_ <br>@ twitter: twitter.com/Fritz0609
