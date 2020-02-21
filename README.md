# Wrapper for Gource, GitHub and ffmpeg

A Git repository history visualization tool using `gource`.

[`gource`](http://gource.io) creates a 3D visualization of the networks formed by authors and committers over time in Git.
This script provides a configuration for `gource` that should work well for repos that are up to a few years old.

When you just run `gource` by itself on the command line, you get an animated 3D playback of activity in your Git repo.
But it's not immediately obvious how to save it and the icons for authors get too small if you have a lot of authors or a lot of code or both. `gource_since` is a script that fixes all that:

* Your `gource` video is saved to disk as an `.mp4` video file, in the current directory.
* The display of `gource` has been tweaked so it should look better in most cases than it does by default.
* A script is included to pull everyone's avatar from gravatar.com, which makes authors much easier to differentiate and is generally more fun!

It is intended that you fork this script and change the settings to you match your own needs. 
No two Git repos are the same and often in order to get a nice visualization, you need to tweak settings!

## Synopsis

    cd your_git_repo
    
    gource_since "90 days ago"
    
This should launch Gource and then when Gource is done, produce an mp4 file in the working directory.

Temp files created by this script are not cleaned up automatically as you may want to re-use them.
However, the `.ppm` file in particular is very large and thus should always be deleted when you are 
finished with it.
