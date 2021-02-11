```
 Milestone 1 - Requirements
 Amina Mahmood; Aaron Wade Parker; Dishant Mishra; Edward Riley; Vincent Cheng
 February 11, 2021
```

## Glossary

* __Automation__ - Automation is the automatic player that randomly draws songs from a pool of potential songs, based on rules set by the Station’s General Manager.  Automation is used overnight, when no DJ is playing, or when a DJ needs to step away from the station.

* __Cart__ - A cart is a sound file and its associated information, they can contain more than one song, but should not. A single cart stores multiple shotguns or instances of imaging.

* __Channels__ - Channels are the different audio inputs to be broadcast over the air, including microphone, manual CD player, and digital songs from the library.  The volume at which they are played is controlled via sliders on the physical broadcast station.

* __Group__ - Group is a category of song that is used to determine how often songs are played.  Currently, A non-specialty show (WITR’s standard “Pulse of Music” show) must consist of 50-70% “New Bin” group music and 50%-30% “Library” music.  These group designations are stored, tracked, and changed, internally at WITR.

* __Imaging__ - Anything that is played over the air that is not music or a DJ’s voice.  Imaging includes advertisements, promotional material for specialty shows, public service announcements, and some messages that DJs are occasionally required to play.

* __Rivendell__ - An open-source music management and queueing system used by WITR to store, search, and access their music, sound bytes, and other audio content.

* __Shotgun__ - A type of Imaging, a Shotgun is the typical 5 second or less callout on air such as “WITR 89.7!” or “Butterfree, I choose you!”  Used to break up a set and facilitate transitions between songs.

* __Song Logger__ - An application, developed by the WITR staff engineer, that records every song ever played by WITR.  The system automatically logs any songs played from the Digital Library (Rivendell), however songs played in any other way (from a CD or record) must be recorded manually by entering information into the interface.  The Song Logger does not record any imaging or shotguns.


## Current System

