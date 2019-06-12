# CalcyToast
CalcyIV PvP IV Percentage Toasts using Tasker

So I suspect CalcyIV will at some point introduce some richer PvP information, hopefully IV percentages and IV ranks. In the meantime I figured out a way to have tasker pop up a 'toast' with the scanned pokemons IV percentage.

Disclaimers: I am not good at programming, this is a hack, there will be lots of bugs etc....

What I do is have tasker check for a change in clipboard value and read it. Tasker gets the atk,def,sta IVs and pokemon type and calculates the IV% and pops it up.

Picture: http://imgur.com/a/V1KYpgl

If you want to try this yourself there are a few steps to do.

1. Set up calcy renaming so that AttIV,DefIV,StaIV are all part of the renaming scheme in that order without spaces using the little circles. Also at the end of your renaming you need to have a '#' followed by the 'No#'. e.g. my 12/14/15 Azumarill would rename to '91⑫⑭⑮37½BuIB#184' with my particular renaming scheme. Other schemes should be fine as long as you obey those rules and also don't use the little circle numbers for '#' anywhere else. https://i.imgur.com/kj8k2zV.jpg

2. Download: pvp.js to your phone.

3. Create a tasker 'task' to run 'javascript' point that to the 'pvp.js' file you made. https://i.imgur.com/4U9G1cJ.jpg

4. Create a tasker 'profile' choose 'Variable Set' and under 'Variable' enter '%CLIP'. https://i.imgur.com/CTiGlaX.jpg

5. Start scanning pokemon.

So if calcy doesn't have a good read on the pokemon this will still pop up a toast based on the black circle numbers but it will potentially be wildly inaccurate. It should notify you of the percent for all relevant forms and evolutions including pre-evolutions.

Change 'flashLong' to 'flash' for shorter duration messages.

This work is all built around CalcyIV but I have no connection to them. They do a wonderful job, please checkout reddit.com/r/calcyiv and consider donating for the work they do. All values I ripped from KiengIV's pvp IV spreadsheet so big thanks to him as well.
