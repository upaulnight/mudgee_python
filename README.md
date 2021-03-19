# mudgee_python
A simple python wrapper for ayyoob/MUDgee that allows for multiple capture files to be merged and used in the file generation

# Prerequisites:
1. Install MUDgee: https://github.com/ayyoob/mudgee
2. Install mergecap: https://www.wireshark.org/docs/man-pages/mergecap.html

# Example Usage:
```python
from generate_mudfile import MUDgeeWrapper

mud_generator = MUDgeeWrapper()
pcap_list = ["test1.pcap", "test2.pcap", "test3.pcap"]
mud_generator.set_device(mac="01:23:45:67:89:ab", name="Example IoT Device")
mud_generator.set_gateway(mac="fe:dc:ba:98:76:54", ip="192.168.0.1", ipv6="::")
mud_generator.gen_mudfile(pcap_list)
```

The MUD File will be saved to the `./mudfile` directory

# Disclaimer
There are no claimed guarantees of accuracy for the MUD file generated. This script/class simply formats the desired inputs and merges capture files to be fed into ayyoob/mudgee
