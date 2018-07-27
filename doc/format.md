# FASCIA format

The FASCIA format is a simple JSON format to exchange information from mobile network monitoring devices (such as IMSI catchers, passive analysis tools) into
a common simple format and to be processed by FASCIA. The format can be used for GSM, UMTS/WCMDA or LTE networks.

## Format


| key  | format | description |
| ------------- | ------------- | --------- |
| timestamp     | datetime      | timestamp in UTC when the event was captured           |
| radiotype     | string        | Network type (such as GSM, UMTS/WCMDA, LTE) |
| sensor        | string        | a GUID representation of the sensor capturing the event |
| imsi | string  | IMSI in the following format (270 01 60000000001)          |
| tmsi1 | string | An hexadecimal representation of the TMSI 1 |
| tmsi2 | string | An hexadecimal representation of the TMSI 2 |
| imsi-country | string | country (if lookup available) |
| imsi-brand   | string | operator brand (if lookup available} |
| imsi-operator | string | operator (if lookup available) |
| mcc | integer | mobile country code (MCC) |
| mnc | integer | mobile network code (MNC) |
| lac | integer | location area code (LAC) for GSM/UMTS or tracking area code (TAC) for LTE |
| cell | integer | Cell ID (CID) of the base transceiver stations (BTS) for GSM and LTE. For UTMS, this is the UTRAN cell id with the addition of the radio network controller (RNC).|
| unit | integer | Primary scrambling code (PSC) for UTMS. Physical cell id (PCI) for LTE. For GSM, the field is empty. |

