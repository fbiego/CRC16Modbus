# CRC16Modbus

### Usage

    val bytes = ByteArray(10)
    for (x in 0 until 10){
        bytes[9-x] = x.toByte()
    }
    
    val crc = CRC16Modbus()
    crc.update(bytes)
    val checkSum = crc.crcBytes
    println(String.format("CheckSum = 0x%02X, 0x%02X", checkSum[0], checkSum[1]))
