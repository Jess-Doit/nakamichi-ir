# Flipper IR Quick Reference

Quick reference for the parsed NEC commands in the Flipper Zero files in this
folder. Address and command values are shown as hexadecimal bytes from the
Flipper `.ir` files.

## Nakamichi RM-7C

Tested with a Nakamichi CR-7A cassette deck. The source file is
[`Nakamichi_RM-7C.ir`](Nakamichi_RM-7C.ir).

| Button | NEC address | NEC command |
| --- | --- | --- |
| Stop | `67` | `11` |
| Play | `67` | `1D` |
| Rewind | `67` | `10` |
| Fast Forward | `67` | `1C` |
| Pause | `67` | `12` |
| Record | `67` | `1E` |
| Azimuth Left | `67` | `13` |
| Azimuth Right | `67` | `1F` |

## Nakamichi RM-2TA

Tested with a Nakamichi TA-2A tuner/amplifier. The source file is
[`Nakamichi_RM-2TA.ir`](Nakamichi_RM-2TA.ir).

### Amplifier and inputs

| Button | NEC address | NEC command |
| --- | --- | --- |
| Power | `5C` | `00` |
| Mute | `5C` | `01` |
| Vol Down | `5C` | `03` |
| Vol Up | `5C` | `02` |
| Input Phono | `5C` | `44` |
| Input CD | `5C` | `45` |
| Input Tuner | `5C` | `46` |
| Input Video | `5C` | `47` |
| Input Tape | `5C` | `49` |

### Tape

| Button | NEC address | NEC command |
| --- | --- | --- |
| Tape RW | `5C` | `55` |
| Tape FF | `5C` | `54` |
| Tape Rev | `5C` | `58` |
| Tape Play | `5C` | `15` |
| Tape Rec | `5C` | `14` |
| Tape Cue | `5C` | `56` |
| Tape Stop | `5C` | `17` |
| Tape Pause | `5C` | `16` |

### CD

These commands are present in the file but have not yet been tested with a
compatible Nakamichi CD player.

| Button | NEC address | NEC command |
| --- | --- | --- |
| CD RW | `67` | `C1` |
| CD FF | `67` | `C7` |
| CD Prev | `67` | `C2` |
| CD Next | `67` | `C8` |
| CD Disc Scan | `67` | `93` |
| CD Stop | `67` | `C5` |
| CD Pause | `67` | `CB` |
| CD Play | `67` | `C6` |
| CD Random | `67` | `DB` |
| CD Disc | `67` | `8F` |

### Tuner

| Button | NEC address | NEC command |
| --- | --- | --- |
| T Preset Dn | `5C` | `13` |
| T Preset Up | `5C` | `12` |
| T AM | `5C` | `06` |
| T FM | `5C` | `07` |
| T Seek Dn | `5C` | `05` |
| T Seek Up | `5C` | `04` |

## Notes

- The complete parsed signals remain in the `.ir` files above.
- These values use the NEC protocol. The files do not include raw pulse timing
  or carrier-frequency details.
- Button behavior can vary between Nakamichi models and should be verified on
  the target equipment.
