## Ubuntu Forums Support Script
The "Ubuntu Forums Support Script" queries the users computer so that Ubunutu Forums Community Members can see what they are recommending solutions for:
## Details

- Creates the file `support-info.txt` at the base of the user's home directory.
- Masks all sensitive info, like IP addresses, MAC addresses, Full FQDN and Serial numbers, automatically in a meaningful way.
- The script displays the report results within the 'less' utility to review the results, one screen at a time. To navigate from there, press the space bar, left, right, up, down, page up or page down keys to navigate. If in a graphical terminal session, you can also use mouse navigation. Press the "q" key to exit "less" and continue. It will print the final report and offer to upload to pastebin site.
- Offers to post the results to the Ubuntu `pastebinit` provider if that program is installed, and a sufficiently reliable internet connection is available. This is the easiest way to share the sanitized results with the Ubuntu Comminity for support. After succssful upload to the pastebin, it will both display and log the URL of the uploaded report (`~/suport-info-link.log`), for you to copy and paste in your post on the Ubuntu Forums.
- Future versions may have an option to create the archive `support-info.tar.gz` if the report exceeds 19.5 kB in size.


## Run from CLI

You can either run it from the command line with these commands:

    wget -N -t 5 -T 10 https://github.com/UbuntuForums/wireless-info/raw/master/wireless-info/support-info/support-info && \
    chmod +x Report.sh && \
    ./Report.sh

This will download the script, make it executable, and run it, all in a row.

## Run from GUI

Or, if `zenity` or `kdialog` is installed, run it from the GUI this way:

1. [Download][1] the script
2. Make it executable
3. Run it from your file browser or a Run dialog

[1]: https://github.com/UbuntuForums/wireless-info/raw/master/wireless-info/support-info/support-info
