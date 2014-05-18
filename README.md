## README for reddit_streamer


###Overview

![image of main interface](https://raw.githubusercontent.com/Glutanimate/reddit_streamer/master/screenshot_reddit_streamer.png)

    # NAME:         reddit_streamer
    # VERSION:      0.4
    # AUTHOR:       (c) 2014 Glutanimate
    # DESCRIPTION:  Collects defined number of top video links off a subreddit and passes them to a
    #               player of your choice (VLC by default)
    #
    # FEATURES:     - supports YouTube, Vimeo, Liveleak and Dailymotion
    #
    # DEPENDENCIES: curl, yad, (vlc)
    #               You can grab the zenity fork yad from http://sourceforge.net/projects/yad-dialog/ or
    #               ppa:webupd8team/y-ppa-manager
    #
    # CHANGES:      - 0.4 -- replaced lynx with curl command-line
    #               - 0.3 -- added support for vimeo.com, liveleak.com and dailymotion.com
    #                     -- adjusted video link limit (100 is the maximum supported by reddit)
    #                     -- youtu.be links aren't unshortened anymore (they are supported by recent
    #                        revisions of the VLC youtube parser)
    #               - 0.2 -- fixed bug where youtube playlists would be played fully
    #               - 0.1 -- initial release
    #
    # LICENSE:      GNU GPLv3 (http://www.gnu.de/documents/gpl-3.0.en.html)
    #
    # NOTICE:       THERE IS NO WARRANTY FOR THE PROGRAM, TO THE EXTENT PERMITTED BY APPLICABLE LAW. 
    #               EXCEPT WHEN OTHERWISE STATED IN WRITING THE COPYRIGHT HOLDERS AND/OR OTHER PARTIES 
    #               PROVIDE THE PROGRAM “AS IS” WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED OR 
    #               IMPLIED, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY 
    #               AND FITNESS FOR A PARTICULAR PURPOSE. THE ENTIRE RISK AS TO THE QUALITY AND 
    #               PERFORMANCE OF THE PROGRAM IS WITH YOU. SHOULD THE PROGRAM PROVE DEFECTIVE,
    #               YOU ASSUME THE COST OF ALL NECESSARY SERVICING, REPAIR OR CORRECTION.
    #
    #               IN NO EVENT UNLESS REQUIRED BY APPLICABLE LAW OR AGREED TO IN WRITING WILL ANY 
    #               COPYRIGHT HOLDER, OR ANY OTHER PARTY WHO MODIFIES AND/OR CONVEYS THE PROGRAM AS 
    #               PERMITTED ABOVE, BE LIABLE TO YOU FOR DAMAGES, INCLUDING ANY GENERAL, SPECIAL, 
    #               INCIDENTAL OR CONSEQUENTIAL DAMAGES ARISING OUT OF THE USE OR INABILITY TO USE 
    #               THE PROGRAM (INCLUDING BUT NOT LIMITED TO LOSS OF DATA OR DATA BEING RENDERED 
    #               INACCURATE OR LOSSES SUSTAINED BY YOU OR THIRD PARTIES OR A FAILURE OF THE 
    #               PROGRAM TO OPERATE WITH ANY OTHER PROGRAMS), EVEN IF SUCH HOLDER OR OTHER 
    #               PARTY HAS BEEN ADVISED OF THE POSSIBILITY OF SUCH DAMAGES.

###Changelog

- 0.4
    - replaced lynx with a curl command-line
- 0.3 
    - added **support for vimeo.com, liveleak.com and dailymotion.com**
    - adjusted video link limit (100 is the maximum supported by reddit)
    - youtu.be links aren't unshortened anymore (they are supported by recent revisions of the VLC youtube parser)
- 0.2 
    - fixed bug where youtube playlists would be played fully
- 0.1 
    - initial release

###Dependencies

VLC and curl should be available in your standard repositories. You can install them with

    sudo apt-get install vlc curl
   
[YAD](http://sourceforge.net/projects/yad-dialog/) is an advanced fork of Zenity. Unfortunately it hasn't arrived in the Debian/Ubuntu repos yet but luckily enough the folks over at www.webupd8.com created a PPA for it. You can add the YAD PPA and install YAD with:

    sudo add-apt-repository ppa:webupd8team/y-ppa-manager
    sudo apt-get update
    sudo apt-get install yad

###Installation

1. Grab the latest source tarball and extract it.

2. Copy `reddit_streamer` to your `$PATH` (e.g. `~/bin` for single user installation or `/usr/local/bin` for multi user installation)

3. Copy `reddit_streamer.desktop` to `~/.local/share/applications` for single user installation or `/usr/local/share/applications` for multi user installation)

Reddit Streamer should now appear in your launcher (e.g. Unity dash).

Note: Some icon themes don't ship with the `minitube` icon by default. I have included the minitube icon found in the [Faenza iconset](http://tiheum.deviantart.com/art/Faenza-Icons-173323228) by tiheum in this repository (License: GNU GPL). If you see a placeholder icon instead of the proper one you can copy the Faenza icon to `~/.icons/hicolor/scalable/apps` and it should be recognized correctly.

###Common issues

**The script has suddenly stopped working**

This script uses VLC to stream videos. If it suddenly stops working, chances are that a video hosting service updated their website and broke VLC's parser scripts. If that's the case you can replace the scripts with more recent revisions by:

1. downloading the [latest VLC sources](https://www.videolan.org/vlc/download-sources.html) 
2. extracting the contents of `./share/lua/playlist` to `~/.local/share/vlc/lua/playlist`.


**The videos are constantly buffering**

VLC will choose the highest resolution by default. You can change this in the settings menu: Go to *Tools* → *Preferences* and make sure *Show settings* is set to *All*. Then click on *Input/Codecs* in the left treeview pane. Find the combobox entry that says *Preferred video resolution*, adjust it to your needs and click *Save*.

**Some videos are played in low resolution even though HD is available**

In some cases VLC will only be able to extract SD streams. This mainly occurs with Vimeo.
