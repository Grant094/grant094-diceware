# Diceware

<img src="./assets/img/dice.jpg" width="250" align="right" />

Feel free to check out the live version at [https://diceware.grantoxer.com/](https://diceware.grantoxer.com/).

Weak passwords are a big flaw in computer security due to a lack of "entropy" or randomness. For example, how many times have you used the name of a pet or relative or street in a password, or perhaps the number "1". Not very random, is it? :-) Worse still, if passwords are reused between services, that increases your security risk.

Fact is, humans are terrible at remembering random combiations of letters and numbers, but we are great at remembering phrases of words. That's where Diceware comes in.

Diceware is based on the proposal at [http://world.std.com/~reinhold/diceware.html](http://world.std.com/~reinhold/diceware.html) wherein virtual dice are roled 5 times, and the 5 digit number used against a lookup table of words. 4 dice rolls gives you 4 random words which are easy for a human being to remember, yet have a high amount of entropy which makes them hard to crack.

For more information on Diceware:
- [The Diceware Passphrase FAQ](http://world.std.com/~reinhold/diceware.html)
- [Diceware word list](http://world.std.com/~reinhold/diceware.wordlist.asc)
- [Diceware for Passphrase Generation and Other Cryptographic Applications](http://world.std.com/~reinhold/diceware.txt)

# Development

This app is built with <a href="https://webpack.js.org/">Webpack</a>.

When done editing `main.js`, the packed file can be built by simply running `webpack` 
on the command line.  It will be writing to `dist/bundle.js`.  To run webpack in a 
mode so that it regularly checks for changed files, run `webpack --watch --mode development`.

A local webserver can be set up by running `npm install http-server -g` to install it, then `http-server` to listen on http://localhost:8080/

## In summary:

- Development
    - `npm run clean` - Cleanup after a previous run
    - `npm install` - Install NPM packages used by Diceware
    - `webpack --watch --mode development` - Run webpack to pack Javascript files and watch for changes.
    - `http-server` - Run server
- Testing
    - `npm test` - Make sure you didn't break any of the core logic!
- Deployment
    - `npm install && webpack --mode production` - Webpack Javscript files in production mode (smaller file but takes longer)

## In practice:

- `npm run clean && npm install && webpack --watch --mode development` - Run webpack in dev mode while working on Javascript
   - `http-server` - Stand up a local HTTP server
- `npm run clean && npm install && webpack --mode production` - Run webpack in prod mode to produce final Javascript bundle

## Render Settings
If you deploy this site via Render, like I do, use these settings:
- Service Type: Web Service
- Build Command: `npm install && webpack --mode production`
- Start Command: `npm install http-server -g && http-server`

# Who built this? / Contact

My name is Grant Oxer, and I am an aspiring software engineer in Seattle.

There are several ways to get in touch with me:
- [LinkedIn](https://linkedin.com/in/groxer)
- [GitHub](https://github.com/Grant094)

Feel free to reach out to me if you have any comments, suggestions, or bug reports.

