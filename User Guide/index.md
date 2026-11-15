---
tags: [reference, training]
---
# IFC Audio/Video Systems — User Guide

This guide covers the audio and video systems used at Immanuel Fellowship Church to support Sunday worship services and live streaming. It is written for the volunteers who run the system each week.

---

## What the System Does

Every Sunday, the A/V system serves two audiences at the same time:

- **The congregation in the worship hall** — microphones capture the pastor's voice, the board processes and amplifies it, and speakers fill the room with clear, consistent sound.
- **Remote listeners and viewers** — the same audio is routed to a computer, combined with camera video, and streamed live to SermonAudio, Facebook, and YouTube. A recording is saved locally for editing and upload after the service.

A secondary speaker feed carries the audio to the narthex and nursery so people outside the worship hall can follow the service.

---

## System Overview

The IFC audio system exists to serve one primary function: make the spoken Word clearly audible to every person in the building, and to anyone listening remotely. Every component in the signal chain — from the microphone clipped to the pastor's ear to the speakers mounted in the worship hall — is in service of that goal. Understanding how sound travels through the system helps you troubleshoot problems quickly, make confident adjustments, and keep the service running without interruption.

Sound moves through the system in a fixed sequence. Each stage receives signal from the one before it, does something to that signal, and passes it to the next. A problem anywhere in the chain affects everything downstream. Knowing this sequence is the foundation of operating and troubleshooting the system.

### Stage 1 — Microphone: Converting Sound to Electricity

Everything begins at the microphone. When the pastor speaks, sound waves cause the microphone's diaphragm to vibrate. Those vibrations are converted into a small electrical voltage — an analog audio signal. The microphone does not amplify; it only converts. The signal it produces is very low in level and must be boosted significantly before it is useful.

The pastor's primary microphone is the **Countryman E6D**, a miniature head-worn condenser microphone worn close to the cheek. Its small size and consistent placement make it the most reliable choice for speech reinforcement. A lapel microphone is available as an alternative when a head-worn mic is not appropriate. A wired **congregation microphone** is also on the system, used to pick up congregational singing and room sound. Unlike the pastor's mics, the congregation mic is plugged directly into the mixing console via a cable — it does not go through the wireless system.

### Stage 2 — Body Pack: Preparing the Signal for Wireless Transmission

The Countryman E6D and the lapel mic both connect to a **wireless body pack transmitter**, a small device typically worn on the belt or clipped inside a pocket. The body pack accepts the microphone's electrical signal, boosts it slightly, and then converts it into a radio signal for wireless transmission to the receiver in the equipment cabinet.

The body pack has a gain trim that sets the input sensitivity — this is a hardware adjustment made before the service and rarely needs to change once dialed in for a given microphone. Setting it correctly ensures the wireless link operates with good dynamic range without overloading the transmitter.

### Stage 3 — Wireless Receiver: Converting Radio Back to Audio

Mounted in the equipment cabinet is the wireless receiver. IFC operates two wireless systems:

The **Shure GLXD4** is a 2.4 GHz digital wireless system. It uses frequency-hopping spread-spectrum technology, meaning it automatically finds and avoids interference from Wi-Fi and other 2.4 GHz devices. The GLXD4 displays received signal strength and battery level for the body pack, and outputs a clean analog XLR signal.

The **Shure SLXD4** is a UHF digital wireless system operating in a licensed spectrum band. It provides very low latency and high dynamic range. Like the GLXD4, it outputs an analog XLR signal to the mixing console.

Both receivers output a line-level or mic-level analog signal over a standard XLR cable that runs directly into the Yamaha DM3 mixing console. The receiver is the bridge between the wireless world and the wired signal chain. Once the signal leaves the receiver, the rest of the system is entirely wired.

### Stage 4 — Yamaha DM3: Processing and Routing

The **Yamaha DM3** is the center of the system. All input signals — the pastor's wireless mic, the congregation mic, and any other sources — arrive here, and all output destinations are controlled from here. The DM3 is a digital mixing console, meaning it converts analog input signals to digital, performs all processing in the digital domain, and converts back to analog for outputs that require it.

When a signal enters the DM3 on a channel, it passes through a processing chain in sequence:

**Input Gain** is the first and most important control. The gain stage amplifies the incoming signal to a level that fills the DM3's internal processing headroom without clipping. Gain is set by ear and by the meters — the goal is for normal speech to read around -18 dB on the channel meter, with peaks reaching no higher than -6 dB. Setting gain correctly at the start of the service is critical because every other processing stage downstream depends on it.

**High-Pass Filter (HPF)** removes low-frequency content below a set cutoff point. For a speaking voice, this is typically engaged around 80–120 Hz to roll off handling noise, HVAC rumble, and the low-frequency buildup that comes from close-mic proximity effect. The HPF makes the vocal sit cleaner in the mix without affecting intelligibility.

**EQ (Equalization)** shapes the tonal character of the signal. The DM3 provides four parametric bands per channel. In practice, EQ is used correctively — to reduce harshness in the upper midrange, tame boxiness in the low-mids, or add presence to a voice that sits back in the mix. A well-set channel often needs very little EQ; it is not a substitute for correct gain and good mic placement.

**Dyn 1 — Gate** is a noise gate. It works by silencing the channel when the signal falls below a set threshold. When the pastor is speaking, the signal exceeds the threshold and the gate opens; when he stops, the signal drops, and the gate closes, cutting off background noise, room reflections, and bleed from other sources. The threshold must be set carefully — too high and it clips words, too low and it fails to gate at all.

