# Metirionic

[Bluetooth Channel Sounding](https://www.bluetooth.com/blog/bluetooth-channel-sounding/) solutions for precise distance measurement and proximity applications.

Based in Dresden, Germany — [metirionic.com](https://metirionic.com)

## MARS — Metirionic Advanced Ranging Stack

**MARS** is our proprietary ranging middleware for Bluetooth Channel Sounding. It processes raw CS subevent data (I/Q samples) and produces accurate distance estimates using the Pathfinder algorithm — even in multipath-heavy environments.

The open-source projects in this organization are the building blocks that work with MARS:

- **[mars-bluetooth-hci](https://github.com/Metirionic/mars-bluetooth-hci)** — Rust library for parsing Bluetooth HCI events related to Channel Sounding. It decodes CS subevent data from the BLE controller and makes it available to the MARS processing pipeline or custom applications.

- **[mars-cs-nrf54l](https://github.com/Metirionic/mars-cs-nrf54l)** — Zephyr RTOS firmware for Nordic nRF54L15 hardware. Provides ready-to-flash initiator and reflector samples that perform CS procedures and output ranging data over UART. The initiator firmware uses `mars-bluetooth-hci` to serialize CS measurements via COBS framing, which can then be fed into MARS for distance estimation.

### How they fit together

```
nRF54L15 hardware
  └─ mars-cs-nrf54l (firmware)
       ├─ Reflector: advertises & responds to CS procedures
       └─ Initiator: connects, runs CS, outputs COBS-encoded data over UART
            └─ mars-bluetooth-hci (Rust library)
                 └─ Parses HCI events into structured CS subevent data
                      └─ MARS (proprietary)
                           └─ Pathfinder algorithm → distance estimates
```

## Open-source projects

| Repository | Language | Description |
|------------|----------|-------------|
| [mars-cs-nrf54l](https://github.com/Metirionic/mars-cs-nrf54l) | C | nRF54L15 Channel Sounding firmware samples |
| [mars-bluetooth-hci](https://github.com/Metirionic/mars-bluetooth-hci) | Rust | HCI event parsing library for BLE Channel Sounding |

## Learn more

- [Metirionic Advanced Ranging Stack (MARS)](https://metirionic.com/products-and-services/mars/)
- [How Channel Sounding works](https://metirionic.com/metirionic-technology/how-it-works/)
- [Evaluation Kit & Demo App](https://metirionic.com/products-and-services/evaluation-kits-and-applications/)
- [LinkedIn](https://www.linkedin.com/company/metirionic) · [YouTube](https://www.youtube.com/channel/UCsDorFeM-ZlLZtv9t5_JDUQ)