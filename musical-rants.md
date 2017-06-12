# No Music for the Unconnected

Let me clarify what I mean by unconnected here: those that cannot or do not wish to remain connected to the internet all day long. I am one of those who likes to work locally and keep my stuff locally, not able to trust streaming sources of videos and music, and almost all things completely dependent on my remaining connected constantly. Call me outdated but since I do happen to frequently be out of wireless signal range, or in general away from decent connectivity options, this world view is not baseless.

And, it is frightening how tough it is getting around here in the unconnected world. If you wish to skip the rant and see my solution, scroll down to read about my current workflow.

## Cloud Is Everything

... or everything's cloudy. Surely, it is easier to listen to music on YouTube than to find that song, download it, and then play it in your local music player. Or if you are on a phone, Spotify or some similar alternative. But, what are the downsides to this? Let's see:

- **Not a customisable experience**  
  You cannot make playlists on YouTube, for one. That is different for apps like Spotify, but those playlists are not exportable or compatible with other applications. Basically, they lock you in in their platform and control how you experience music, and that goes completely against how I like my computing experience in general to be. That is the reason I use Android, and on my laptop, Linux. I like to be in control of my devices and workflows, and these applications are a huge pain to someone like me. I need keyboard shortcuts, _smart_ playlists, cross-fading, a good equiliser, etc.

- **You need to be continuously connected**  
  For someone like me who travels a lot, this is not possible. I cannot always have 3G signals wherever I go, especially during travel itself. And even if I did have them, remaining connected consumes a lot of battery. I am able to pull out 3-4 days of decent usage from my phone on flight mode, while it would give up in a day if I switch to Spotify.

Now, I'm not saying having music on the cloud is not good. To the contrary, it is very easy to play almost any track you want at a whim instantly, provided you are online and have a stable connection. If you are one of those who can enjoy it, there is practically no need for you to even have to consider switching back to the old ways. In fact, most people are very adept at adapting to chanigng circumstances and wouldn't mind losing the advantages of having mp3 files on their devices, but sadly, I cannot adapt to dumbed down interfaces much and something as esential as music wants me to break free.

## So Make It Rain

All that I wrote doesn't mean I wanna go back to the old days of yore when your music didn't have proper tags and album arts, or you had to hook up a USB cable everytime to copy the files over. That would be stupidity. In the current scenario, I've this particular task broken into the following parts:

1. Downloading the mp3 files
2. Proper ID3 tags and sorting
3. Syncing the music across devices
4. Throwing music from a device to another

I'll describe my current system as of now, which I am planning to automate a little bit. So, here is how I currently do stuff: 

First, let's get the music from our good old source of new and latest music and save it into a temporary directory. I'm not sure about the legal implication of this, but here goes:

```bash
$ youtube-dl --extract-audio --audio-format mp3 {youtube-video-url}`
```

Then, usually [MusicBrainz Picard](https://picard.musicbrainz.org/) easily finds and autofills the tags, but if not, I can manually edit the tags because its usually one or two songs at a time. After this, I place the songs in the main directory.

This is where my syncing setup works. When my phone connects to the WiFi, it turns on an FTP server, which is then mounted by my laptop and the new files are copied over, using cron. The laptop version of files is considered the master and if there are any conflicts, the phone's version would get over written.

Here, I used to use Bittorrent Sync but that beautiful piece of software went into a weird commercial direction and also grew slightly too complex for simple tasks.

That's it so far and I would update this post when I finally automate all of these tasks to the extent that I just press a button on my browser while listening to a song on YouTube so that it downloads it, adds proper ID3 tags, and if fails, prompts me to, and then places the files in proper directory to be synced with my phone, and potentially other devices.

## Throwing The Music

But that's not enough. Let's go one step ahead and think what could be the most you could do with your music. Play it on any device from anywhere, right? Here's my dream world: I play a song on my phne and set my home theatre system as my output device. Well, I've tried DLNA and it is cumbersome at time. Also, currently Android has no way of act as a source or sink for audio, to the best of my knowledge. This is what I want to change. I want to find a way around this limitation so that we would be able to throw audio streams around from one phone to another, or from a laptop to a phone, et cetera.

I'll try to update this post with stuff I find and progress I make. If you have any suggestions regarding this idea, please contact me. I hope I can pull this off!
