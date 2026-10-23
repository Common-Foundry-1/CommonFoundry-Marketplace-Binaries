# Common Foundry GPU marketplace: renter kit

Rent a GPU from the Common Foundry marketplace beta and pay for it in CMFD.
During the beta, renting needs an invitation: Tim sends you an invite code,
and the kit enables your PC with it.

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
3. Paste the invite code Tim sent you (it starts with `CMFD-`) and press
   Enter. The code works once, for this PC only.
4. The window enables this PC, sets it up and opens the renter app in your
   browser. Leave it open until then.
5. Send CMFD from your own wallet to the renter address the window shows
   (about 3 CMFD covers a first test rental; the unused part comes back),
   then pick a GPU and a template in the app and rent.

Next time, open the app with **Open CMFD Renter** on your Desktop. Keep the
PC on while a rental runs; the app pays for it as it goes.

If the app says Common Foundry refused your address, your internet address
has changed: run **Start CMFD Renter** again. It enables the new address
with your invite code by itself.

No invite code? Press Enter at step 3. The window then shows a line starting
`CMFD-ACCESS-1` and, on Windows, copies it for you. Send it to Tim and leave
the window open; it carries on once Tim has enabled you. The line holds no
password or key.

## Get your CMFD back

In the app, open **Wallet**. Under **Collect refunds**, bring back what
finished rentals returned. Then, under **Withdraw**, paste your own
wallet's address (the `cmfd1…` form catches typos; with an older wallet
that shows only the 64-character form, check every character), choose to
send everything or to keep some, click **Review withdrawal**, check the
address and amount, and click **Send**. Wait until the transaction is
mined before renting or withdrawing again.

## Update

Already have the kit? Unzip the new one and double-click its **Start CMFD
Renter**. Your wallet, rentals and settings stay, and **Open CMFD Renter**
on your Desktop opens the new version from then on.

`README-FIRST.txt` inside the kit has a few more tips.
