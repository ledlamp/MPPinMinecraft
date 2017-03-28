# MPP in Minecraft: Resource Pack for MidiPlayer
This is a resource pack for use with the [Bukkit MidiPlayer plugin](https://www.spigotmc.org/resources/midiplayer.2587/) that contains sounds from [MultiplayerPiano.com](http://www.multiplayerpiano.com/). It is based on the [General MIDI resource pack](https://github.com/SBPrime/GMResourcePack) and contains only instrument 0, so it is compatible with the General MIDI map file (but only instrument 0 will work).

## pianomap.txt Instrument Mapping
Included in this repository is an instrument map file for the MidiPlayer plugin. It is similar to the GeneralMIDI map file (gm.map) but all instruments are directed to instrument 0 (including default). This should be used with the resource pack because it only has one instrument. It is also compatible with the original GeneralMIDI resource pack but only instrument 0 will be used.

## Installation and usage

1. Download the [resource pack](https://github.com/ledlamp/MPPinMinecraft/releases/download/v3/MPP_in_Minecraft_v3.zip) and [piano map file](https://github.com/ledlamp/MPPinMinecraft/releases/download/v3/pianomap.txt)
2. Put pianomap.txt in the MidiPlayer folder of your server and set pianomap.txt as the instrument map in the config (leave drum map blank)
3. For use as a server resource pack, use the following URL in server.properties:
`http://files.catbox.moe/g2gd50.zip`

## Issues

1. This resource pack sounds exactly like Multiplayer Piano, except for distortion caused by changing of pitch. Because of the way the MidiPlayer plugin works, only five sound files are used; one for each octave, and the notes are made by adjusting the pitch using the pitch-adjustment ability of the Minecraft sound API. Ideally, each MIDI key should have its own sound file like MPP does. This can be done if SBPrime modifies the code, but until then (if it ever happens) this issue will always exist :(
2. The last (88th) key is missing because it's an odd one that's the only key that uses the 5th octave (g9), and that octave needs to be super high so that it sounds correctly when played at its lowest pitch. This can be fixed by increasing the pitch of the highest MPP key so that it sounds right when played at the lowest pitch in Minecraft, but meh
3. After these two other issues are fixed, the only difference between this and MPP is that sustain-off (pedal released) cannot be simulated and music will always sound with sustain on (pedal pressed), because played sounds in Minecraft cannot be stopped. There is no way around this.

## Demo
A demo video is at https://youtu.be/7GDqOZKv0Nc

This resource pack and piano map file are used on my Minecraft server, the [Terrium Minecraft Server](http://terrium.net/index.php?threads/terrium-minecraft-server.29/).