The existing Song Logger is used by WITR DJs to maintain a searchable record of what songs were played during their shows. The complete historical log is available for public viewing at [http://logger.witr.rit.edu/](http://logger.witr.rit.edu/). As DJs play songs in the Rivendell Library, the Song Logger is automatically updated, pulling the song’s information from Rivendell. Songs played from a CD or record, however, must be entered manually by the DJ, making them susceptible to human error. Errors such as misspellings and capitalization differences can make it difficult to accurately determine historical play information for a given song or artist.

Additionally, the information available on the public logger page is limited to each song’s title, the name of the artist, and the date and time at which the song was played. Listeners wishing to learn more about a given song or artist must search for them on a separate service such as [Google]( https://www.google.com/) or [AllMusic](http://www.allmusic.com/).

The Song Logger also does not keep track of imagings that are played, which results in entire shows having to be reviewed by the Programming Director or Assistant Programming Director to ensure that the correct content was played.

There is currently no way to view or automatically compile summary statistics about previous broadcasts. Specifically, the Programming Director has no straightforward way to check that the DJs are following the guidelines set forth by the WITR Eboard regarding the types of content and imaging that is used in each show.

The Song Logger is also apparently somewhat unstable, and has been known to crash and require troubleshooting from the WITR staff engineer.

Since the current system is relatively simple, there is no concept of authentication or “roles”: any WITR studio computer can be used to add songs to the log. This also means that it is not possible to add or edit information from outside the studio.


## Goals

We plan on designing and building a more capable replacement for the Song Logger that addresses the problems identified by the stakeholders we interviewed (the General Manager and Programming Director of WITR). Our solution will provide the following additional functionality and changes:

* Manual entry of songs played from outside of Rivendell (CDs, records, tapes, and otherwise) can be performed by searching for the song by name or artist and selecting the correct song from a list of results. This search will be powered by one or more music database APIs (see __Data Sources__ below). This will prevent misspellings and incorrect capitalization during entry, and will make analyzing the logs much easier.

* As each song is added to the log (either manually or automatically), one or more music database APIs will be queried to acquire metadata for the song. This metadata can then be viewed by WITR listeners and staff in the log itself, allowing them to easily find more information about each artist and song played without having to search a different service.

* In addition to songs, the tracker will also keep track of which imagings are played. WITR listeners will still only be shown songs, but WITR staff will be able to quickly review which imagings were played during different shows and make sure requirements were met.

* In case a log entry was entered incorrectly or accidentally, WITR DJs will be able to edit existing records: either changing the song information or removing the record entirely.

* In case a manual log entry was missed, WITR DJs will be able to retroactively add songs to the log.

* WITR DJs will continue to access the application without a login from studio computers.

* WITR E-Board and administrators will be able to login to the application remotely to view statistics and detailed information about song and imaging broadcasts so that they do not need to be in the studio to check for compliance with guidelines and review DJ performance.


## Stakeholders

* WITR listeners
    * They want to know what songs have been playing on air recently, and further in the past
    * They want to find out more information about songs and artists they hear on the air
        
* WITR DJs
    * They want to use the logger to automatically create a comprehensive record of what was played during their show, both for their review and for review by members of the Eboard.
    * They want to be able to enter manually-played songs into the log quickly and without errors.


* WITR E-Board & Administrators
    * E-Board & Administrative members want to use the Song Logger to verify that DJ’s shows are in compliance with the rules & regulations set forth regarding what content can be played and what imaging needs to be played.  They also would like to use the Logger as a means of tracking trends in song playing and popularity over time.  As some E-Board members also work as DJs, some may have similar interest as regular DJs.


## Scope

The scope of the project involves the logging of songs, shotguns, and imagings. Viewing of logs and generating visualizations and reports from the logs is also within the scope of the project. For the purposes of the project we will not be working with the queueing, requesting, or playing of songs: these things are outside of our scope and are handled well by WITR currently.


## Input

The following inputs will be used:

* Partial user input will be received as users enter search queries or new log entries.

* An audio file’s information from Rivendell or manually entered information in the case of physical media.

* Song metadata from one or more online music database APIs.

* Song name, artist, and air date information entered by the user when searching the log.

* Date and song metadata information entered by the user for viewing statistics and generating reports.


## Processing

* Searches will be run on partial user input (while entering or searching for a song, artist, or imaging) to provide autocompletion suggestions.

* Song and artist metadata provided by users and online music database APIs will be cleaned and checked against existing entries to ensure consistency.

* Searches will be run based on artist, song name, and date parameters.

* Historical broadcast data will be aggregated and processed to create summary statistics and visualizations.


## Output

* For listeners: A searchable collection of music played WITR, complete with song and artist metadata. Autocompletion suggestions will be displayed for search inputs.

* For DJs, WITR E-Board, and Administrators: A searchable collection of music (including metadata), imagings, and shotguns played on air, as well as visualizations and summary statistics of broadcast logs. Autocompletion suggestions will be displayed for search and log entry inputs.


## Data Sources

* __[The Echo Nest](http://developer.echonest.com/)__ - An API offering a wide array of music data and services for application development.

* __[Decibel](https://developer.decibel.net/our-api)__ - An API tracking over 100 fields of information for many songs.

* __[Discogs](http://www.discogs.com/developers/)__ - An API offering JSON access to many songs.

* __[All Music](http://www.allmusic.com/advanced-search)__ - A search repository and database that offers advanced querying and information on millions of songs.

* __[WITR Song Logger](http://logger.witr.rit.edu)__ - An application coded by a former WITR Staff Engineer that automatically tracks any song played from WITR’s online library.  It also allows for manually logging songs, which is used to record when a song is played from a location other than WITR’s online library.  The public-facing side of the logger tracks artist name, song name, and time played.  The WITR-exclusive side tracks these three things and the group that the song falls into.  The logger has currently tracked over 426,000 songs played by WITR dating back to March 2012.
