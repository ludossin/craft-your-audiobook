# Craft your audiobook
Semi-automated process to create an audiobook (in m4b format) from markdown files. For further info and a bit of context, check: http://www.publishinglab.nl/blog/2016/07/11/craft-your-own-audiobook/ ‎

For this process, you'll need:
-one or more text files in <a href="https://daringfireball.net/projects/markdown/syntax">markdown</a> format (each chapter should have its own file, they should all be located inside directory 'md')
-a cover image (jpg or png)
-a YAML file containing chapter names (simply edit toc.yaml)
-<a href="https://www.python.org/downloads/">python</a>
-<a href="http://pandoc.org/installing.html">pandoc</a>
-<a href="http://www.speech.cs.cmu.edu/flite/doc/flite_4.html">flite</a>
-sox (available as package or you can compile)
-<a href="https://ffmpeg.org/download.html">ffmpeg</a>
-ffprobe (installed with ffmpeg)
-<a href="https://gpac.wp.mines-telecom.fr/downloads/">MP4Box</a>
-<a href="https://code.google.com/archive/p/mp4v2/">m4chaps</a>

After installing all required software and downloading these files, make sure you have your content in markdown format (inside directory 'md') and run, <strong>in this order</strong>:

-create-chapters.py
-get-durations.py
-pack-chapters.py

To run these files, open your Terminal, navigate to the directory where the scripts are located and type

python create-chapters.py

Wait until the script is completely processed and then type the next one. It might take a while. Text-to-speech operations (which occur in the first script) and audio manipulation/concatenation (which occur in the third script) can take <strong>a few minutes</strong> to be completed.
