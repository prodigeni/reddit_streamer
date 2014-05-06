## README for reddit_streamer


###Overview

![image of main interface]()

    # NAME:         reddit_streamer
    # VERSION:      0.1
    # AUTHOR:       (c) 2014 Glutanimate
    # DESCRIPTION:  Collects given number of highest ranking youtube links on a subreddit and passes them
    #               to a player of your choice (VLC by default)
    # DEPENDENCIES: lynx, yad, (vlc)
    #               You can grab the zenity fork yad from http://sourceforge.net/projects/yad-dialog/ or
    #               ppa:webupd8team/y-ppa-manager
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

###Installation

1. Grab the latest source tarball and extract it.

2. Copy `reddit_streamer` to your `$PATH` (e.g. `~/bin` for single user installation or `/usr/local/bin` for multi user installation)

3. Copy `reddit_streamer.desktop` to `~/.local/share/applications` for single user installation or `/usr/local/share/applications` for multi user installation)

Note: Some icon themes don't ship with the `minitube` icon by default. I have included the minitube icon found in the [Faenza iconset](http://tiheum.deviantart.com/art/Faenza-Icons-173323228) by tiheum in this repository (License: GNU GPL). If you see a placeholder icon instead of the proper one you can copy the Faenza icon to `~/.icons/hicolor/scalable/apps` and it should be recognized correctly.