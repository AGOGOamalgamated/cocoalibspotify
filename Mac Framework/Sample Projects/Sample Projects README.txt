CocoaLibSpotify Sample Projects
===============================

Please note: These sample projects require Mac OS X 10.6 and higher and Xcode 4.0 to build.

Please also note: The sample projects need a valid application key to build, placed in "appkey.c" in the same directory as the rest of the code files. Premium users can obtain an application key at http://developer.spotify.com/.

Please ALSO note: If you checked this out from our GitHub repo, you must run git submodule update --init before the sample projects will build.

SimplePlayer
============

SimplePlayer is a very simple project that demonstrates logging in to the Spotify service using CocoaLibSpotify and playing a track.

Since CocoaLibSpotify doesn't handle audio playback itself, a two classes are provided to help out:

SPPlaybackManager: A class that takes care of SPSessionPlaybackDelegate methods to extract audio data and push it through CoreAudio. It uses a third-party Objective-C CoreAudio wrapper to do this.

SPCircularBuffer: A simple circular buffer built around libspotify's behavior. This is used by SPPlaybackManager, but you may find it useful if you'd like to implement playback yourself.

Guess the Intro
===============

Guess the Intro is a less simple project that presents a game to the user - they have ten minutes to correctly guess as many tracks as possible. Each round presents four options and the user has twenty seconds to guess.

The project contains code for navigating playlists, folders and top lists to get the user's tracks, as well as creating and adding tracks to playlists. 