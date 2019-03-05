# zxcvbn
A command-line implementation of the open-source zxcvbn password-strength tool

To use:

- You must have node installed. Type `node --version` on the command-line. If you get an error, download Node from https://nodejs.org/en/download/current/

Download my `zxcvbn` stript and put in your path, or put in your home directory:

    # from the directory where you downloaded my zxcvbn script, type:
    chmod +x zxcvbn

To install the npmjs module 'zxcvbn' type:

    sudo npm install -g zxcvbn

To run this script:

    ./zxcvbn
    # if that gives an error, try
    node zxcvbn
    
It will sit and wait for you to input a password.  Press ENTER to generate a report about the password you entered.

This does not save your password to the command-line bash history, but does output it to your screen.
