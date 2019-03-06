# pw
A command-line implementation of the open-source zxcvbn password-strength tool to check password strength

To use:

- You must have node installed. Type `node --version` on the command-line. If you get an error, download Node from https://nodejs.org/en/download/current/

# Install my `pw` script:

- Download my `pw` stript (it's an executable text file) and install into `/usr/local/bin/`
- Once downloaded, make the script executable. Do this by typing:

    chmod +x /usr/local/bin/pw

This script has a dependency of the npm module called `zxcvbn`, so install it by typing

    sudo npm install -g zxcvbn

If you got an error that npm command is not found, verify that you have `node` installed.  See above.

# To run this script, just type:

    pw

Type a password to check, then press ENTER.  Nothing will happen until you press enter.

It's safe to type your password because:

- Your password stays on your local machine. Nothing is transmitted to the Internet or saved to a file.
- Your password is not saved to bash history.

----------

Example use for password `Z,W}13[H7OLc`:

    /usr/local/bin/pw
    Z,W}13[H7OLc
    
    Strength score (0=worst, 4=best): 4
    
    Estimated time to crack this password:
      Online (slow) at 100 guesses per hour      : centuries
      Online (fast) at 10 guesses per second     : centuries
      Offline (slow) at 1,000 guesses per second : 3 years
      Offline (fast) at 10 billion guesses/second: 2 minutes

Another example, this with less-secure password of `P@ssword1`:

    /usr/local/bin/pw
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
