# Spotify-Playlist-Generator

## Desscription

This script makes one playlist of an artist you've never heard of before (probably) each time you run it. The list of new artists is based on your likes. I run this code as a cron job, once a day, for the entire year 2020

## Different Scripts Used
1. list366.py : This creates a list of 366 bands based on the bands I like
2. playlist_a.py : This creates the playlist. Run once to create one playlist. 

## Text Files

1. `artist_list.txt` : List of artists I really,really like. I use this information to find similar artists
2. `blacklist.txt` : The artists I have already listened to (and a few I don't like). I don't want repitition in the final list of 366 artists
3. `all.txt` : List generated after using the artist_list.txt . In my case the list contained around 430 artists after filtering out the ones from `blacklist.txt`
4. `list366.txt` : The final list of 366 artists, picked out at random from `all.txt`
5. `last.txt` : stores the name of the last artist whose playlist was created. So the next playlist will be of the artist right after this one in the `list366.txt`

## How To Use 

1. If your tastes are like mine, just directly run `python3 playlist_a.txt` . 
2. You can delete contents of every txt file, and in `artist_list.txt` add a bunch of artists you like, in the `blacklist.txt` add a bunch of artists you don't want to repeat, and then run `python3 list366.py`. Check that the list of 366 artists is created, and then run `python3 playlist_a.txt` 
3. Running `python3 playlist_a.py` creates 1 playlist each time you run itmpoe

## Client ID, Client Secret and User ID

1. Client ID and Client Secret can be obtained once you sign up on the developers page of Spotify ([here](https://developer.spotify.com/documentation/web-api/))
2. User ID (uid) can be obtained from your regular Spotify profile. It'll be in the "username" field, which will be a number.
3. Password : your Spotify password
