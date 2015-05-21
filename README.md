# Wireless Info

This script gathers the infos necessary for troubleshooting a wireless connection
and saves them in a text file, wrapping it in an archive if it exceeds the 19.5 kB
size limit for `.txt` attachments on the Ubuntu Forums.

## Details

- Creates the file `wireless-info.txt` at the location it is run from.
- Additionally creates the archive `wireless-info.tar.gz` if the file exceeds 19.5 kB in size.
- Masks all sensitive info, like MAC addresses and WPA/WEP keys, automatically in a meaningful way.
- Offers to post the results to your default `pastebinit` provider if the program is installed,
  and a sufficiently reliable internet connection is available.

## Run from CLI

You can either run it from the command line with these commands:

    wget -N -t 5 -T 10 https://github.com/UbuntuForums/wireless-info/raw/master/wireless-info && \
    chmod +x wireless-info && \
    ./wireless-info

This will download the script, make it executable, and run it, all in a row.

## Run from GUI

Or, if `zenity` or `kdialog` is installed, run it from the GUI this way:

1. [Download][1] the script
2. Make it executable
3. Run it from your file browser or a Run dialog

[1]: https://github.com/UbuntuForums/wireless-info/raw/master/wireless-info

## Disconnected

If you cannot connect to the internet with the affected system, including via a wired connection,
you will have to move files between it and a system connected to the internet.
