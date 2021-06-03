# *Secure Message*
## Introduction
Secure Message is an android application that uses SMS as mode of communication and a 128 bit AES encryption/decryption algorithm to secure the messages. The app can run on Android versions 4.0 and above.

### Technologies used

* Android Studio
* Java
* XML

### Modules

* ``activity_main.xml`` is the layout XML file for layout of the front page of the app (Sender).

* ``Onreceive.xml`` is the layout XML file for layout of the second page of the app where the receiver receives the text from sender (Receiver).

* ``EncDecSMSActivity.java`` is the main activity class to send message. The message is encrypted using 128 bit AES encryption algorithm, which uses a 16 character secret key.

* ``DisplaySMSActivity.java`` is the main activity class to receive message. This class receives the encrypted message from the sender, decrypts the cipher text and displays the original plain text.

* ``SMSBroadcastReceiver.java`` is the main activity class to send message. It uses ``android.provider.Telephony.SMS_RECEIVED`` and class ``BroadcastReceiver`` to send the message as SMS.

* ``AndroidManifest.xml`` is the main manifest file which declares the function intents and user permissions like ``<uses-permission android:name="android.permission.SEND_SMS"/>`` to send SMS and ``<uses-permission android:name="android.permission.RECEIVE_SMS" />`` to receive SMS

### Working method

The sender first enters the recipient's mobile number (in the given screenshots below I've run it on the Android Studio emulator, hence I've used the emulator port number instead of an actual mobile number), followed by a 16 character secret key which is used to encrypt the plain text. The sender then types in the desired message to be sent (In my example I've sent "Test Message") in the next field, and then hits the send button. On the Receiver's end the encrpyted message (cipher text) shows up along with the secret key input, which the receiver has to type in and then the cipher text is decrypted.

You will receive the cipher text in your default messaging app as well, but only this app will decrypt the message for you.

### Screenshots 
Sender:
![sender](https://user-images.githubusercontent.com/45178771/120397626-40ff2980-c356-11eb-964b-dbeb6c9c865d.png)

Receiver:
![receiver](https://user-images.githubusercontent.com/45178771/120397647-4b212800-c356-11eb-8211-350e9152e887.png)
