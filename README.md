# Common Foundry GPU marketplace: renter kit

Rent a GPU from the Common Foundry marketplace beta and pay for it in CMFD.
During the beta, renting needs an invitation: the kit shows an access line
that you send to Tim, and it finishes setting up once you are enabled.

## Download

Get the kit for your system from the
[latest release](../../releases/latest):

- **Windows 10 or 11:** `CMFD-Renter-Kit-Windows.zip`. It brings everything
  it needs, Python included.
- **Linux:** `CMFD-Renter-Kit-Linux.zip`. It needs `python3` and `ssh`.

`SHA256SUMS` in the release lists each file's checksum.

## Start

1. Unzip the kit somewhere you will keep it, for example Documents.
2. Double-click **Start CMFD Renter** (on Linux, run
   `./start-cmfd-renter.sh`). If Windows asks, click Run.
3. It shows a line starting `CMFD-ACCESS-1` and, on Windows, copies it for
   you. Paste it to Tim and leave the window open. The line holds no
   password or key.
4. Once Tim has enabled you, the window carries on by itself and opens the
   renter app in your browser.
5. Send CMFD from your own wallet to the renter address the window shows
   (about 3 CMFD covers a first test rental; the unused part comes back),
   then pick a GPU and a template in the app and rent.

Next time, open the app with **Open CMFD Renter** on your Desktop. Keep the
PC on while a rental runs; the app pays for it as it goes.

If the app says Common Foundry refused your address, your internet address
has changed: run **Start CMFD Renter** again and send Tim the new line.

`README-FIRST.txt` inside the kit has a few more tips.
