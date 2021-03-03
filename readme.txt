# RemindersGeneral
General reminders of commands and shortcuts

ImageMagick 
$ convert img.gif -crop 32x32 +repage out%03d.gif



Mac Shortcuts [unofficial cheat sheet]
Cmd+shift+h - go home
Cmd+dn - open
Alt+dn - cursor to bottom file
Fn+backspace - delete

Finder
alt+up - jump to top
cmd+up - go to containing folder
cmd+down - open with default app
cmd+shift+h - go to Home folder


VSCode
ctrl+shift+right - expand selection to enclosing brackets
cmd+shift+\ - jump to matching bracket
cmd+shift+l - select all occurrences  of current selection
alt+shift+drag - box select
xmd+alt+f - Find & Replace
cmd+l - select line
cmd+alt+shift+c - In File Explorer, copy a file's relative path


Outlook (PC)
Ctrl+Shift+i - Inbox


GMail Shortcuts
? - more shortcuts
g, i - to go inbox
/ - search inboxes. Or within email
u - Back to threadlist
x - select conversation (mail)
d - delete (customised)
arrow - move blue vertical cursor up/dn emails
p - previous mail
n - next mail
k - later mail
j - earlier mail
(shift+8)*+a - select all
(shift+8)*+n - deselect all
c - compose new email in current tab
# - compose new email in new tab (swapped d)
r - reply
Shift+i - Mark as read
Shift+u - Mark as unread
cmd+\ - Remove formatting

GDrive Shortcuts
/ = search
Ctrl+/ = keyboard shortcuts. Searchable
Shift+t = new doc
Shift+f = new folder
p = preview. Works for GDocs, text files and PDFs
Esc = exit preview and popups
n = rename
z = move to folder
g = show the ‘file cursor’
g, p = go up a folder level
Compact view - settings, pick view > Compact
s = star a folder. New?
g, f = focus on folder tree in side panel?

GDocs
Cmd+/        shortcuts
Cmd+\        remove formatting (backslash)
Increase font size    ⌘ + Shift + .
Decrease font size    ⌘ + Shift + ,
Cmd+f        Find
Cmd+shift+h    Find and replace
Cmd+shift+v    paste without formatting
⌘ + Option + o  Apply normal text style
⌘ + Shift + c    Word count
Esc        exit the Find popdown. Find again to focus and then Esc.
Cmd+alt+shift+h = see version history
⌘ + z        Undo
⌘ + Shift + z    Redo
⌘ + k        Insert or edit link
Page up    Fn + Up arrow
Page down    Fn + Down arrow
Left align    ⌘ + Shift + l
Center align    ⌘ + Shift + e
Right align    ⌘ + Shift + r
Justify    ⌘ + Shift + j
Numbered list    ⌘ + Shift + 7
Bulleted list    ⌘ + Shift + 8
Select current list item holding Ctrl + ⌘ + Shift, press e then i
Move to next link    holding Ctrl + ⌘, press n then l
Move to previous link    holding Ctrl + ⌘, press p then l
Cmd+shift+\    rightclick!
Show your browser's context menu     Shift + right-click
Strikethrough    ⌘ + Shift + x
Superscript    ⌘ + .
Subscript    ⌘ + ,


Youtube Shortcuts:
/        search
space        pause/play (need to have clicked video area (for Flash to take over?))
up/down    volume up/down
Shift+m    mute
Left/Right    Jump back/ahead 5 seconds
1-9        jump to that division(%) of the total video length, e.g. 5 = halfway point. Pity this overrides Firefox's tab selection +1-9.
0        back to start!
c        captions!
f        fullscreen
Esc        exit fullscreen
function+Right = next video in a playlist e.g. Watch Later
Home/End    (PC) Seek to the start/last seconds


Amazon. a script for Chrome console to add all list items to basket!
`Array.prototype.forEach.call(document.querySelectorAll('[data-action=reg-item-inline-order]'), function(e) { setTimeout(function() { e.click() }, 100) }) `

A Dark Room
`$SM.add(‘stores.steel’, 9999)`

Google
`<site>: <query>`

Firefox Shortcuts
cmd+shift+a - Add-ons
cmd+j - Downloadss


Web Dev
Local server (Python) on port 8081
$ http-server -p 8081

HTML Mini Ref
```
<h1 style=”font-size: 200; font-family: impact;”> HEY YOU! </h1>
<details><summary>collapsable section</summary> <p>content</p></details>
<img src=”” alt=””>
```

CSS Mini Ref
table { border-collapse: collapse; }

JS Mini Ref

PHP Mini Ref
$ php -S localhost:8888
var_dump()


