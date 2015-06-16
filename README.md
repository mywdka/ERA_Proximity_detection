# ERA_Proximity_detection
Object proximity detection using the EasyRadio Advanced modules
An example of using the Easy Radio Advanced TRS modules as way to detect and identify object proximity.

The ERA modules can be configured to prepend an RSSI byte to the received data payload.
This information can be used to see if the transmitting object is within a certain range of
the receiver. This is not a definite measure as orientation, movement and objects wihtin the
line of sight of the transmitter and receiver can significantly alter the signal strength.

This example will trigger an action based on the object ID in range. It will retrigger after
REACTIVATE_DELAY milliseconds, or after the object has been out of range first.

The RSSI value will need to be determined by experimentation. An indication on the received
value and the signal strength can be found in the datasheet (see link below). The min/max value
depends on the transmition band. To change the trigger threshold change SEEN_THRESHOLD.

http://www.lprs.co.uk/assets/media/downloads/easyRadio%20Advanced%20Datasheet.pdf
