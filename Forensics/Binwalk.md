**Binwalk - Forensics - 30 Pts**

Challenge :

*Here is a file with another file hidden inside it. Can you extract it? https://mega.nz/#!qbpUTYiK!-deNdQJxsQS8bTSMxeUOtpEclCI-zpK7tbJiKV0tXYY*


So we need to find a way to read all of the embbeded files. I tried to extract the files but couldn't get to decompress the .zlib archive. I then switched to using  the `foremost` cli-tool that helps to recover deleted or lost files by scanning a device or disk image and reconstructing files based on their unique headers, footers, and internal data structures.

Anyway :

![](https://github.com/Kaalig/CTFLearn-Writeups/blob/42d01a166c98c842c4cb5ebb4bb1fe06592ad675/images/Pasted%20image%2020250721214657.png)

we had an output where we got two more png images. The flag is in one of those twos.
