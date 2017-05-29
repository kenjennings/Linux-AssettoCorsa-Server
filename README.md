# Linux-AssettoCorsa-Server
Lame tools for managing the server.

ac - stupid script for launching the server, so I don't have to remember nohup blah de blah.

acpick - WORK IN PROGRESS

5/26 --The script examines the content directories on the server and enumerates all the tracks and cars available.   Eventually this will allow the user to choose a track and car and quickly rewrite the server config file....

5/29 -- Some improvements.  The scope for the arrays for track names and card names is fixed.

The script allows choice of track name (and car) and will rebuild the server_cfg.ini file using that chosen track.

Note that it only goes through the motion of choosing a car.  It turns out the car selection is more complicated and will require more thought.  The car names put into server_cfg.ini must match entries in the entry_list.ini file which describes individual cars.  So, this will need modification to build both files.

Also TO-DO -- On further testing it appears track names with a blank CONFIG_TRACK value are only valid if there is no other entry for that same track with a non-blank CONFIG_TRACK setting.  Therefore, the script needs to be modified to eliminate the blank CONFIG_TRACK entries when a subsequent non-blank CONFIG track is added.

acpick.txt -  example output from an earlier version of the script enumerating the tracks and track variations, and the availabe cars.
