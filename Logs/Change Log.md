---
tags: [log]
---
# IFC Vault — Project Change Log

## Session Summary — 2026-06-07

### Project Goal
  
Build a complete, well-organized documentation system for the audio/video tech team at Immanuel Fellowship Church (IFC). The vault serves volunteers who run sound and live streaming every Sunday. The primary deliverable is a **User Guide** — a set of documents that covers the full A/V system from component-level technical reference through step-by-step operational procedures. The guide will be published locally as a webpage for easy access on-site.

A secondary goal is a **maintenance and configuration tracking system** — structured notes that capture current equipment settings, log deliberate changes, and record maintenance events so the system state is never lost when volunteers change.

---
### What Was Found at the Start of the Session

The vault already contained scattered documentation in several locations:

- `Sound System/IFC Sound System Users Guide/` — a partial user guide with a good DM3 operations manual, a microphone overview (generic, not IFC-specific), an Audacity job aid, and signal path documentation describing a pre-DM3 signal chain that was no longer accurate.
- `Workbench/` — operational notes including Sunday service reports (dated logs going back to July 2025), soundboard adjustment notes, a rotation schedule, a task list, and a checklist stub.
- `Projects/` — a continuous improvement/gear wishlist, a video editing stub, and a training folder.
- `Random Notes/` — a Statement of Faith, Windows admin notes, and markdown examples.
- `zz_assets/Templates/` — one daily notes template used to create each Sunday report.

Key problems identified:

- Signal path documentation described the old system (MX400 era — Focusrite interface, Samson compressor). The Yamaha DM3 was installed December 2024 and replaced most of that outboard gear.
- The Shure SLXD4 wireless receiver is new and completely undocumented.
- No single source of truth for service procedures — steps were scattered across Tasks.md, Adjustment Notes, and How to Start AudioVideo.md.
- No equipment registry, maintenance log, or change tracking system.
- Canvas Manual folder in the Users Guide contained mostly empty stub files.


---
  
### Changes Made This Session
  
#### 1. Archived Outdated Content

Created `Archive/` at the vault root. Moved the following into it:

- `Archive/Old Signal Path Docs/Sound Processing Path.md` — described the pre-DM3 signal chain (Focusrite, Samson compressor, MX400 routing). No longer accurate.
- `Archive/Old Signal Path Docs/New Sound System path.md` — identical content to above, both were present.
- `Archive/Yamaha MX400/Drawing 2024-06-16 09.40.02.excalidraw.png` — Excalidraw diagram of the MX400 signal flow. Equipment retired December 2024.

Nothing was deleted — all content is preserved in Archive for reference.
#### 2. Created the User Guide Structure

Created `User Guide/` at the vault root with the following folder structure and empty placeholder files:


```

User Guide/
├── index.md                          ← landing page (written)
├── Components/
│   ├── Equipment Registry.md         ← written (template/starter)
│   ├── Yamaha DM3.md                 ← empty
│   ├── Shure GLXD4.md                ← empty
│   ├── Shure SLXD4.md                ← empty (undocumented new gear)
│   ├── Microphones.md                ← empty
│   ├── Cameras.md                    ← empty
│   └── Computer and Capture Cards.md ← empty
├── Software/
│   ├── OBS.md                        ← empty
│   ├── Audacity.md                   ← empty
│   ├── DaVinci Resolve.md            ← empty
│   └── Streaming Platforms.md        ← empty
├── Procedures/
│   ├── Service Startup.md            ← written (full service runbook)
│   ├── Service Shutdown.md           ← empty (content folded into Service Startup)
│   ├── Quick Reference Card.md       ← empty
│   └── Volunteer Training.md         ← empty
└── Configuration/
    ├── DM3 Channel Config.md         ← empty
    ├── GLXD4 Config.md               ← empty
    └── SLXD4 Config.md               ← empty
```

  
Note: A `Logs/` folder was created but the user moved it to the vault root level during the session. It is not inside `User Guide/`.

#### 3. Documents Written


**`User Guide/index.md`** — Landing page for the entire guide. Contains:
- Brief introduction to what the system does and who it serves
- Full system overview written in prose — walks through the signal chain from microphone to speakers in five stages (microphone → body pack → wireless receiver → Yamaha DM3 processing chain → three simultaneous outputs), then covers the recording/streaming path and a closing section on how the pieces depend on each other
- Navigation table linking to every document in the guide

**`User Guide/Components/Equipment Registry.md`** — Starter template for the equipment inventory. Organized into sections: Microphones, Wireless Systems, Mixing Console, Amplifiers and Speakers, Cameras, Computer and Capture, Networking, Accessories, Software, and Retired/Disposed. Pre-populated with known equipment from existing vault notes. Many serial numbers and exact models are blank — data gathering required. The user filled in the SLXD4 purchase year (2026) and confirmed body pack models during the session.


**`User Guide/Procedures/Service Startup.md`** — Comprehensive service runbook covering the full Sunday workflow in seven phases:

