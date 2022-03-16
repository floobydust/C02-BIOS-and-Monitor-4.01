# C02-BIOS-and-Monitor-4.01
Updated C02BIOS and C02Monitor to Version 4.01

This updated BIOS and Monitor version support a prototype 3.3V SBC based on the C02 Pocket SBC V2
 - NXP SC28L92 DUART (replaces SCC2691 UART)
 - Hitachi MicroDrive (replaces Compact Flash Card)
 - AT28BV256 EEPROM (replaces AT28C256 EEPROM)
 - Other chips are replaced with 3.3V versions as required

New functions provide for:
 - Supports the second UART port with 128-byte receive and transmit circular buffers located at $0400
 - Enable/Disable Write Cache on the MicroDrive (enabled by default)
 - Multiple Block Read/Write access to the MicroDrive - improves performance
 - Ability to write to the AT28BV256 EEPROM insitu (unlock code sequence added to Monitor)
 - 
