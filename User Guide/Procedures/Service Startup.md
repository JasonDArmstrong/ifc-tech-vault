---
tags: [procedure, service/am, service/pm]
---
# Running the Service

This document covers the full service workflow from walking in the door to shutting down after the last person leaves. Follow the steps in order. Each phase builds on the one before it — skipping steps early causes problems that are harder to fix once the service is live.

**AM stream goes live: 9:21 AM**
**PM stream goes live: 5:21 PM**

---

## Phase 1 — Equipment Startup

Allow at least 20–30 minutes before the service to complete startup and run through the pre-service checklist.

### Power-On Sequence

Turn equipment on in this order. Order matters — the DM3 should be initialized before the computer tries to use it as an audio interface.

1. **Main power switch in the equipment cabinet** — powers the rack equipment
2. **Yamaha DM3** — wait for it to fully boot before proceeding
3. **Both cameras** — Sony wide shot and Canon close shot
4. **A/V computer** — log in and proceed to software setup

### Computer Software Startup

Open applications in this exact order. Audacity must be fully open before OBS launches — if both try to claim the audio driver at the same time, one will fail.

1. **iCUE** — open it and then close it. This initializes the Corsair keyboard and only needs to run briefly.
2. **Audacity** — open and wait until the interface is fully loaded before moving on
    - Confirm the input device is set to the DM3 (not the computer's built-in audio)
    - Check that the input meter responds to audio from the DM3
3. **OBS** — open after Audacity is fully loaded
    - Select the AM or PM pre-roll scene and fade it to Program
    - Set the close camera shot in Preview
4. **Firefox** — right-click the **Stream** folder in the bookmarks toolbar and select **Open All Bookmarks**. This opens SermonAudio, Facebook, and YouTube in tabs simultaneously.

> **Desktop speakers:** Confirm they are on but with the volume turned all the way down. They should never be audible in the room during a service.

---

## Phase 2 — Pre-Service Checks

Work through these checks before the congregation arrives. Fix problems now — not after the stream is live.

### DM3 Audio Check

- Load the correct channel preset for the pastor preaching today
- Check **Analog Gain** on the pastor's channel — verify it matches the saved preset for that mic and speaker combination
- Confirm the **gate threshold** is set correctly — speak into the mic and verify the gate opens cleanly and closes in silence
- Check all channel sends: **Computer**, **Narthex**, and **Main** should all be active. All other channels should be off.

### Wireless System Check

- Confirm the body pack is powered on and paired to the correct receiver (GLXD4 or SLXD4)
- Check **battery level** on the receiver display — replace batteries if below 50%
- Check **RF signal strength** on the receiver — confirm a solid link with no dropouts
- Walk the pastor through the full range of movement they will use during the service and confirm no dead spots

### Camera Check

- Confirm both cameras are powered on and sending video to OBS
- Check **framing** on the wide shot — full congregation view, nothing clipped at the edges
- Check **framing** on the close shot — pulpit centered, appropriate headroom
- Check **color and exposure** on both cameras — they should match. If one looks significantly warmer or brighter, adjust the white balance or exposure on that camera.
- Confirm OBS is receiving video from both cameras and that switching between scenes works

### Stream Setup — SermonAudio

- Navigate to the SermonAudio dashboard and click **Webcast**
- Confirm the stream key is connected and the webcast is ready
- Check **stream health** — this will show as inactive until OBS starts streaming, but the configuration should be correct

### Stream Setup — Facebook

- Navigate to Facebook and go to the **Immanuel Fellowship** page
- Click **Live Video** at the top of the right column
- Click **Go Live** to open the configuration panel
- Under **Streaming Software**, open **Advanced Settings** and confirm **Persistent Stream Key** is toggled on
- Find the sermon title and description on SermonAudio
- Paste the sermon **title** into the Facebook title field
- Paste the sermon **description** into the Facebook description field
- Click **Save** — do not click Go Live yet

### Stream Setup — YouTube

- Confirm YouTube is logged in as immanuelfellowshipchurch6015@gmail.com
- Click **Create → Go Live** in the top right corner
- Paste the sermon **title** and **description** (same as Facebook)
- Click **Save** — YouTube will start streaming automatically once it receives the OBS feed

### OBS Audio Check

- Confirm the audio mixer in OBS is showing signal from the DM3
- At normal speaking volume the meter should read between **-20 and -15 dB**
- Confirm there is no audio from the desktop speakers bleeding into the room

### Audacity Audio Check

- Confirm Audacity is showing input signal from the DM3
- At normal speaking volume the input meter should read between **-24 and -15 dB**
- If there is no signal, check that the DM3 USB cable is connected and the DM3 is selected as the input device

---

## Phase 3 — Starting the Service

### When the Music Starts

- Turn on the **congregation microphone** (Channel 1)
- Set the narthex volume — adjust after the congregation mic is on so you can hear the actual room level in the narthex feed
- **Start Audacity recording** — click the Record button. Confirm the waveform is moving and the level is healthy.
- **Start OBS streaming** — click Start Streaming. Stay on the pre-roll scene until the pastor walks to the pulpit.
- On the **SermonAudio webcast dashboard**, scroll to **Multicast Channels** and click **Start** next to Facebook.
- Navigate to **Facebook** and click **Go Live** when the stream is established. Watch until the indicator turns green.
- Return to **SermonAudio** and click **Start** next to YouTube. Navigate to YouTube and confirm it begins streaming automatically.

### When the Pastor Walks to the Pulpit

- Press the **G1 key** to transition OBS from the wide pre-roll shot to the close pulpit shot
- **Turn on the pastor's microphone** channel on the DM3
- **Turn off the congregation mic** once the pastor begins speaking
- Check the **Analog Gain** on the pastor's channel — confirm levels look correct for this speaker. Adjust if needed at the very start while there is still room to make changes quietly.

---

## Phase 4 — Monitoring the Service

Once the service is live, your job is to monitor and stay out of the way. Most problems announce themselves early. Check these regularly throughout the sermon.

### DM3

- Watch the channel meter — normal speech should sit around **-18 dB** with peaks no higher than **-6 dB**
- If the level is consistently too hot or too quiet, adjust the **channel fader**, not the gain. Gain changes affect the gate and compressor thresholds — fader changes do not.
- Watch for feedback — a rising, sustained tone means the mic is too hot or aimed at a speaker. Pull the fader immediately.

### OBS

- **Audio mixer** should read **-20 to -15 dB** during normal speech
- Watch **Dropped Frames (Network)** — any dropped frames indicate a stream quality problem
- Watch **Frames Missed Due to Rendering Lag** — indicates the computer is under load
- Watch **Disk Space** — confirm there is adequate space for the recording to continue
- Watch **camera color** — if a camera shifts color significantly during the service it may need attention

### Audacity

- Monitor the **input meter** — should read **-24 to -15 dB**
- The waveform should show clear peaks during speech and relative silence between sentences, confirming the gate is working
- If the waveform flatlines, the input signal has been lost — check the DM3 USB connection

### Streams

- Periodically check **stream health** on SermonAudio, Facebook, and YouTube
- Green means healthy. If any indicator turns red or yellow, check OBS dropped frames first — the problem is almost always on the sending side.

---

## Phase 5 — Ending the Service

### At the End of the Sermon

- **Stop Audacity recording** — click Stop immediately after the closing prayer or amen. Do not wait.
- **Save the Audacity project file** using the format: `MM-DD-YYAM` or `MM-DD-YYPM`
  - Example: `05-04-25AM`
- Stop the **DM3 USB recording** if it was running

### At the End of the Full Service

- Click **Fade to Black** in OBS
- Click **Stop Streaming** in OBS
- Turn off the **congregation mic** and the **pastor's mic** on the DM3. Leave the Computer, Narthex, and Main sends active until everything is shut down.
- Upload the sermon audio (see Phase 6 below)
- Turn off **both cameras**
- Turn off the **equipment cabinet** main power
- Turn off the **Yamaha DM3**
- **Restart the computer** — the computer must remain powered on during the week for remote access. After the evening service, restart rather than shut down.

---

## Phase 6 — Post-Service Audio Export

Complete this after the service ends, before leaving.

### Export MP3 from Audacity

1. Open the saved Audacity project file
2. Listen through and trim any significant silence at the very beginning and end
3. Apply effects in this order:
    - **Amplify** — set peak amplitude to **-1 dB**
    - **Compression** — apply standard speech compression settings
    - **Normalize** — normalize to **-1 dB**
4. Export as **MP3**
5. Name the file using the same format as the project: `MM-DD-YYAM.mp3`

### Upload to SermonAudio

- Open **FileZilla**
- Connect to SermonAudio using the FTP credentials in the Logins note
- Transfer the MP3 file — SermonAudio will automatically attach it to the correct service entry
- Confirm the upload completes without errors before closing FileZilla

---

## Phase 7 — Post-Service Video

Video editing does not need to happen the same day and can be done during the week.

1. Open **DaVinci Resolve** and import the OBS recording
2. Add the clip to the timeline on the Edit tab
3. Using the blade tool, cut 2–4 seconds before the pastor begins speaking and 2–4 seconds after the closing amen. Delete the trimmed portions.
4. Normalize the audio: right-click the audio track → **Normalize Audio Levels** → set mode to **ITU-R BS.1770-1** → target loudness **-25 LKFS**
5. Navigate to the Deliver tab and export
6. Upload the finished video to YouTube and Facebook
