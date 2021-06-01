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
```
Give examples
```
