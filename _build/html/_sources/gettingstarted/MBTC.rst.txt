Syncing the Modified Bitcoin Core v0.18.1
************************************************

Now that you've built the wallet program, you're ready to download and sync the Modified Bitcoin Core.

1. Download the `Modified BTC`_ and unzip it.
2. Run combfullui.exe, and a black window should appear. Do not close this window.
3. Go to the "btc" folder and open the "bin" folder. You should see a file called "bitcoin-qt.exe".
4. Run bitcoin-qt.exe, and choose a directory to store the BTC blockchain information. This location should have over 400GBs of free space.
5. Once BTC window finishes synchronizing the headers and begins to download blocks, close the BTC window and run bitcoin-qt.exe again.

Now to wait. It may take several days to finish downloading the full BTC blockchain. If your're an expert and you've opted to copy over information from a previously existing BTC download, you will see a "Rescanning" screen at startup. It may appear as if there is no progress, but there is. Wait until the rescanning has finished.

While the BTC chain is downloading, it is a good idea to familiarize yourself with Haircomb's Usage Guidelines. Haircomb relies on building certain files that can be corrupted easily when used incorrectly. If you want to save yourself a headache, follow those guidelines very strictly.



 .. _Modified BTC: https://github.com/natasha-otomoski/bitcoin/releases/tag/0.18.1-prod