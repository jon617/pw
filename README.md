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

----------

Example:

    ./zxcvbn
    Z,W}13[H7OLc
    
    Strength score (0=worst, 4=best): 4
    
    Estimated time to crack this password:
      Online (slow) at 100 guesses per hour      : centuries
      Online (fast) at 10 guesses per second     : centuries
      Offline (slow) at 1,000 guesses per second : 3 years
      Offline (fast) at 10 billion guesses/second: 2 minutes

Another example:

    ./zxcvbn
    P@ssword1
    
    Strength score (0=worst, 4=best): 1
    
    Estimated time to crack this password:
      Online (slow) at 100 guesses per hour      : 5 days
      Online (fast) at 10 guesses per second     : 19 minutes
      Offline (slow) at 1,000 guesses per second : 1 second
      Offline (fast) at 10 billion guesses/second: less than a second
    
    Warning: This is similar to a commonly used password
    Suggestions: 
      Add another word or two. Uncommon words are better.
      Capitalization doesn't help very much
      Predictable substitutions like '@' instead of 'a' don't help very much
