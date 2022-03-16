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

MD Util ZIP file comntains a utility for the Realtime Clock and MicroDrive
 - RTC setup: prompts for date/time and sets up RTC values
 - Sets up the NVRAM two-byte signature (required by BIOS to find the RTC)
 - Clears the Alarm functions if desired
 - Can Read/Display the NVRAM contents
 - Can Write the NVRAM contents from any 256 bytes of memory (memory not edited via utility)

 - Can show Identify information for the MicroDrive (condensed useful parameters)
 - Can Read any LBA on the drive, a Next key allows sequential reads
 - Can Write any LBA on the drive (prompts for this)
 - Can sequentially Read or Write the entire drive
 - Provides Performance Benchmarking for Read or Write
   - Prompts for a starting LBA
   - Reads or Writes 16MB of sequential blocks
   - Uses the BIOS multiple block read/write function for a 16KB block (32 LBAs)
   - Shows the total time in seconds to complete the benchmark (accuracy to 10 milliseconds)
