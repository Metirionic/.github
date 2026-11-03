# Metirionic

[Bluetooth Channel Sounding](https://www.bluetooth.com/blog/bluetooth-channel-sounding/) solutions for precise distance measurement and proximity applications.

Based in Dresden, Germany — [metirionic.com](https://metirionic.com)

## MARS — Metirionic Advanced Ranging Stack

**MARS** is our proprietary ranging middleware for Bluetooth® Channel Sounding. It processes raw Channel Sounding subevent data, including I/Q samples, and produces accurate distance estimates even in multipath-heavy environments.

The public repositories in this organization provide evaluation tools and integration building blocks around MARS:

* [`mars-ranging-demo`](https://github.com/Metirionic/mars-ranging-demo) — Windows desktop application for visualizing continuous Bluetooth Channel Sounding distance measurements between an initiator and a reflector development kit. The app provides live distance monitoring, signal-path insight, and export of measurement data for further analysis.
* [`mars-cs-nrf54l`](https://github.com/Metirionic/mars-cs-nrf54l) — Zephyr RTOS firmware for Nordic nRF54L15-based hardware. Provides ready-to-flash initiator and reflector samples for Channel Sounding evaluation.
* [`mars-cs-nrf54lm`](https://github.com/Metirionic/mars-cs-nrf54lm) — Zephyr RTOS firmware for Nordic nRF54LM20-based hardware. Provides initiator and reflector samples for Channel Sounding evaluation, with prebuilt firmware releases for quick evaluation.
* [`mars-bluetooth-hci`](https://github.com/Metirionic/mars-bluetooth-hci) — Rust library for parsing Bluetooth HCI events related to Channel Sounding and making CS measurement data available to MARS or custom applications.

## Public repositories

| Repository                                                               | Language / Type | Description                                                                             |
| ------------------------------------------------------------------------ | --------------: | --------------------------------------------------------------------------------------- |
| [`mars-ranging-demo`](https://github.com/Metirionic/mars-ranging-demo)   |     Windows GUI | Channel Sounding Evaluation Application for live distance visualization and data export |
| [`mars-cs-nrf54l`](https://github.com/Metirionic/mars-cs-nrf54l)         |      C / Zephyr | nRF54L15 Channel Sounding firmware samples for initiator and reflector roles            |
| [`mars-cs-nrf54lm`](https://github.com/Metirionic/mars-cs-nrf54lm)       |      C / Zephyr | nRF54LM20 Channel Sounding firmware samples for initiator and reflector roles           |
| [`mars-bluetooth-hci`](https://github.com/Metirionic/mars-bluetooth-hci) |            Rust | Bluetooth HCI parser for Channel Sounding events and MARS integration                   |


## Learn more

- [Metirionic Advanced Ranging Stack (MARS)](https://metirionic.com/products-and-services/mars/)
- [How Channel Sounding works](https://metirionic.com/metirionic-technology/how-it-works/)
- [Evaluation Kit & Demo App](https://metirionic.com/products-and-services/evaluation-kits-and-applications/)
- [LinkedIn](https://www.linkedin.com/company/metirionic) · [YouTube](https://www.youtube.com/channel/UCsDorFeM-ZlLZtv9t5_JDUQ)
