---
tags: [configuration, gear/console]
---
Important Soundboard Operation Notes:
1. If channel gain is adjusted it effects gate, compressor, Computer, narthex, and main
2. 



**04-27-25 -** 
Turned down Cong. A. gain to +41 for Organ
OBS: 35 - 21db
Audacity: 35 - 20db
Set pastor at +47, +48
Set Organ to +45

**5-4-25**
set pastor to +51, gate threshold down to -44 from -43
pastor to narthex is -3.00, cong. is 0.00 no change from last week

PM - Chris Engelsma
Settings:
- Input:
    - A. Gain: +42
    - D. Gain: +5
- EQ:
    - Yes
- Dyn 1 - Gate
    - Thresh: -44
    - Range: -14
    - Attack: 1m
    - Hold: 110m
    - Decay: 1.07
- Dyn 2 - Compressor
    - Thresh: -32
    - Ratio: 4.0:1
    - Attack: 18m
    - Release: 89.2m
    - Out Gain: +6.0
    - Knee: Soft
- Sends:
    - Computer: -3.00
    - Narthex: -3.00
Saved channel as ENGELSMA  





Dynamics:
Organ vs. Piano
Pastors Mic position
Guest Pastor
Lapel vs. Head worn vs Pulpit




### *TODO List*
Make new labels for custom keys
rust desktop 
burn down list
DESKTOP-KVRCAAH name of Audiotech Computer
Setup VLANs
Change Guest name and have every one use that
## *Network List*
Default
Guest
Iot
reformedifc
Surveillance (change to security)
## WiFi Networks
IFC Guest open
IoT wpapsk
ReformedIFC wpapsk
Send logs to gray log through TailScale





### Check list:
- OBS 
    - Dropped Frames
    - Stream on
    - Disk Space
- Audacity
- Computer speakers vol down
- Sermonaudio
- Facebook
- Youtube
- DM3 recording
- Video Recording?
- Camara Framing for both
- Camera Color
- Wide Focus



Starting Service
Ending Service
Running Service
Uploading video
Editing sound/export MP3



### Starting a Service
- Turn on audio equipment in cabinet
- Turn on Yamaha DM3 mixing console
- Turn on both cameras
- Log in to computer and open
    - Audacity
    - Open Broadcast Studio (OBS)
	- Open Firefox to:
	  - SermonAudio.com
	  - Youtube.com
	  - Facebook.com
- Setup streaming (see Setup Stream Section)
- When music starts turn on congregation mic
- Click start stream at: 
  - AM Service Stream starts at 9:21am
  - PM Service Stream starts at 5:21pm


### Ending a Service
- At end of sermon Stop recording in Audacity
     - Save Audacity recording. Use the format MM-DD-YYAM/PM
        - Example: 05-04-25PM
    - Stop Video recording in OBS is needed
    - Stop DM3 recording
- At end of service
    - Click fade to black in OBS
    - Stop OBS stream
    - Turn off Cong. mic. all channels except Computer, Narthex, and Main
    - Upload sermon
    - Turn off both cameras
    - Turn off cabinet
    - Turn off DM3
    - Restart computer



## Setup Stream 

#### Start Streaming to Sermonaudio.com
Open OBS
select am or pm preroll and fade it to Program
Check sound level in OBS audio Mixer is between -30 and -20 db
Turn on cong. mic when music starts
set vol for narthex after mic is turned on
Click start streaming
Watch OBS as stream starts and check for
    frames missed due to rendering lag
    Skipped frames due to encoding lag
    Dropped Frames (Network) 
Navigate to https://www.sermonaudio.com/dashboard/
Click on webcast
Under live Webcast check the stream health
At this time streaming to sermonsudio is complete the Fellowship hall and Nursery  tvs can be started

#### Starting stream to facebook and youtube
Navigate to facebook
in the top right conner select the account icon and go to Immanuel fellowship
Click on live Video at the top of the right column 
Click golive to open config
Under Streaming software setup drop down advanced setting and verify Persistant stream key is toggled on
Close advanced drop down
Navigate to you tube
youtube should be logged in as immanuelfellowshipchurch6015@gmail.com
In the top right conner click on create then go live
Navigate back to sermon audio to get sermon title and description
Click on sermons find sermon and click on it
copy full title 
go back to face book and click on 'What's your live video about?'
Paste title of sermon in title
go back to sermon audio and copy description
go back to facebook and paste description in description
click save
For youtube click edit and paste the title and description and click save
Navigate back to Webcasts on the sermonaudio dashboard
sccroll down to Multicast channels 
Click start on the facebook and go back to facebook
when stream is established click go live.
watch facebook until it starts something turns green or red
go back to sermon audio and click start on youtube 
navigate to you tube. you tube starts streaming automatically verify it does
check stream health on OBS, facebook, and youtube through out the service

When music stops and Pastor starts to walk to the pulpit to start the service push teh G1 key to fade to the close shot
Turn on pastors mic then turn off cong when pastor begins to speak
on DM3 Check A. gain and make adjustments if need at the beggining of service
Check channel settings on pastors channel