**Dyn 2 — Compressor** controls dynamic range. A speaking voice naturally varies in level — some words land loud, others are soft. The compressor catches peaks that exceed its threshold and reduces their level by a set ratio, bringing the overall dynamic range under control. The result is a voice that sits more consistently in the mix and is easier to listen to over the course of a long sermon. After compression, makeup gain restores the average level so the fader position does not need to change.

After processing, the fader controls the channel's contribution to the mix outputs. The DM3 then routes the processed signal to multiple destinations simultaneously.

### Stage 5 — Outputs: Where the Signal Goes

The DM3 sends the mixed signal to three independent destinations at the same time.

**Main Mix to the Worship Hall** — The primary mix output leaves the DM3 on balanced XLR cables and feeds the main power amplifier. The amplifier raises the signal from line level to speaker level — enough electrical power to drive the loudspeakers in the worship hall. The speakers convert the amplified electrical signal back into acoustic sound. This is the sound the congregation hears in the room.

**Mix Bus to the Narthex and Nursery** — A separate mix output on the DM3 feeds a secondary PA amplifier that powers the overflow speakers in the narthex and nursery. This feed is independently leveled from the main mix, allowing the tech to set an appropriate volume for those spaces without affecting the worship hall.

**USB Audio to the Computer** — The DM3 connects to the A/V computer via USB and presents itself as a USB audio interface. The computer receives a stereo mix from the DM3 as a digital audio stream. This feed is used simultaneously by Audacity for recording and by OBS for streaming. The USB send level is controlled from within the DM3 and is independent of the main fader, meaning the tech can adjust the house volume without changing the recording or stream level.

### The Recording and Streaming Path

Once the audio reaches the computer over USB, it splits into two parallel workflows.

**Audacity** captures the incoming audio as an uncompressed WAV file throughout the service. The tech monitors the input meter throughout the sermon to confirm the signal is arriving, not clipping, and not dropping. At the end of the sermon, Audacity is stopped and the file is saved. After the service, the audio is trimmed, normalized, and exported as an MP3 for upload to SermonAudio.

**OBS** runs simultaneously and receives the same USB audio feed alongside live video from two cameras — a Sony wide shot and a Canon close shot. The tech switches between camera angles during the service. OBS streams the combined audio and video live to SermonAudio's webcast, Facebook Live, and YouTube Live simultaneously.

After the service, the recorded video is edited in **DaVinci Resolve** — trimmed, with audio normalized to broadcast standards — and uploaded to YouTube and Facebook as the permanent archive recording.

### How the Pieces Depend on Each Other

The **gain structure** set on the DM3 affects every downstream destination equally — the house speakers, the narthex feed, the recording, and the stream all receive the same processed signal. If the gain is wrong, everything is wrong. Getting the gain right before the service starts is the single most important technical task.

The **DM3 USB send** is a separate mix level from the main fader. This means the house volume and the recording/stream volume can be balanced independently. If the house is loud but the stream sounds low, the USB send level on the DM3 is the right place to look — not the main fader.

The **wireless receivers** are upstream of everything. If a receiver loses signal or the body pack battery dies, no amount of adjustment on the DM3 will restore audio. Battery level and receiver signal strength should be checked before every service and monitored throughout.

The **congregation mic** adds ambient room sound to the mix. It is off at the start of the service and turned on when the music begins. It should be turned off when the pastor begins preaching. If it is accidentally left on during the sermon, it will increase reverb and intelligibility problems in both the room and the stream.

---

## Guide Sections

| Section | What It Covers |
| --- | --- |
| [[Components/Equipment Registry\|Equipment Registry]] | Every device: model, serial number, purchase date, status |
| [[Components/Yamaha DM3\|Yamaha DM3]] | Mixing console — channels, EQ, dynamics, presets, USB recording |
| [[Components/Shure GLXD4\|Shure GLXD4]] | Digital wireless system — setup, gain, frequency management |
| [[Components/Shure SLXD4\|Shure SLXD4]] | Digital wireless system — setup, gain, pairing |
| [[Components/Microphones\|Microphones]] | Countryman E6D, lapel mic, congregation mic — placement and care |
| [[Components/Cameras\|Cameras]] | Sony and Canon cameras — settings, framing, remote operation |
| [[Components/Computer and Capture Cards\|Computer and Capture Cards]] | Hardware overview — Elgato HD60, Black Magic Intensity |
| [[Software/OBS\|OBS]] | Streaming setup, scenes, monitoring, multi-platform stream |
| [[Software/Audacity\|Audacity]] | Recording, saving, exporting sermon audio |
| [[Software/DaVinci Resolve\|DaVinci Resolve]] | Video editing, audio normalization, export, upload |
| [[Software/Streaming Platforms\|Streaming Platforms]] | SermonAudio, Facebook Live, YouTube Live — workflow and monitoring |
| [[Procedures/Service Startup\|Service Startup]] | Step-by-step from walking in to going live |
| [[Procedures/Service Shutdown\|Service Shutdown]] | From final amen to powering down |
| [[Procedures/Quick Reference Card\|Quick Reference Card]] | One-page cheat sheet for running the service |
| [[Procedures/Volunteer Training\|Volunteer Training]] | Onboarding path for new techs |
| [[Configuration/DM3 Channel Config\|DM3 Channel Config]] | Saved channel settings for each speaker and mic scenario |
| [[Configuration/GLXD4 Config\|GLXD4 Config]] | Current GLXD4 settings |
| [[Configuration/SLXD4 Config\|SLXD4 Config]] | Current SLXD4 settings |
