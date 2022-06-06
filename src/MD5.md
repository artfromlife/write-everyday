# md5 ?
Message Digest Algorithm

 N * 512 + 448 + (message.length % 264 -> 64 bit) -> (N + 1) * 512
 base 1 0 0 0 ... to fill end then 

each 512 do cal 64 times

got 128 bit HashCode
