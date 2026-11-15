---
tags: [project]
---
# Main List
- [ ] Upload all sermons
- [ ] Finish login page
- [ ] Make check sheet
- [ ] Headphones on computer corded
- [ ] find average size for calculating the USB storage and mark on USB tag
- [ ] setup RDP and practice control
- [ ] make note template add tasks section to 
- [ ] make burn down for sermon upload
- [ ] Clean up
- [ ] make instructions on video edit
- [ ] Logins for SermonAudio and Facebook, google immanuelfellowshipchurch6015@gmail.com
- [ ] Take pictures of mic placement both lapel and head worn
- [ ] setup QoS for audio computer
- [ ] make instruction for how to turn monitoring on and off on OBS
- [ ] Instruction on how to monitor sound at the computer


### 


## Setup
###  Power on:
- Main power in cabinet
- DM3 Soundboard
- Both cameras
- Computer
### Setup Live Stream and Recording


#### DM3 Mixing Board
- good luck
#### Computer
- Login to computer
- Open iCUE and close it
- Open in this order:
	- Audacity
	- OBS
	- Firefox
		- Open all web pages by right clicking on stream folder and clicking 'Open All Bookmarks'
- Copy and paste sermons into Facebook and Youtube
- In OBS fade pre-roll to program and set close to preview

## Start Live stream and recording
- When piano starts turn on cong. mic (channel 1)
- Start Audacity recording
- Click start streaming in OBS . Stay on pre-roll until Pastor walks up to the pulpit
- Start Facebook on SermonAudio, then click go live on Facebook
- On the SermonAudio webcast page start Youtube. Youtube start stream automatically when it receives the stream

## Monitoring Streaming and recording
- Throughout the service monitor meters and streaming
- Listen to stream directly from computer

### OBS
- On OBS Audio mixer should be around 20-15dB
- Watch frames missed due to rendering lag
- watch Dropped Frames (network)
- Monitor Disk Space
- Monitor color of cameras

### Audacity
- monitor input should around 24-15dB
- 

## Ending service
- stop recording audio and video 
- stop streaming
- edit audio
- edit video
- post audio or video
- shutdown equipment after evening service and restart computer. Computer must stay on during the week.




# Techs
- Calvin
- Isaac
- Kyle
- Josh
- Tyce

## Installation

Follow the steps below to install Tasks.

1. Search for "Tasks" in Obsidian's community plugins browser
2. Enable the plugin in your Obsidian settings (find "Tasks" under "Community plugins").
3. Check the settings. It makes sense to set the global filter early on (if you want one).
4. Replace the "Toggle checkbox status" hotkey with "Tasks: Toggle Done".
    - I recommend you remove the original toggle hotkey and set the "Tasks" toggle to `Ctrl + Enter` (or `Cmd + Enter` on a mac).

## Getting Started

### Write some tasks

Create a few tasks in a Markdown note in your vault. For example:

```text
- [ ] Something non-important, with no date
- [ ] Remember to do that important thing - with a due date 📅 2022-12-17
- [ ] Send Kate a birthday card - with a scheduled date 🔁 every January on the 4th ⏳ 2023-01-04
```

Find out more in [Getting Started](https://publish.obsidian.md/tasks/Getting+Started/Getting+Started), and its sub-sections.

### Create your first Tasks search

And then write a Tasks search block somewhere in your Obsidian vault, to find the tasks that are interesting.

Here is an example that shows a few different features. View it in Reading or Live Preview modes to see the results.

````text
```tasks
# Only tasks that are not done, that is, which begin like this (but without the quotes):
#   '- [ ] ' or
#   '* [ ] ' or
#   '1. [ ] '
# Indented tasks are supported, but only single-line tasks.
not done

# Tasks due today or earlier:
due before tomorrow

# Restrict to at most 100 tasks.
# If you ask Tasks to display many hundreds or thousands of tasks,
# Obsidian's editing performance really slows down.
limit 100

# Group and sort the output:
group by filename
sort by due reverse
sort by description

# Optionally, ask Tasks to explain how it interpreted this query:
explain
```
````

Find out more in [Queries](https://publish.obsidian.md/tasks/Queries/Queries), and its sub-sections.

## Documentation

For user documentation, please check [https://publish.obsidian.md/tasks/](https://publish.obsidian.md/tasks/).

## Development

Clone the repository, run `yarn` to install the dependencies, and run `yarn dev` to compile the plugin and watch file changes.

Then see [the Contributing Guide](https://publish.obsidian.md/tasks-contributing).

## Donations

The plugin is completely free to use, and very willingly developed and supported by Clare Macrae since May 2022.

If you have particularly been helped by the Tasks plugin and wish to support it, please see the following link.

- [https://github.com/sponsors/claremacrae](https://github.com/sponsors/claremacrae)

Donations will go towards my computing costs and licenses for development tools that I use for productivity.

Thank you 🙏.