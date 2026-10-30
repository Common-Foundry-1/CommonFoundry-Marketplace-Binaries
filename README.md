# Common Foundry GPU marketplace: renter kit

Rent a GPU from the Common Foundry marketplace beta and pay for it in CMFD.
The kit signs your PC up with Common Foundry by itself; during the beta the
number of renters is limited.

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
3. The window enables this PC with Common Foundry, sets it up and opens
   the renter app in your browser. Leave it open until then.
4. Send CMFD from your own wallet to the renter address the window shows
   (about 3 CMFD covers a first test rental; the unused part comes back),
   then pick a GPU and a template in the app and rent.

Next time, open the app with **Open CMFD Renter** on your Desktop. Keep the
PC on while a rental runs; the app pays for it as it goes.

If the app says Common Foundry refused your address, your internet address
has changed: run **Start CMFD Renter** again. It enables the new address
by itself. The same happens after about two weeks without using the app:
access lapses, and the next start renews it.

If the window says the beta is full, try again in a day or two.

## Get your CMFD back

In the updated app, open **Wallet**. Confirmed rental returns are included
in **Available** automatically, without a separate collection transaction.
Under **Withdraw**, paste your own
wallet's address (the `cmfd1…` form catches typos; with an older wallet
that shows only the 64-character form, check every character), choose to
send everything or to keep some, click **Review withdrawal**, check the
address and amount, and click **Send**. Wait until the transaction is
mined before renting or withdrawing again.

**Returning** is an estimate while settlement or a timeout refund is pending;
it is not spendable yet. Keep the payment agent running until rentals close.
Older kits may still require **Collect refunds** before withdrawal.

See [Returns, fees and compensation](REFUNDS.md) for cancellation before
launch, failed starts, network fees, and reporting service problems.

## Update

Already have the kit? Unzip the new one and double-click its **Start CMFD
Renter**. Your wallet, rentals and settings stay, and **Open CMFD Renter**
on your Desktop opens the new version from then on.

`README-FIRST.txt` inside the kit has a few more tips.
