Nabless: use your Vault without Nabless (stand-alone copy)
===========================================================

This folder is the page nabless.com/rescue as plain files. It needs no
Nabless server. It talks only to the network address you give it and to a
wallet in your browser.

How to open it
--------------
It must be served by a web server, at the root of an address. Opening the
file from disk (file://) does not work: passkeys need a real address.

On your own computer, from inside this folder, either of these will do:

    python3 -m http.server 8080
    npx serve -l 8080 .

then open http://localhost:8080/rescue/ in your browser.

On the web: put the whole folder at the root of an https address you
control, and open https://<that address>/rescue/.

What you need to know
---------------------
- A passkey only works at the address it was made on. Your Nabless passkey
  was made for nabless.com and does nothing here.
- With your recovery kit and your backup key you can put a new passkey on
  your Vault from this copy ("Get back in with my kit and my backup key").
  The new passkey is made for the address this copy is served from, so keep
  using the same address afterwards (for example always http://localhost).
- You also need your Vault file, saved from the app while Nabless worked.
- Only use a copy from a source you trust. Compare SHA256SUMS.txt with the
  list published by that source. A false copy cannot move your money
  without your approvals, but it could ask for your kit, your backup key
  and their passwords.
- This page never asks for a seed phrase or a private key.