1. Equipment startup (power-on order, software launch order)
2. Pre-service checks (DM3, wireless, cameras, stream setup for SA/FB/YT)
3. Starting the service (congregation mic, Audacity, OBS, Facebook/YouTube go-live sequence, G1 pulpit transition)
4. Monitoring (DM3 meters, OBS, Audacity, stream health — with specific dB targets)
5. Ending the service (Audacity stop/save with naming format, OBS fade/stop, power-down sequence)
6. Post-service audio export (Audacity amplify/compress/normalize/MP3 export, FileZilla FTP upload)
7. Post-service video (DaVinci Resolve trim, normalize to ITU-R BS.1770-1 at -25 LKFS, export, upload)

**`README.md`** (vault root) — Short repository description written for the GitLab repo. Describes the vault purpose, five main sections, tools used, and a contributing note.

#### 4. Updated the Daily Notes Template

`zz_assets/Templates/template-daily-notes.md` was updated to merge the service checklist into the existing template. The template now produces a Sunday report that includes both a service checklist and the existing equipment settings table and sermon notes section, duplicated for AM and PM services.


Checklist phases per service: Startup (8 items), Go Live (5 items), During Service (3 items), Shutdown (3 items), Post-Service (2 items). The only difference between the AM and PM checklists is the Audacity filename format (`MM-DD-YYAM` vs `MM-DD-YYPM`).

#### 5. Wrote Excalidraw Diagram Prompt


A detailed prompt was written (delivered as chat text, not saved to a file) for use in a separate AI session to generate an Excalidraw signal flow diagram. The prompt specifies: five layout groups (microphones, wireless, DM3 with internal processing boxes, outputs, computer/distribution), exact component names and models, connection types and arrow styles (solid for wired, dashed for RF), and the Excalidraw JSON output format. This diagram has not been created yet.

---

### Current System — Key Facts for Context


**Active equipment:**
- Mics: Countryman E6D (head-worn), lapel mic (new 2026), congregation mic (wired)
- Wireless: Shure GLXD4 (2.4 GHz, ~2018) + Shure SLXD4 (UHF, 2026, new and undocumented)
- Console: Yamaha DM3 Standard (December 2024) — replaced MX400, Samson compressor, and Focusrite
- Amplifiers: QSC 1200 (main FOH), secondary PA amp (narthex/nursery)
- Cameras: Sony (wide, 2020), Canon (close, 2017)
- Capture: Elgato HD60 PCIe, Black Magic Intensity
- Computer: Intel i9-10900, 16 GB RAM, GTX 1660 Super, named DESKTOP-KVRCAAH (2020)
- Software: Audacity, OBS, DaVinci Resolve, FileZilla, iCUE


**Streaming targets:** SermonAudio.com (primary + FTP audio upload), Facebook Live (Immanuel Fellowship page), YouTube (immanuelfellowshipchurch6015@gmail.com)

**Service times:** AM stream 9:21 AM, PM stream 5:21 PM

**Active tech volunteers:** Jason, Isaac, Josh, Evan, Calvin, Tyce, Daniel


**Key operational notes:**
- Open Audacity before OBS — both compete for the audio driver; Audacity wins if open first
- iCUE must be opened and closed before other software to initialize the keyboard
- DM3 USB send is independent of the main fader — house volume and stream level can be adjusted separately
- Computer is restarted (not shut down) after the evening service — it must stay on during the week for remote access
- Audacity files named `MM-DD-YYAM` or `MM-DD-YYPM`

**Unresolved questions noted during the session:**

- Is the Focusrite still in the signal chain or fully replaced by DM3 USB audio? (pre-DM3 docs referenced it; DM3 has built-in USB audio interface)
- Is the dbx DriveRack still active between the DM3 and the QSC amplifier? (listed in equipment registry as assumed active but not confirmed)
- Exact body pack models for GLXD4 and SLXD4 need confirmation (guessed GLXD1 and SLXD1)
- G1 key on the DM3 — assumed to be a User Defined Key macro for the OBS camera transition; needs confirmation

---
### What Still Needs to Be Done

**High priority:**
- Fill in the Equipment Registry — serial numbers, exact models, firmware versions
- Write `Components/Shure SLXD4.md` — new gear with no documentation anywhere in the vault
- Write `Procedures/Quick Reference Card.md` — one-page cheat sheet for solo volunteers
- Fill in `Configuration/DM3 Channel Config.md` with current saved presets per speaker

**Medium priority:**
- Write `Components/Yamaha DM3.md` — can draw from the existing `IFC DM3 Operations Manual.md` in the old Users Guide
- Write `Software/OBS.md` and `Software/Audacity.md` — partial content exists in old Users Guide
- Write `Software/Streaming Platforms.md` — detailed Facebook/YouTube/SermonAudio workflow
- Write `Components/Microphones.md` — IFC-specific version replacing the generic textbook content
- Write `Procedures/Volunteer Training.md` — onboarding path for new techs

**Lower priority:**

- Write `Components/Cameras.md`, `Components/Computer and Capture Cards.md`
- Write `Software/DaVinci Resolve.md` — stub exists in old Projects folder
- Write `Components/Shure GLXD4.md`
- Create the Excalidraw signal flow diagram (prompt already written)
- Set up `Logs/Change Log.md` and `Logs/Maintenance Log.md` with a consistent entry format
- Decide whether `Procedures/Service Shutdown.md` should remain as a standalone doc or be retired (its content is already in Service Startup.md Phase 5)
- Review and possibly update or retire remaining old docs in `Sound System/IFC Sound System Users Guide/` — most have been superseded but not yet archived