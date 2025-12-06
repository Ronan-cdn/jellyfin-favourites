# jellyfin-favourites
An extremely simple python script to import audio favourites from users in jellyfin and create m3u playlists.

This will create m3u files for each user in jellyfin, containing all the audio files they have marked as a favourite.

This is useful in Android auto, where the jellyfin app doesn't have way to play user's favorites.

Sample usage (as root):

    cd /tmp
    cp /var/lib/jellyfin/data/library.db .
    jellyfinfav2m3u --shuffle --database library.db
    
    Favourites for userid=3
    Wrote 261 to file 00-Favourites-3.m3u
    Favourites for userid=7
    Wrote 60 to file 00-Favourites-7.m3u
    Favourites for userid=1
    Wrote 78 to file 00-Favourites-1.m3u

# Important Notice:
This Script was written before the release of Jellyfin version 9.11.
It is possible this script will not work with versions >= 9.11.

