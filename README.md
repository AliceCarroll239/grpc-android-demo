GRPC Android Demo
=================

About
-----

As there seems to be currently no ready-to-go example for an Android application communicating with
a GRPC server which doesn't involve setting up a boatload of tools we decided to create this simple
demo project which contains a simple GRPC Java server and a matching Android client.

The setup contains working code generation so feel free to change the proto file in lib_hello_grpc.
You'll just have to adapt the server and client code to the newly generated GRPC java classes. The
compiler will point you to the locations you have to adapt.

Setup
-----

The following documentation assumes that you've installed Android Studio. Import the project via
gradle.

Running the server
------------------

By default the server runs on port 8080, but you may change that via command line arguments or
directly in the code.

Run the server from Android Studio by right-clicking the `Server.java` in the `lib_hello_grpc`
module. This also creates a suitable run configuration which you can use to run the server again
later. Make sure, that only one server instance runs at a time (at least if you attempt to use the
same port).

Incoming requests are logged on stdout.

Running the client
------------------

While importing the project to Android Studio via gradle the IDE automatically generates a run
configuration for the app which you can use to install it on your device or emulator.

In the app first type in the hostname and the port of your server. Then click on the `HELLO SERVER!`
button to execute a request against your GRPC server instance. In case of success the server will
reply with `Hello Android`.

Licence
-------

    Copyright (c) 2015, LOVOO GmbH
    All rights reserved.

    Redistribution and use in source and binary forms, with or without
    modification, are permitted provided that the following conditions are met:

    * Redistributions of source code must retain the above copyright notice, this
      list of conditions and the following disclaimer.

    * Redistributions in binary form must reproduce the above copyright notice,
      this list of conditions and the following disclaimer in the documentation
      and/or other materials provided with the distribution.

    * Neither the name of LOVOO GmbH nor the names of its
      contributors may be used to endorse or promote products derived from
      this software without specific prior written permission.

    THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
    AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
    IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
    DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE
    FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
    DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
    SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOEVER
    CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
    OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
    OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.