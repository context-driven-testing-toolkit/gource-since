# Wrapper for Gource, GitHub and ffmpeg

Git repository history visualization tool.

## Synopsis

    cd your_git_repo
    
    gource_since "90 days ago"
    
This should launch Gource and then when Gource is done, produce an mp4 file in the working directory.

Temp files created by this script are not cleaned up automatically as you may want to re-use them.
