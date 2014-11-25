Nexage SourceKit-VAST for Android
=====================================

Nexage SourceKit-VAST for Android is an open sourced IAB VAST 2.0 compliant rendering engine for HTML ad creatives.

For more information on IAB VAST 2.0 compliance please visit http://www.iab.net/guidelines/508676/digitalvideo/vsuite/vast/vast_copy

**Features:**

- VAST 2 implementation
- Handles VAST & VAST Wrapper
- Optionally choose to validate with Xerces

**Requirements:**

- Android 2.3+
- Eclipse + ADT

Getting Started
===============

Step 1: Import the VAST project into your Eclipse workspace.

Step 2: Include the VAST library in your project under Project Properties -> Android -> Library.

Step 3: Add the following Activity into AndroidManifest.xml under the <application> tag.

	<activity
		android:name="org.nexage.sourcekit.vast.activity.VASTActivity"
		android:theme="@android:style/Theme.NoTitleBar.Fullscreen" />

Step 4: Add the following permissions to the AndroidManifest.xml under the <manifest> tag.

	<uses-permission android:name="android.permission.INTERNET"></uses-permission>
	<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE"></uses-permission>

Step 5: Use VASTPlayer in your project.

	VASTPlayer vastPlayer = new VASTPlayer(this, this);
	vastPlayer.loadVideoWithData(vastXMLContent);
	// OR: vastPlayer.loadVideoWithUrl(urlOfContent);

Implement VASTPlayerListener in your activity to listen for VASTPlayer ready or fail events.

After you've received the vastReady callback you can play the video.

	vastPlayer.play();

That's it!


LICENSE
=======

Copyright (c) 2014, Nexage, Inc.<br/>
All rights reserved.<br/>
Provided under BSD-3 license as follows:<br/>

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are
met:

1.  Redistributions of source code must retain the above copyright notice,
    this list of conditions and the following disclaimer.

2.  Redistributions in binary form must reproduce the above copyright
    notice, this list of conditions and the following disclaimer in the
    documentation and/or other materials provided with the distribution.

3.  Neither the name of Nexage nor the names of its
    contributors may be used to endorse or promote products derived from
    this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS
IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED
TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A
PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT
HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED
TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR
PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF
LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING
NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS
SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
