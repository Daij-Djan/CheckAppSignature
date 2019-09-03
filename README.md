CheckAppSignature
=================

Run the CheckAppSignature.sh script on the command line and pass it the path to an ipa or an extracted ios app as argument. 

E.g. Run:
    
    $ CheckAppSignature.sh /Users/dpich/Downloads/myApp-arm64-debug.ipa

How it works
------------

IPA file is extracted into a temp directory, and then

    codesign -dvvv /path/to/the.app

and

    codesign -d --entitlements :-

is run.

See
[TN2250: Understanding and Resolving Code Signing Issues](http://developer.apple.com/library/ios/#technotes/tn2250/_index.html#//apple_ref/doc/uid/DTS40009933)
for more info.
