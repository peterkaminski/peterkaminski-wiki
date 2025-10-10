#  Backed up my 1Password passwords to a semi-permanent archive

_Last updated: 2023-12-03_

_Mastodon: https://mastodon.social/@peterkaminski/111518205275247228_

I'm very pleased with myself, I've backed up my 1Password passwords to a semi-permanent archive: 8 sheets of paper and ink (46kb, encrypted with GPG symmetric).

Longevity of data on USB thumbdrive or hard drive in storage: single digit years or less.

Longevity of ink on paper: decades or centuries, if you keep water and fire away.

A useful page for deciding on storage format (I went vanilla): https://www.monperrus.net/martin/perfect-ocr-digital-data

Next up, someday: do a better writeup and test/document OCR + data recovery.

## Image and Alt Text

![[PXL_20231203_185928542.jpg]]

Photograph of the top half of eight sheets of printer paper fanned out on top of a computer keyboard. We can see the contents of the top half of the first sheet. It was printed from the Chrome web browser, with a small header line showing the date and filename.

The bulk of the text is hexadecimal digits in monospace font, filling the page. The bits of the subsequent pages we can see appear to be more of the same.

At the top of the first page are semi-cryptic notes, "Output created with" and some arcane shell commands that manipulate files, and handwritten notes on how to recover and decrypt the digital data.

Transcription of top text follows.

Output created with:

export FN=1PasswordExport-MASKED-20231203-072003.csv.gpg
cat $FN | od -t x1 -An -v | tr -d ' \n' | fold -w 96 >body.html
cat header.html body.html footer.html >$FN.html

To recover, OCR, then with just the hex saved to file.csv.gpg:

gpg --decrypt file.csv.gpg > file.csv

## Improved header.html

```html
<html><body><pre>
Output created with:

export FN=1PasswordExport-MASKED-20231203-072003.csv.gpg
cat $FN | od -t x1 -An -v | tr -d ' \n' | fold -w 96 >body.html
cat header.html body.html footer.html >$FN.html

To recover, OCR and save just the hex to "decrypted-passwords.csv.gpg"

Decrypt with:

export FN=decrypted-passwords.csv
gpg --decrypt $FN.gpg > $FN
```

## footer.html

```html
</pre></body></html>
```

