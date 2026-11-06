# ER-102 Sequencer Controller

Fork of [odevices/er-102](https://github.com/odevices/er-102) (Orthogonal
Devices). The upstream repository holds no firmware source for the ER-102: it
contains the default configuration file and the voltage-table scripts. This
fork keeps them alongside the [ER-101 firmware fork](https://github.com/fluxxion82/er-101),
whose changes must keep the ER-102 pairing working.

## Contents

- `config/default-config.ini` — the module's default configuration file
- `voltage-tables/python/` — scripts that generate voltage tables in the
  binary format the ER-102 loads from its SD card: `chromatic/generate.py`
  (scales on the twelve chromatic degrees), `csv/csv-to-voltage-table.py`
  (CSV to binary) and `just-intonation.py` (an algorithmic example)
- `voltage-tables/scala/` — Scala scale files

The scripts are **Python 3** (ported from Python 2 in this fork). They need
no packages beyond the standard library.

## Pairing with the ER-101 firmware fork

The ER-101 firmware fork is versioned 3.x. Every ER-101 release that touches
code shared with slave mode is checked against the ER-102 before release. The
table below records what has been paired and tested; it is filled in from the
bench, not from reading code.

| ER-101 firmware | ER-102 firmware | Tested | Result |
|---|---|---|---|
| 2.10 (shipped) | (read from the module) | — | baseline, to be recorded at the first bench session |
| 3.0.0 | | | |

## Credit

Orthogonal Devices built both modules and published these files; the
compatibility notes for the pairing are kept with the ER-101 fork.