Mini keyboard
AltGr+` - | (pipe)

SSH Keys
[From ProjSSH doc, which from ssh.com] 
$ ssh-keygen -f ~/<keyname>
Copy to server. enter system pw
$ ssh-copy-id -i ~/.ssh/<priv-key> <user>@<host>
Add to your auth agent
$ ssh-add <priv-key>
Optionally add a shortname to ~/.ssh/config . https://linux.die 
$ nano ~/.ssh/config



Terminal Mac
ctrl+k - delete from cursor to end



Terminal Scenarios

Upgrading
$ npm i -g npm
$ npm i -g n
$ n stable
$ brew update && brew upgrade

Show installed packages
$ compgen -c
$ dpkg --get-selections | less
$ apt-get list ?
$ brew list

Show all installed Node packages
$ npm ls -g --depth=0

Show installed Python modules
$ pydoc modules
$ pip list ?
$ pip3 list


Echo both alphabets
$ echo {A..z}

Echo special charas
$ echo -e ‘\n\n\n’

Number all Lines
$ nl a.txt > b.txt

A sequence of numbers
$ seq 10
Two times table
$ seq 2 2 10

$ mkdir 0{1..9} - make 9 directories named “01” etc
$ mkdir -p path/path - make nested directories. Works with bracket expansion
$ touch {0..1}{0..9}.txt  - make 20 text files “00”-”19”
$ touch 0{1..9}/{1..9}.txt - make 9 files in each folder, only if they exist.

Move file from ‘path/file’ to here:
$ mv ~/new1.sh  .

Delete every file starting s and then any letter but t (orig staff, then sa, sb, sc):
$ rm s[!t].txt
sometimes need:
$ rm s[0-9]*

Nested for loops
$ for i in {1..3}; do for i in {1..5}; do echo $i; done; done

Wipe all files in a folder:
$ for i in *; do : > $i; done

Translate all lowercase letters to uppercase
$ tr a-z A-Z < file.txt > output.txt
Delete all digits
$ tr -d 0-9 < filename
Delete all spaces
$ tr ‘ ‘ ‘’ < filename
Delete selected letters
$ echo "abcdef" | tr -d bcd
> aef
Replace letters, conversely
$ echo "acfdeb123" | tr -c b-d +
> +c+d+b++++
Squeeze multiple spaces into a single
$ tr -s ‘ ‘ ‘ ‘
Character types
$ echo "abcd2ef1" | tr [:alpha:] -
> ----2--1

Squeeze multiple consecutive blank lines into a single blank line.
$ cat -s

Show IP address
$ ipconfig getifaddr en1
Or narrow down ifconfig, but still 2 lines of info
$ ifconfig en1 inet
Or ask Google (for your public IP)

Reverse line order
$ tail -r  in.txt > out.txt

Extract a column of text in tab separated ‘table’
Raw “\t thing”
$ cut -f2 in.txt > out.txt

Set executable permissions
$ chmod 755 script.sh
Or
$ chmod +x
Check a file's executable permissions:
$ ls -l script.sh

My Favourite sed commands:
Delete the 2nd line
$ sed 2d
Delete every 2nd line
$ sed ‘n;d’
Delete 1st 15 lines
$ sed '1,15d'
[?] Delete repeating spaces at the start of all lines
$ sed 's/^ *//' input.txt > output.txt
Delete one space at the start of all lines
$ sed 's/^ //' input.txt > output.txt
Delete up to the $, leaving the $. (delete the user@host etc from my Terminal dump)
$ sed ‘s/^.*\$/\$/’
New line every 2nd line
$ sed G
[?] To replace the first line with another line in many text files
$ sed -i.bak '1s/^.*$/new line/' *.txt
Put a “$ “ at the start of every non-blank line, for my Terminal notes (mine!):
$ sed '/^$/!s/^/\$ /' file1.txt > file2.txt

To duplicate a file 39 times, and number them “01”-”39”
$ for i in {0..3}{0..9}; do cp f.txt "f0$i.txt"; done

Save a list of all the filenames in the current folder
$ ls > file.txt

List only the folders in these folders
$ ls -d */ > d1.txt    [tested?] [?]

Join all files
$ cat * > big.txt


To re-link some css files in html after moving folders around
$ sed -i.bak '/link/s/f="/f="..\/styles\//g' *html

Which line number contains only a number?
$ sed -n '/^[1-9]$/='     [?]
Which line number is the last line?
$ sed -n '$=' h1.txt

Swap columns in a tabbed table 1st+2nd
$ cut -f1 in.txt > 04.txt
$ cut -f2 in.txt > 05.txt
$ paste 05.txt 04.txt > out.txt

To swap a list of pairs so 2nd line is atop 1st,
delete the first line, and all blank lines (optional)
$ sed '1d; /^$/d'  mraw.txt > m1.txt
delete every 2nd line
$ sed 'n;d'  m1.txt > m2.txt
extract every 2nd line
$ sed -n 'n;p'  m1.txt > m3.txt
merge em
$ paste m3.txt m2.txt > m4.txt 
replace tabs (paste) with newlines
$ tr '\t' '\n' < m4.txt > m5.txt

Sort a bibliography alphabetically
$ sort in.txt | cat -s | sed G > out.txt

In man pages (Info). And Less
Shift+g - go to end
g - go to start

In Less, start at the end of the file
$ less +G file.txt
start at the search term "xyz"
$ less +/xyz

Date. Just the time
$ date +”%T”
Weekday name
$ date +”%A”
Time
$ date +”%T”
Current seconds
$ date +”%S”










