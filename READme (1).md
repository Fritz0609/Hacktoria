# @author:Fritz0609

_**Challenge Description**_

![instructions](https://hacktoria.com/wp-content/uploads/2023/05/withering-lotus-web.png)

Briefing
Greetings, Special Agent K

Thalia was able to pinpoint the organization responsible for her Valentine’s Day tragedy. Information has been conveyed to LeRoux, a red team counsel member who has infiltrated the location where the leader of The High Guard may be on vacation. Your mission is to assist LeRoux in obtaining the BSSID of the wifi utilized for 70th-floor interchanges. We have sent you a map to assist you in your search.

As always, Special Agent K, the contract is yours, if you choose to accept.

![Map](https://hacktoria.com/wp-content/uploads/2023/05/Map-Withering-Lotus.jpg)

First thing I did was making an revers image search for the map and found this map of the Yokohama Landmark Plaza Tower. 

![LanmarkTower](https://github.com/Fritz0609/Hacktoria/blob/Withering-Lotus/Screenshot%202023-05-18%20011801.jpg)

I looked around in Google Street View a bit but found myself only in the lower floors. So I wanted to check whats located on the 70th floor. So I looked for a floor map and found this nice overview which told me that the floors 49th - 70th are used by the Yokohama Royal Park Hotel. The Sky Lounge Sirius and the banquet rooms Auora and Rainbow are located there. 

![Floors](https://www2.yrph.com/wp-content/uploads/2023/04/map-500x550.jpg)

So I searched the internet for the hotel or the Lounge Sirius combined with SSID, WIFI, BSSID but found nothing usefull. So I trasnlated WIFI to Japanese and searched again. With that search I found an japanese forum which told me, that the SSID used by the hotel would be "ROYALPARKHOTEL".

![SSID](https://github.com/Fritz0609/Hacktoria/blob/Withering-Lotus/Screenshot%202023-05-18%20013107.jpg)

But how shoud I get the BSSID from the SSID. A quick internet search brought me to the site https://wigle.net/. There you can look up specific WIFI networks at one location. So I tried the BSSID I found there for the ROYALPARK SSIDs but non worked. I figured since it is the top floor and not the area with normal rooms there might be a special SSID so I looked throug the other SSIDs in the area an tried the BSSID from the SSID Wi2premium_club, which worked:

![SSID2](https://github.com/Fritz0609/Hacktoria/blob/Withering-Lotus/Screenshot%202023-05-18%20013820.jpg?raw=true)

I did it:



_**My socials:**_ <br>@ twitter: twitter.com/M3tr1c_root <br>@ instagram: instagram.com/m3tr1c_r00t/
