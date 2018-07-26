# FASCIA format

The FASCIA format is a simple JSON format to exchange information from mobile network monitoring devices (such as IMSI catchers, passive analysis tools) into
a common simple format and to be processed by FASCIA.

## Format


| key  | format | description |
| ------------- | ------------- | --------- |
| timestamp     | datetime      | timestamp in UTC when the event was captured           |
| sensor        | string        | a GUID representation of the sensor capturing the event |
| imsi | string  | IMSI in the following format (270 01 60000000001)          |
| tmsi1 | string | An hexadecimal representation of the TMSI 1 |
| tmsi2 | string | An hexadecimal representation of the TMSI 2 |
| imsi-country | string | A string representation of the country (if lookup available) |
| imsi-brand   | string | A string representation of the operator brand (if lookup available} |
| imsi-operator | string | A string representation of the operator (if lookup available) |
| mcc | integer | An integer representing the mobile country code (MCC) |
| mnc | integer | An integer representing the mobile network code (MNC) |
| lac | integer | An integer representing the location area code (LAC) |
| cell | integer | An integer representing the Cell ID (CID) of the base transceiver stations (BTS) |

