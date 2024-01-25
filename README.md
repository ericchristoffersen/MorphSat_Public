MorphSat - Morphism through constraint Satisfation

Eric Christoffersen - 2024.

This is a command line tool for arbitrary manipulation of workout files.
This project is currently private and not open source.

This project makes use of or has source code derived from the following sources:
- david eberly's geometric tools: https://github.com/davideberly/GeometricTools
- google or-tools               : https://github.com/google/or-tools
- vince's csv parser            : https://github.com/vincentlaucsb/csv-parser
- garmin fit sdk                : https://developer.garmin.com/fit/overview
- rapidxml project              : https://sourceforge.net/projects/rapidxml
- rapidjson project             : https://github.com/Tencent/rapidjson


Goals:
1) Read and write most workout file types:

     Currently supports:

       CSV  - READ WRITE

       JSON - READ WRITE - in the style of golden cheetah

       GPX  - READ WRITE

       FIT  - READ WRITE

       RLV  - READ WRITE

       PGMF - READ

       TTS  - READ

   Example: to write out a tts as csv do:

     morphsat.exe -i t.tts -o t.csv

2) Allow files to be blended into a single representation, then exported:

   For example to read a complete tts and output it as separate gpx and rlv file you can do:

     morphsat.exe -i t.tts -o t.gpx -o t.rlv

   Similarly you can import multiple files and output them as one:

     morphsat.exe -i t.gpx -i t.rlv -o t.fit

3) Rescale distance and time within regions of loaded file, this can be used to synchronize workout tracks with video.

   - move and scale a segment in the track from one distance or time to another (stretching all other points so file total doesn't change)

4) Gps track smoothing.

5) Calculate and print workout statistics.

6) Compare workout files.

