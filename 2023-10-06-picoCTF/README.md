# picoCTF Scavenger Hunt

## Description
There is some interesting information hidden around this site http://mercury.picoctf.net:39491/. Can you find it?

## Page Inspection
My first thought after seeing nothing interesting on the page itself was to open the inspection tool. I tabbed to the 'Sources' and on the (index) page I immediately see the first part of the flag as a comment in the HTML:

```<!-- Here's the first part of the flag: picoCTF{t -->```

Then I tabbed over to the 'mycss.css' file and scrolled to the bottom to be met with part 2 also commented out:

```/* CSS makes the page look nice, and yes, it also has part of the flag. Here's part 2: h4ts_4_l0 */```

Finally, 'myjs.js' had an interesting comment:

```/* How can I keep Google from indexing my website? */```

## Time to Google
The question in 'myjs.js' prompted me to search information on how to find the indexed pages on google. Which led me to google:

> site:http://mercury.picoctf.net:39491/

Both links led to part 3 and 4 of the flag.

The first link directed me to http://mercury.picoctf.net:39491/robots.txt revealing part 3:

> Part 3: t_0f_pl4c

The second link on the google results page led me to http://mercury.picoctf.net:39491/.htaccess/ granting me part 4 of the flag:

> Part 4: 3s_2_lO0k # I love making websites on my Mac, I can Store a lot of information there.

In addition to the flag was the last clue. 'Mac' and 'Store' both were capitalized so I googled 'mac store information website.' A poorly worded search, I know. But a few links down I noticed 'DS_Store.'

> In the Apple macOS operating system, .DS_Store is a file that stores custom attributes of its containing folder, such as folder view options, icon positions ...

I took a shot in the dark and made the URL path http://mercury.picoctf.net:39491/.DS_Store which led me to the final part of the flag:

> Congrats! You completed the scavenger hunt. Part 5: _f7ce8828}

## The Flag
picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_f7ce8828}