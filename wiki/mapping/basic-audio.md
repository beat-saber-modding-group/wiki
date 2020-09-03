---
sidebar: auto
prev: false
next: ./advanced-audio.md
description: How to get your audio file set up and ready for mapping.
---
# Basic Audio Setup
_Get your audio file set up and ready for mapping_

* [Glossary of Terms](/mapping/glossary.md)

This page provides both new and experienced mappers with general recommendations for setting up a new song file before starting to map. Review the quick start guide below for steps that are **critical** before you begin mapping vs. those that can be done at any time, if they're needed.

## Audio Setup Quick Start
::: warning
* Steps 1-5 **MUST** be completed before you start mapping or your audio will be out of sync and may have a [*hot start*](./glossary.html#h).

* Using Online Websites to convert audio to `.ogg` may result in your audio file being treated as invalid and will not be loaded by the game! Processing and exporting from [Audacity](https://www.audacityteam.org/) is the easiest way to ensure your audio file works as expected.
:::
1. Download and Install [Audacity](https://www.audacityteam.org/)
	* Optionally install the [ffmpeg for windows](https://manual.audacityteam.org/man/installing_ffmpeg_for_windows.html) addon to open additional file types such as `.aac` or `.m4a` from iTunes.
2. [Find the BPM](./basic-audio.html#finding-the-bpm) and offset of your song
3. [Add a click track](./basic-audio.html#add-a-click-track) to verify your BPM and [sync your song](./basic-audio.html#sync-the-song-to-the-beat)
4. Figure out if you have [enough intro/silence](./basic-audio.html#plan-your-first-note) at the start of your song and [add silence](./basic-audio.html#add-silence)
5. Remove your click track then [Export your song](./basic-audio.html#exporting) as an `.ogg` format file

**Any time before upload:**  
6. [Check your song volume](./basic-audio.html#check-song-volume) and make it [louder](./basic-audio.html#making-your-song-louder) or [softer](./basic-audio.html#making-your-song-softer) as needed

## Song Selection for New Mappers
Below are recommendations, **not** requirements, and will help to ease you into mapping. If you want to map 17 minutes of "In A Gadda Da Vida" for your first map then have at it but know that you’ll face a **lot** of additional challenges.

* Choose a song that has a clear beat to map to. Some genres work better than others.
* Choose a song with a consistent tempo (for example songs with electronic drums). Songs that have tempo/BPM changes over time can be very complicated to map.
* Choose a song on the shorter side (less than 3 minutes is better). Mapping a 10-minute epic to start with may lead to frustration and/or burn out.
* Finally, choose a song that you don’t mind listening to over and over and over and over again. But avoid mapping your favorite song as your first few maps, save that for when you’re more experienced.

## Audio Quality
Before you begin mapping, ensure you have a high quality source file for your song. Many maps have terrible audio files, often from YouTube rips or low bitrate files. This is a game for music after all, so having good audio is essential for a good player experience.

Follow these general guidelines as you work on your maps:
* Use the highest quality source you can find such as **FLAC or WAV(E)** files (lossless format).
* A close second are high bitrate (+200kbps) **MP3 or AAC** files (lossy formats). 
* Use a YouTube rip **only** as a last resort. The bitrate is low and the volume is seldom right. In this case some audio editing might be required (see [Editing with Audacity](/mapping/basic-audio.html#editing-with-audacity)).

> Sites where you can buy the tracks/album, such as an artist’s [Bandcamp](https://bandcamp.com/), usually will have the highest quality source available. If the artist does not have a Bandcamp available, Google Play Music, Amazon Music and iTunes are alternatives for high quality MP3 files.

By purchasing and using a high quality audio file, not only are you supporting your artist, but you save yourself a lot of headache while mapping. Look at the difference in quality for the same song, at the same beat. 

| OGG Quality | YouTube Rip | MP3| WAV | FLAC |
| :----: | :----: | :----: | :----: | :---: |
| 1 | ![YouTube Rip 1](./images/ytrip1.jpg) | ![MP3 1](./images/mp31.jpg) | ![WAV 1](./images/wav1.jpg) | ![Flac 1](./images/flac1.jpg) |
| 5 | ![YouTube Rip 5](./images/ytrip5.jpg) | ![MP3 5](./images/mp35.jpg) | ![WAV 5](./images/wav5.jpg) | ![Flac 5](./images/flac5.jpg) |
| 10 | ![YouTube Rip 10](./images/ytrip10.jpg) | ![MP3 10](./images/mp310.jpg) | ![WAV 10](./images/wav10.jpg) | ![Flac 10](./images/flac10.jpg) |

Can you see the difference? You cannot scale up audio quality; only starting with a high quality audio file can give you clean, percise lines. 

See the [Advanced Audio Editing](/mapping/advanced-audio.md) page for more in-depth techniques and tools for analysing the audio quality of files.

## Finding the BPM
There are three ways to find the BPM for the song which you want to map. Try them in order (easiest to hardest) if you don't get any results:

### Tool-Assisted BPM Calculation
::: tip NOTE   
This is the recommended method for songs with a constant BPM
:::

[Arrow Vortex](https://arrowvortex.ddrnl.com/) is a free tool to analyze a song’s BPM automatically. It will also find the offset needed to line the audio up to the beat in Audacity or your map editor. 

**Using Arrow Vortex to find BPM and offset:**  
The steps listed below are the same as those used in Ryger’s [Arrow Vortex BPM Analysis Video Tutorial](https://youtu.be/Z49UKFefu5c) (which also includes BPM confirmation). 
1. Download Arrow Vortex (AV), extract the file, and open `ArrowVortex.exe`
	- Discord [Zip Download](https://cdn.discordapp.com/attachments/443569023951568906/662417326771273728/ArrowVortex.zip) (Recommended Method)
	- Arrow Vortex Website [Rar Download](https://arrowvortex.ddrnl.com/)
		- You will need additional software such as [7zip](https://www.7-zip.org/) to extract `.rar` files such as this one.
2. Export your song to `.ogg` using [Audacity](https://www.audacityteam.org/)
	* Using other formats (ie. `.mp3` or `.m4a`) adds a delay to the audio that varies every time and is not accounted for when you export your changes for use in editor.

:::danger
**This is a critical step!**  
Not using a `.ogg` file or using the export feature in AV **will** desync your song by an inconsistent amount of time.
:::

3. Drag the song file into the AV window
4. Go to the `View` menu and click `Time based (C-mod)` to see the waveform
	* Use <kbd>CTRL</kbd> + mouse scroll to zoom
5. Go to the `Tempo` menu and click `Adjust sync...` or just press <kbd>SHIFT</kbd>+<kbd>S</kbd> to open the adjustment window.
6. Click the <kbd>Find BPM</kbd> button
	- If you're lucky, AV will return a single BPM value with 100% confidence.  
	![AV adjustment window](./images/adjustments.png)
	- If you get multiple options you will want to listen to the options to see if they match with the song. Most of the time it will be the first option but follow steps 7 and 8 to make sure.  
	![Multiple BPM Values](./images/alternateAdjustments.png)
7. Click the <kbd>Apply BPM</kbd> button
8. Press <kbd>F3</kbd> to turn on beat ticks and press <kbd>Spacebar</kbd> to listen through the song to confirm that the beginning, middle, and end of your track are all lined up.
	- If only a single result was given and the ticks do not match, this suggests that the song has a variable BPM. 
	- If the detection gave multiple options and the ticks do not match, select the next option, click the <kbd>Apply BPM</kbd> button and listen again. If none of the options work for the song, this suggests that it has a variable BPM.

:::warning NOTE on Variable BPM
It is recommended that newer mappers choose a different song due to the increased difficulty associated in mapping variable BPM.
Not sure if your song is variable? Drop by BSMG's `#mapping-discussion` and ask!  

If you have the experience, see [Advanced Audio Editing: Variable BPM](/mapping/advanced-audio.md#variable-bpm) on how to account for this.
:::

10. Give the player about two seconds to get ready by clicking the `Move first beat` button ![Arrow Vortex move beat button](./images/av_movebeat.png) however many times needed to get your start time close to 2.000 seconds or the sound you want to place your first note on aligned with the first bar.  
![Aligned with first bar](./images/av_aligned.png) ![Alternate Aligned with first bar](./images/av_altAligned2.png)
	* After aligning, you should check the song again to verify that the beats still match.
	* If your song has too much intro silence, you will end up with a negative `Music offset`. What this means is that you will need to remove silence from intro of the audio file in Audacity. If you are not comfortable with removing the exact amount, you can remove more than needed, export the change `.ogg` and re-sync with the new file to get a positive offset.
11. After finding the BPM and offset values you can skip to [Add Silence: After Tool Assisted Sync](/mapping/basic-audio.html#after-tool-assisted-sync).

### Online Search
You can search online using a search engine site (e.g. [Google](http://google.com)) in your web browser for `[song name] + [artist] + "bpm"` and often find a number of sites (e.g. [SongBPM.com](https://songbpm.com/)) with this information.

### Manual BPM Calculation
If both methods above fail you will have to manually find the BPM, but this is easier than you might think.
1. Use an online BPM tapping calculator (like the [Tap for BPM Tool](https://www.all8.com/tools/bpm.htm), open the page in your web browser).
2. Play the song in your favorite music player.
3. With the webpage in focus, tap any key to the beat (every quarter note) for about 30 seconds and the tool will display the BPM of the song.
4. Take note of the nearest whole value.

## Audio Preparation
To make it easier to map and make sure that the song is synced perfectly to the game's beat you need to set up your audio file correctly. This section will assume you are using [Audacity](https://www.audacityteam.org/).
If you have used [Tool Assisted BPM](/mapping/basic-audio.html#tool-assisted-bpm-calculation) and offset detection (such as Arrow Vortex) you can skip to [Add Silence: After Tool Assisted Sync](/mapping/basic-audio.html#after-tool-assisted-sync).

### Plan Your First Note
Analyse the intro of the song. Depending on where in the song you want to place your first block, you'll need to avoid both a *hot start* (not enough time before the first block) and a too-long intro. Your song will fit into one of three categories:
1. **Songs with no intro:** It is critical to leave at **minimum two seconds** of preparation time for the player before the first playable note(s) in your map, otherwise this is known as a "Hot Start."
2. **Songs with a short intro:** If your song has a short intro that is **less than eight seconds** it is OK for the music to start playing immediately.
3. **Songs with a long intro:** If the song has a very long and uneventful/fade-in intro for **more than ten seconds** it is strongly recommended to shorten the intro so the first note(s) are placed within eight seconds from map start.

In all cases above you will need to time shift the song to an appropriate time based on your needs:
1. **No intro:** Move the song back in time (to the right in the audio track), placing the first mapped note(s) after two seconds. Then sync the song to the beat (See [Sync the Song to the Beat](/mapping/basic-audio.html#sync-the-song-to-the-beat)). Later fill the gap with silence (See [Add Silence](/mapping/basic-audio.html#add-silence)).
2. **Short Intro:** Sync the song to the beat (See [Sync the Song to the Beat](/mapping/basic-audio.html#sync-the-song-to-the-beat)) and then fill the gap with silence (See [Add Silence](/mapping/basic-audio.html#add-silence)) or trim the audio before 0 seconds (See [Trim the Intro](/mapping/basic-audio.html#trim-the-intro)) depending on which case applies.
3. **Long intro:** Move the song forward in time (to the left in the audio track), placing the first note(s) within 8 seconds (See [Sync the Song to the Beat](/mapping/basic-audio.html#sync-the-song-to-the-beat)), then trim the audio before 0 seconds (See [Trim the Intro](/mapping/basic-audio.html#trim-the-intro)).

### Add a Click Track
This is to confirm that the BPM you have found online or manually matches the audio file you have. This addition is temporary; you should remove the click track before [exporting your audio](/mapping/basic-audio.html#exporting).
1. Open the song you want to map into Audacity.
2. Add a new mono track from `Tracks menu > Add New > Mono Track`
3. Place the cursor at the start of the new track (Click on the track and press your Home key) and then click `Generate menu > Rhythm Track…`
4. Input the nearest whole BPM you got earlier into the `Tempo (bpm)` field and enter the duration of the song in the optional `Rhythm track duration` field (the duration is displayed at the top right of the timeline).
5. Copy the other recommended settings below:
![Audacity Rhythm Track Menu](./images/click-track-1.png)

If everything was correctly input you will have something like this:
![Audacity main screen showing song track and rhythm track](./images/song_rhythm.png)

This click track is completely in sync with the beats in the map editor and game, but the song is currently not synced. Continue below for how to do that.

### Sync the Song to the Beat
1. Select the Time Shift Tool (![Time Shift Tool](./images/timeshift.png)).
2. Left click on the song track and hold, then drag the audio so that the first planned mapped note(s) in your song ends up within the appropriate seconds (see timeline above the track) to avoid a "Hot Start" or too long intro (See [Plan Your First Notes](/mapping/basic-audio.html#plan-your-first-note) if you haven’t already).
3. Release to place the audio in the new position.
4. Play back the audio in this position. The song will be out of sync, so find the closest beat in the click track and align your song to the beat (click track) by moving it backward or forwards in time by small increments. Zoom in for better accuracy. Repeat until it sounds spot on.
5. When you think you’ve found the beats of the song to match the Click Track review the whole song to ensure that the BPM you have is the correct one and that the song is in the same fixed BPM throughout the whole song. If not, you might have gotten the wrong BPM, in which case try to tap out the BPM manually (again), see "Manual BPM Calculation". 
::: warning
If the BPM is correct for the first part of the song but suddenly change or drifts off then you most likely have a song with Variable BPM, see [Advanced Audio Editing: Variable BPM](/mapping/advanced-audio.html#variable-bpm) for more info on this subject.
:::

Below shows how it looks like when the first planned mapped note(s) (cursor position) are placed after 2 seconds and the beats of the song is synced to the BPM/Click Track.
![Audacity song lined up with rhythm track](./images/synced_rhythm.png)
After time shifting the song you will need to add silence, continue below on how to do that.

## Editing with Audacity
After syncing the song to the beat manually or by using tool assisted sync (e.g. Vortex Arrow) you will have to add silence to the intro of the song. You may also need to do other edits if they’re necessary. More on that below.

### Add Silence
#### After manual sync:
If the waveform/audio clip has a gap to the timeline start (0,0 seconds) you will need to add silence to the audio, or else Audacity will export from the start of the audio clip and you will lose any sync you've done. Do the following to add silence:
1. Switch to the Selection Tool (![Selection Tool](./images/selection.png)).
2. Select the empty space between the audio clip and the start of the track (Yellow vertical lines will indicate the start and end edges when you make a selection).  
![Adding silence with Audacity](./images/add_silence.png)
3. Click `Generate menu – > Silence…`  
![Generate Silence...](./images/audacity-generate_silence.png)
4. The right amount of silence should already be input automagically so just hit OK.
5. Done.


After generating the silence you can click the dark line in the song track to get rid of the cut.

#### After tool assisted sync:
If you've used Arrow Vortex or other tool assisted syncing then do the following to add or remove the right amount of silence to the song track.

**If you have a positive offset**, you will need to add that amount to the intro.  
1. Open the song in Audacity if you haven't already done so, then switch to the Selection Tool (![Selection Tool](./images/selection.png)).
2. Place the cursor at the start of the song track (Click on the song track and press your <kbd>Home</kbd> key).
3. Click `Generate – > Silence…`  
![Generate Silence...](./images/audacity-generate_silence.png)
4. Input the sync `Music offset` value you got from Arrow Vortex (or similar tool) and then click OK. 
![Adding silence with Audacity](./images/av_audacity.png)
5. Done.  
___
**If you have a negative offset**, you will need to remove that amount from the intro.  
1. Open the song in Audacity if you haven't already done so, then switch to the Selection Tool (![Selection Tool](./images/selection.png)).
2. Add a new mono track   
![Add new mono track](./images/audacity-add_new-mono-track.png)
3. Select the new track and tap the <kbd>Home</kbd> key.
4. Click `Generate – > Silence…`  
![Generate Silence...](./images/audacity-generate_silence.png)
5. Enter the amount of negative offset found in Arrow Vortex (or similar tool) into the Duration field and click OK.
![Adding silence with Audacity](./images/av_audacity-negative.png)  
	* You should see something similar to this  
![Resulting Silence](./images/audacity-neg-generated_silence.png)
6. Select from the end of the generated silence (yellow vertical line) to the start of the song track selecting the contents of both tracks.  
![Select up to generated silence](./images/audacity-neg-select_silence.png)
7. Press the <kbd>Delete</kbd> key.
8. Click the X on the newest track to delete it.  
![Delete The Track](./images/audacity-delete_track.png)
9. Done.

> If you are not comfortable with removing the exact amount, you can remove more than needed, export the change `.ogg` and [re-sync using your tool](#tool-assisted-bpm-calculation) with the new file to get a positive offset.

After generating the silence you can click the dark line in the song track to get rid of the cut.

### Trim the Intro
This step is optional, but can be useful if you need to make a more graceful fade-in for your song, if needed.

If your track has arrows pointing to the left at the start it means you’ve time shifted the audio forward in time outside the timeline. If you’ve done this to shorten the intro, although not necessary, it is beneficial to trim the sound clip and add a fade in. To trim and add a fade in to the song (optional) do the following:
1. Drag a selection from 0.0 seconds to the end of the audio track (yellow vertical lines).
2. Click Trim audio outside selection (![Trim audio to selection](./images/trim.png)). The arrows should now disappear. 
3. (Optional) Make a selection from track start (vertical yellow line) to about 0.5-1 seconds (depending on intro).
4. (Optional) Go to `Effect menu -> Fade In`.
5. Done.

Before (left) and after trim and fade-in applied (right):

![Trimming the song intro](./images/trim_fade.png)

### Check Song Volume
To ensure that your song isn’t too soft, or even too loud for that matter, we can measure it using RMS (Root Mean Squared) in Audacity. To have a good balance between note slice sounds and your song the RMS value should be **louder than -11db** (in the verses and/or choruses) or **softer than -8.5db** (at the loudest parts).

To check the RMS value in your song do the following:
1. Open Contrast Analyzer in `Analyze menu -> Contrast…`
2. With the Contrast Analysis window still open, select a part of the chorus section (about 15-20 seconds) of your song
3. Click any of the `Measure selection` buttons. (We only need to use one.)
4. In the `Volume output` field you will now find a value. Compare this value to the recommended values above.
5. If this value is smaller (more negative) than the recommended values, see [Volume Modification: Making Your Song Louder](/mapping/basic-audio.html#making-your-song-louder).
6. If this value is bigger than (less negative) than the recommended values see [Volume Modification: Making Your Song Softer](/mapping/basic-audio.html#making-your-song-softer).
![Analyzing song volume with Audacity](./images/contrast.png)

### Volume Modification
Before you continue with the next steps with the song editing it highly recommended to save your current progress as a WAVE file as a backup. This is to ensure that you if you need to go back and redo some of the editing you will have a high quality source to use. (Don’t load the OGG you exported as it will have lost a lot of the source quality.) Remove the Click Track if you haven’t already done so, then go to `File menu -> Export -> Export as WAV`, then save the file to a location of your choice.
::: tip NOTE
Doing any kind of audio processing on a song will inevitably change its sound, however, it's an important step to give your players the best map and song experience.
:::

#### Making Your Song Louder
If your song’s chorus has a lower RMS value than the recommended **-11db** then you will need to do Compression and/or Limiting to bring the volume up. (Note: Amplify/Gain is not used for this, as anything above 0db will create an unpleasant distortion.)

To check if you need to apply Compressor before Limiter visually analyse the waveform. If there are a lot of sharp peaks with a pretty constant body throughout the song, as shown in the example below, then you will not need to apply compressor. Only a Limiter will suffice (skip to [Limiter](/mapping/basic-audio.html#limiter)).

![Viewing a song that is too quiet](./images/louder.png)

However, if the waveform varies a lot between soft and loud parts then compression will most likely be needed first.

#### Compression
1. Select the whole song track (Double click on the track)
2. Go to `Effects menu -> Compressor`
3. As a starting point, copy the settings below and click OK. Make sure that `Compress based on Peaks` is checked.
![Understanding compression](./images/compression.png)

Here’s a before (top) and after (bottom) Compressor comparison:
![Before and after compression](./images/bna_compression.png)

Check the song again and listen for any unnatural distortions, such as volume cut outs after loud peaks. If so, undo (`Ctrl-Z`), tweak the `Threshold` setting to a louder one (less negative) and apply again. If you want to know more about the settings check the [Advanced Audio Editing: Compressor](/mapping/advanced-audio.html#compressor) page.


#### Limiter
The compressor reduces many of the unnecessary peaks and makes the more important sounds louder. However, we still haven’t reached the right RMS volume for the song. To achieve this we will remove more of the headroom using the Limiter effect:
1. Select the whole song (Double click the song track)
2. Go to `Effects menu -> Limiter…`
3. As a starting point, copy the settings below:  
![Limiter in Audacity](./images/limiter.png)
4. Click OK to apply Limiter.

Check the song again and listen for any unnatural distortions, such as crushed/severely distorted peaks. If so, undo (`Ctrl-Z`), tweak the `Input Gain` settings to a lower value (still above 0db) and apply again. Make sure both `Input Gain`values are the same or else the stereo image will be skewed. If you want to know more about the settings of the Limiter effect check the [Advanced Audio Editing: Limiter](/mapping/advanced-audio.html#limiter) page.

To know if you’ve reached the right volume after compressing and limiting check again with the RMS volume tool:
1. Open Contrast Analyzer in `Analyze menu -> Contrast…`
2. With the Contrast Analysis window still open, select a part of the chorus section (about 15-20 seconds) of your song.
3. Click any of the Measure selection buttons. (We only need to use one.)
4. In the `Volume output` field you will now find a value. This value should be between -8.5db and -9.5db for optimal level. If not, undo the limiter process and increment the `Input Gain` by +/-0.5db and try again.

After limiting you will have something like this:
![Song after limiting](./images/bna_limiting.png)
You can now skip to [Trimming the Outro](/mapping/basic-audio.html#trimming-the-outro).


#### Making Your Song Softer
Some modern electronic music producers have a tendency to make their songs really loud just to have a track louder than other's. In the rare cases you have this kind of song (**RMS value above -8.5db**) it is **strongly recommended** to lower the volume of the song to make all Beat Saber songs normalized. This helps with hearing the note slice sounds better and to give the players a much more pleasant experience switching between songs.

Before you lower the volume you want to know approximately how much you need to lower the volume with. Do this by checking with the RMS volume tool:
1. Open Contrast Analyzer in `Analyze menu -> Contrast…`
2. With the Contrast Analysis window still open, select a part of the chorus section (about 15-20 seconds) of your song.
3. Click any of the Measure selection buttons. (We only need to use one.)
4. In the Volume output field you will now find a value. Calculate the difference between your value and -8.5db and remember this value.
5. Close the Contrast Analysis window.

Now let’s use the Amplify effect to lower the volume:
1. Select the whole song (Double click the song track)
2. Go to `Effects menu -> Amplify...`
3. Enter the difference value you calculated earlier (it should be negative) into the `Amplification` field. `New Peak Amplification` field will repeat what the first input field says, this is normal for a song that is already peaking at 0db.   
![Amplification menu](./images/amplify.png)
4. Click OK to apply a negative Amplify effect.
5. Done.

To know if you’ve reached the right volume check again with the RMS volume tool:
1. Open Contrast Analyzer in `Analyze menu -> Contrast…`
2. With the Contrast Analysis window still open, select a part of the chorus section (about 15-20 seconds) of your song.
3. Click any of the `Measure selection` buttons. (We only need to use one.)
4. In the `Volume output` field you will now find a value. This value should be between -8.5db and -9.5db for optimal level. If not, undo the Amplify process and increment the Input value by +/- 0.5db and try again.

After the negative value Amplify effect your song will look something like this:
![Amplification effect](./images/bna_amplify.png)


#### Trimming the Outro
In Beat Saber the map will continue for as long as the audio file lasts. E.g. this means that having silence for five seconds after the song has ended the map will still play for five seconds before terminating and bringing the player to the score view. This is why it’s important to mind the time from the last note to when the audio track ends.

Go to the end of your song and play the last part and outro. From the point where you intend to have the last note(s) count to 3 or 4 seconds and pause the playback. Where your playback cursor is now located is where you should generally cut off your song. (Naturally all songs will differ, so do what makes most sense for your song.)

To trim the ending at this point do the following:
1. From the paused playback position drag a selection from here to the end of the track (yellow vertical line) and press the `Delete` key to remove this part.
2. Make a new selection from the end of the song track (yellow vertical line) and backwards about 2 to 3 seconds.
3. Go to `Effects menu -> Studio Fade Out`
4. Done.

The song will now fade out just before it gets to the end of the map and the player will be presented with the scoring results much faster.

## Exporting
We now have our finished audio that you will use and hear in the editor and the game. It is recommended to make another WAVE file backup just in case you need to export to OGG again with a different quality setting. (`File menu -> Export as WAV`).

To generate a compatible sound file to use we need to do the following:
1. Delete the Click Track (if you haven’t already done so).
2. Click the `File menu -> Export -> Export as OGG.`  
![Export As Ogg Location](./images/audacity-export.png)
3. Name your file `song.ogg`.
4. Choose an appropriate OGG quality ([more info here](/mapping/advanced-audio.html#choosing-appropriate-ogg-export-quality)):  
![Export Quality Slider](./images/export-quality.png)
	* High quality source (WAVE / FLAC / MP3 / AAC) use 6-9 (unless there is a file size issue.)
	* Low quality source (YouTube or such): use 3-5
5. Click Save.

The song/audio file is now ready to be used in any map editor. Input the same BPM you got earlier in your map editor of choice and make sure to use 0ms offset for all difficulties (since the song is already synced to the beat).
::: warning NOTE
Audio file should not be larger than ~12 MB due to the BeatSaver 14.3 MB ZIP file limit. The 15 MB listed is not accurate at this time. If this is the case export at a lower quality until the file meets the file size limit. ZIP files over 8 MB cannot be shared directly on Discord (without Nitro or Server Boost Level 2) for playtesting.
:::

## Credits
Content on this page is derived from guides by [Kolezan](/mapping/mapping-credits.html#kolezan) & [Nik](/mapping/mapping-credits.html#nik-n3tman).
